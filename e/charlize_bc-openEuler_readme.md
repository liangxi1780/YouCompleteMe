# bc RPM package for openEuler
    
[bc](http://u.720life.cn/g/80aceec34af2d650b057d93ea119d365124e2d98e5366e31114ec7e1502c8b84)  is an arbitrary precision numeric processing language. Syntax is similar to C, but differs in many substantial areas. It supports interactive execution of statements.

# Build Package
 
To build a RPM package, create packaging scaffold with `rpmdev-setuptree`
if it doesn't exist.
Then copy bc-1.07.1.tar.gz ([upstream URL](http://u.720life.cn/g/64d339796635e776c984a2b987d723265de4dfbfca1670fc4a6145e3df541752fc064d57ad3a28afd79cbb4621f2567e) 
to ~/rpmbuild/SOURCES, bc.spec to ~/rpmbuild/SPECS, and run:
```
rpmlint bc.spec
rpmbuild -bs bc.spec
rpmbuild -bb bc.spec
```

To be verified on openEuler 20.03 (LTS).




 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)