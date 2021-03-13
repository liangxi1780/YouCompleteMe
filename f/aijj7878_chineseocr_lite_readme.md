## 本项目基于[chineseocr](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046aa893c680988bb89dfa6347b40b788e8ce6e068b6233028d8d1e898c4af805d7)  与[psenet](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046cf7520ef14a61b6ccfbab8a47743068b335e9079d60a10a379debc471d4a68fb)   实现中文自然场景文字检测及识别

# 环境
pytorch  1.2.0
linux/macos
## PSENET 编译
``` Bash
cd psenet/pse
rm -rf pse.so 
make 
```
  
# 实现功能
- [x]  提供轻量的backone检测模型psenet（8.5M）,crnn_lstm_lite(9.5M) 和行文本方向分类网络（1.5M）
- [x]  任意方向文字检测，识别时判断行文本方向 
- [x]  crnn\crnn_lite lstm\dense识别（ocr-dense和ocr-lstm是搬运[chineseocr]https://github.com/chineseocr/chineseocr)的）   
- [x]  支持竖排文本识别  
- [x]  ncnn 实现 (支持lstm) nihui大佬实现的[crnn_lstm推理](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046294e366ebf543a12622db37cbfb26e65f6d6bf9795f1ce3c699bf1a252a4e55c4a8641ade9792d9c0310a5df797fe784)  具体操作详解: [详细记录超轻量中文OCR LSTM模型ncnn实现](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e9931a2f3f13db0aebba2398a83a5121ef4516395e6f5c8623cf375e898375a2420da045364ab28942301e9a6c8ee7dd59c5f77b4a825f7bf17c6597786964d614308f4cda5c624ad9caf67ca8646d7b0cf5) 
- [x]  提供竖排文字样例以及字体库（旋转90度的字体）
- [ ]  mnn  实现 


# 2020.03.16更新
- psenet ncnn核扩展实现，有效解决粘连文本检测问题，详见[ncnn ocr一条龙](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046294e366ebf543a12622db37cbfb26e655467132918d31cf8324e3ea77695b6db54c7b828c55499edb59fcf75c387140a4512a4022c25c4aa1d3d4bc611c01f77) 
- nihui大佬实现的[crnn_lstm推理](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046294e366ebf543a12622db37cbfb26e65f6d6bf9795f1ce3c699bf1a252a4e55c4a8641ade9792d9c0310a5df797fe784)  具体操作详解: [详细记录超轻量中文OCR LSTM模型ncnn实现](http://u.720life.cn/g/85a9f52868358c3208a4b5fd9062e9931a2f3f13db0aebba2398a83a5121ef4516395e6f5c8623cf375e898375a2420da045364ab28942301e9a6c8ee7dd59c5f77b4a825f7bf17c6597786964d614308f4cda5c624ad9caf67ca8646d7b0cf5) 

# 2020.03.12更新
- 升级crnn_lite_lstm_dw.pth模型crnn_lite_lstm_dw_v2.pth , 精度更高



## 竖排字体样式：
   

## 竖排生成的竖排文本样例：
   
   
   
   
  


 


## web服务启动
``` Bash
cd chineseocr_lite## 进入chineseocr目录
python app.py 8080 ##8080端口号，可以设置任意端口
```

## 访问服务
http://127.0.0.1:8080/ocr


## 识别结果展示

 
 
 
 
 


## ncnn检测识别展示(x86 cpu 单进程)
 
 



## 参考
1. ncnn  https://github.com/Tencent/ncnn         
2. crnn  https://github.com/meijieru/crnn.pytorch.git              
3. chineseocr  https://github.com/chineseocr/chineseocr      
4. Psenet https://github.com/WenmuZhou/PSENet.pytorch  
5. 语言模型实现 https://github.com/lukhy/masr



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)