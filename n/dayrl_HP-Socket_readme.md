# HP-Socket
High Performance Network Framework
## Description
- ***Server*** Based on IOCP/EPOLL communication model, combined with technology of memory pool, private heap etc., efficient memory management is implemented to support large scale and high concurrent communication scenarios.
- ***Agent*** The Agent component is essentially a Multi-Client component that uses the same technical architecture as the Server component. An Agent component object can create and efficiently handle large-scale Socket connections at the same time.
- ***Client*** Based on Event-Select/POLL communication model, each component object creates a communication thread and manages a Socket connection. Client components are suitable for small-scale client scenarios.
## Document
- HP-Socket Development Guide 
[[pdf]](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466fb359854a73b878f711f89abb514e81fe6b2d804b7235aaba7c5d09fbb47fef72b12ac3cec4ff3b799a0ffe76788953) 
- HP-Socket Class Diagram 
[[uml]](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466fb359854a73b878f711f89abb514e81fe6b2d804b7235aaba7c5d09fbb47fef72b12ac3cec4ff3b799a0ffe76788953) 
- HP-Socket Class Diagram 
[[jpg]](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466fb359854a73b878f711f89abb514e81fe6b2d804b7235aaba7c5d09fbb47fef72b12ac3cec4ff3b799a0ffe76788953) 
- HP-Socket SSL Class Diagram 
[[jpg]](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466fb359854a73b878f711f89abb514e81fe6b2d804b7235aaba7c5d09fbb47fef72b12ac3cec4ff3b799a0ffe76788953) 
- HP-Socket HTTP Class Diagram 
[[jpg]](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466fb359854a73b878f711f89abb514e81fe6b2d804b7235aaba7c5d09fbb47fef72b12ac3cec4ff3b799a0ffe76788953) 
## Workflow
1. Create listener object
2. Create component object (and binding with listener object)
3. Start component object
4. Connect to dest host (for *Agent* Component only)
5. process network events (*OnConnect/OnReceive/OnClose* etc.)
6. Stop component object (optional: component object will be stopped before destroy in step 7)
7. Destroy component object
8. Destroy listener object

![Agent Workflow](https://gitee.com/uploads/images/2017/1213/120601_c0d950fb_81720.jpeg "HP-Socket-Agent-Demo.JPG")
## Example
- ***C++ Example***

``` C++
#include  

/* Listener Class */
class CListenerImpl : public CTcpPullServerListener
{

public:
	// 5. process network events
	virtual EnHandleResult OnPrepareListen(ITcpServer* pSender, SOCKET soListen);
	virtual EnHandleResult OnAccept(ITcpServer* pSender, CONNID dwConnID, UINT_PTR soClient);
	virtual EnHandleResult OnHandShake(ITcpServer* pSender, CONNID dwConnID);
	virtual EnHandleResult OnReceive(ITcpServer* pSender, CONNID dwConnID, int iLength);
	virtual EnHandleResult OnSend(ITcpServer* pSender, CONNID dwConnID, const BYTE* pData, int iLength);
	virtual EnHandleResult OnClose(ITcpServer* pSender, CONNID dwConnID, EnSocketOperation enOperation, int iErrorCode);
	virtual EnHandleResult OnShutdown(ITcpServer* pSender);
};

int main(int argc, char* const argv[])
{
	// 1. Create listener object
	CListenerImpl s_listener;
	// 2. Create component object (and binding with listener object)
	CTcpPullServerPtr s_pserver(&s_listener);
	
	// 3. Start component object
	if(!s_pserver->Start("0.0.0.0", 5555))
		exit(1);
	
	/* wait for exit */
	// ... ... 
	
	// 6. (optional) Stop component object
	s_pserver->Stop();

	return 0;
	
	// 7. Destroy component object automatically
	// 8. Destroy listener object automatically
}
```

- ***C Example***

``` C
#include  

// 5. process network events
EnHandleResult __HP_CALL OnConnect(HP_Agent pSender, HP_CONNID dwConnID);
EnHandleResult __HP_CALL OnReceive(HP_Agent pSender, HP_CONNID dwConnID, int iLength);
EnHandleResult __HP_CALL OnSend(HP_Agent pSender, HP_CONNID dwConnID, const BYTE* pData, int iLength);
EnHandleResult __HP_CALL OnClose(HP_Agent pSender, HP_CONNID dwConnID, En_HP_SocketOperation enOperation, int iErrorCode);
EnHandleResult __HP_CALL OnShutdown(HP_Agent pSender);

int main(int argc, char* const argv[])
{
	HP_TcpPullAgentListener s_listener;
	HP_TcpPullAgent s_agent;

	// 1. Create listener object
	s_listener	= ::Create_HP_TcpPullAgentListener();
	// 2. Create component object (and binding with listener object)
	s_agent		= ::Create_HP_TcpPullAgent(s_listener);
	
	/* Set listener callbacks */
	::HP_Set_FN_Agent_OnConnect(s_listener, OnConnect);
	::HP_Set_FN_Agent_OnSend(s_listener, OnSend);
	::HP_Set_FN_Agent_OnPullReceive(s_listener, OnReceive);
	::HP_Set_FN_Agent_OnClose(s_listener, OnClose);
	::HP_Set_FN_Agent_OnShutdown(s_listener, OnShutdown);
	
	// 3. Start component object
	if(::HP_Agent_HasStarted(s_agent))
		exit(1);
	
	// 4. Connect to dest host
	::HP_Agent_Connect(s_agent, "remote.host.1", REMOTE_PORT_1, nullptr);
	::HP_Agent_Connect(s_agent, "remote.host.2", REMOTE_PORT_2, nullptr);
	::HP_Agent_Connect(s_agent, "remote.host.3", REMOTE_PORT_3, nullptr);
	
	/* wait for exit */
	// ... ... 
	
	// 6. (optional) Stop component object
	::HP_Agent_Stop(s_agent);

	// 7. Destroy component object
	::Destroy_HP_TcpPullAgent(s_agent);
	// 8. Destroy listener object
	::Destroy_HP_TcpPullAgentListener(s_listener);
	
	return 0;
}
```

## Component List
- ***Basic Components***

![Basic Component](https://images.gitee.com/uploads/images/2019/0331/102422_3eecfdb7_81720.jpeg "Basic Component - mini.jpg")

- ***SSL Components***

![SSL Component](https://gitee.com/uploads/images/2017/1214/143622_d6c1f436_81720.jpeg "SSL Component - mini.jpg")

- ***HTTP Components***

![HTTP COmponent](https://gitee.com/uploads/images/2017/1214/143640_0eb6f9e4_81720.jpeg "HTTP Component - mini.jpg")

## Reference Projects

- *[jemalloc](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461b5abbd6f030dcef19e8ec1f853d573dbdb6b713f26a53e6c1188ae31d21e139 
- *[openssl](http://u.720life.cn/g/54145d0471d91890860f7f8463c030466211ce577e66b0b644b2e8f1602410b3a55234d424ccf3864543c3f0382a98c6 
- *[http-parser](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d9259ac169db32df0709db579a24498af8d3a1dcc8c841f86e712ae8ef6d55f5 
- *[zlib](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046d1443f87d5b8bd128a8dd0dc5c22d417 
- *[kcp](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046dfc97f672fdf7e9b8871c526ffa2881fbc2ce66aa84b22b547ba4699cfbbc509 


 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)