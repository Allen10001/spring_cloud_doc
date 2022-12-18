# 文章

## 使用Feign实现远程HTTP调用

https://blog.csdn.net/yuanyuan_gugu/article/details/107404955

>Feign 性能优化
> Feign 默认情况下是使用DefaultClient，集成Ribbon的时候使用的是LoadBalancerFeignClient，底层也是DefaultClient，只是加入了负载均衡规则。
>
>而DefaultClient底层是使用的HttpURLConnection来进行请求，是没有连接池支持的。
>我们可以为Feign加入HttpClient或OKHttp支持，来优化Feign的性能。这里我们使用apache的httpClient来完成。
>
>首先添加依赖
>
>```xml
><dependency>
>    <groupId>io.github.openfeign</groupId>
>    <artifactId>feign-httpclient</artifactId>
></dependency>
>```
>
>然后在配置文件中启动并配置连接池
>
>```yml
>feign:
>  httpclient:
>    enabled: true
>    #最大连接数
>    max-connections: 200
>    #单个路径最大连接数
>    max-connections-per-route: 50
>```
>
>修改完成后可以看到，Feign已经使用HttpClient构建LoadBalancerFeignClient。

## [SpringCloud学习系列之四-----配置中心(Config)使用详解 ](https://blog.csdn.net/qazwsxpcm/article/details/88578076)(SpringCloud Config 的基本使用方式)

>

## [微服务：注册中心ZooKeeper、Eureka、Consul 、Nacos对比](https://blog.csdn.net/fly910905/article/details/100023415)

