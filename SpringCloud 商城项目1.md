# 商城项目鉴赏

有助于对分布式部署的微服务有个全局的初步认识，便于查漏补缺。

![image-20221029150134304](SpringCloud学习笔记.assets/image-20221029150134304.png)

## p04 服务架构图

https://www.bilibili.com/video/BV1np4y1C7Yf?p=4

![image-20221029150459429](SpringCloud学习笔记.assets/image-20221029150459429.png)

## P505、简介-项目微服务划分图](https://www.bilibili.com/video/BV1np4y1C7Yf?p=5)

![image-20221029151215942](SpringCloud学习笔记.assets/image-20221029151215942.png)

## [15、环境-数据库初始化](https://www.bilibili.com/video/BV1np4y1C7Yf?p=15)

powerdesiner

## [P16、快速开发-人人开源搭建后台管理系统14:11](https://www.bilibili.com/video/BV1np4y1C7Yf?p=16)

人人开源

## [17、快速开发-逆向工程搭建&使用](https://www.bilibili.com/video/BV1np4y1C7Yf?p=17)

代码生成器：生成基本的增删改查代码

## [P20、分布式组件-SpringCloud Alibaba简介10:45](https://www.bilibili.com/video/BV1np4y1C7Yf?p=20)

![image-20221029154035211](SpringCloud学习笔记.assets/image-20221029154035211.png)

![image-20221029154341990](SpringCloud学习笔记.assets/image-20221029154341990.png)

## [21、分布式组件-SpringCloud Alibaba-Nacos注册中心09:20](https://www.bilibili.com/video/BV1np4y1C7Yf?p=21)

部署并启动 nacos：

![image-20221029155454192](SpringCloud学习笔记.assets/image-20221029155454192.png)

引入依赖：

![image-20221029155523547](SpringCloud学习笔记.assets/image-20221029155523547.png)

使用 nacos 做注册中心需要添加的配置：

![image-20221029155303745](SpringCloud学习笔记.assets/image-20221029155303745.png)

启动类上加个注解：

![image-20221029155412150](SpringCloud学习笔记.assets/image-20221029155412150.png)

然后启动一个服务，服务就能注册到注册中心。

## [P22、分布式组件-SpringCloud-OpenFeign测试远程调用](https://www.bilibili.com/video/BV1np4y1C7Yf?p=22)

从注册中心找服务，然后调用接口。

![image-20221029155750353](SpringCloud学习笔记.assets/image-20221029155750353.png)

以上是调用 gulimall-ware 服务的 /ware/waresku/skus 远程接口。

## [P23、分布式组件-SpringCloud Alibaba-Nacos 配置中心-简单示例15:08](https://www.bilibili.com/video/BV1np4y1C7Yf?p=23)

启动 nacos 服务器。

导入依赖：

![image-20221029160640319](SpringCloud学习笔记.assets/image-20221029160640319.png)

bootstrap.properties 文件是springboot 标准规定的，该配置中的文件会优先与 application.yml 文件读取。

里面配置 引用名称、nacos 配置中心的地址。

需要提前在nacos的远程配置中添加  当前应用名.properties 文件。

![image-20221029160714778](SpringCloud学习笔记.assets/image-20221029160714778.png)

注意：打开动态刷新注解，能动态获取到值。

![image-20221029161650055](SpringCloud学习笔记.assets/image-20221029161650055.png)

配置中心有的优先用配置中心的配置。

## [24、分布式组件-SpringCloud Alibaba-Nacos配置中心-命名空间与配置分组16:50](https://www.bilibili.com/video/BV1np4y1C7Yf?p=24)

![image-20221029175512291](SpringCloud学习笔记.assets/image-20221029175512291.png)

* **使用配置空间进行配置隔离**

项目中使用某个命名空间的配置，使用命名空间的 id，不能使名字。

![image-20221029175654024](SpringCloud学习笔记.assets/image-20221029175654024.png)

配置集id、配置分组：

![image-20221029180645636](SpringCloud学习笔记.assets/image-20221029180645636.png)

## [25、分布式组件-SpringCloud Alibaba-Nacos配置中心-加载多配置集10:54](https://www.bilibili.com/video/BV1np4y1C7Yf?p=25)

加载多个配置集：

![image-20221029181157825](SpringCloud学习笔记.assets/image-20221029181157825.png)

![image-20221029181308748](SpringCloud学习笔记.assets/image-20221029181308748.png)

![image-20221029181614827](SpringCloud学习笔记.assets/image-20221029181614827.png)

## [26、分布式组件-SpringCloud-Gateway网关核心概念&原理14:01](https://www.bilibili.com/video/BV1np4y1C7Yf?p=26)

![image-20221029181852286](SpringCloud学习笔记.assets/image-20221029181852286.png)

1. 服务路由。
2. 在网关层做统一的数据处理。   鉴权、限流、日志输出  

![image-20221029182124332](SpringCloud学习笔记.assets/image-20221029182124332.png)

 ![image-20221029182159030](SpringCloud学习笔记.assets/image-20221029182159030.png)

* 路由：定义一些路由规则
* 断言：匹配请求的任何信息，判断路由到哪个服务

* 过滤器：请求和相应都可能被修改

![image-20221029182428727](SpringCloud学习笔记.assets/image-20221029182428727.png)



## [27、分布式组件-SpringCloud-Gateway-创建&测试API网关12:23](https://www.bilibili.com/video/BV1np4y1C7Yf?p=27)

Gateway 官网： https://spring.io/guides/gs/gateway/

![image-20221029183007316](SpringCloud学习笔记.assets/image-20221029183007316.png)

![image-20221029183157931](SpringCloud学习笔记.assets/image-20221029183157931.png)

## [27、分布式组件-SpringCloud-Gateway-创建&测试API网关12:23](https://www.bilibili.com/video/BV1np4y1C7Yf?p=27)

![image-20221029183841238](SpringCloud学习笔记.assets/image-20221029183841238.png)

网关在用的时候，参考官方文档配置即可。

## [61、商品服务-API-品牌管理-云存储开通与使用13:17](https://www.bilibili.com/video/BV1np4y1C7Yf?p=61)

文件存储

* 这种方式需要将文件流经过应用服务器中转

![image-20221029203550303](SpringCloud学习笔记.assets/image-20221029203550303.png)

* 应用服务器只是返回防伪签名给用户，用户直接上传文件到oss

![image-20221029203727127](SpringCloud学习笔记.assets/image-20221029203727127.png)

## [66、商品服务-API-品牌管理-JSR303数据校验16:52](https://www.bilibili.com/video/BV1np4y1C7Yf?p=66)

notnull  notEmpty 

## [P101、分布式基础篇总结11:11](https://www.bilibili.com/video/BV1np4y1C7Yf?p=101)

![image-20221029204421048](SpringCloud学习笔记.assets/image-20221029204421048.png)

使用 **网关做统一的跨域解决方案**：

![image-20221029204731061](SpringCloud学习笔记.assets/image-20221029204731061.png)

# 商城 分布式 高级篇

## [102、全文检索-ElasticSearch-简介14:59](https://www.bilibili.com/video/BV1np4y1C7Yf?p=102)

![image-20221029210256427](SpringCloud学习笔记.assets/image-20221029210256427.png)

![image-20221029210333720](SpringCloud学习笔记.assets/image-20221029210333720.png)

![image-20221029211810081](SpringCloud学习笔记.assets/image-20221029211810081.png)

![image-20221029214446685](SpringCloud学习笔记.assets/image-20221029214446685.png)

上面三个分别对应  ：  **数据库  数据表  数据**

![image-20221029214600083](SpringCloud学习笔记.assets/image-20221029214600083.png)

全文检索。

## [105、全文检索-ElasticSearch-入门-_cat](https://www.bilibili.com/video/BV1np4y1C7Yf?p=105)

通过 restful api 查询

![image-20221104200954543](SpringCloud学习笔记.assets/image-20221104200954543.png)

![image-20221104201035559](SpringCloud学习笔记.assets/image-20221104201035559.png)

相当于给 customer 库下的 external 表下。

![image-20221104201527501](SpringCloud学习笔记.assets/image-20221104201527501.png)

![image-20221104202035773](SpringCloud学习笔记.assets/image-20221104202035773.png)

![image-20221104202437908](SpringCloud学习笔记.assets/image-20221104202437908.png)

![image-20221104202642544](SpringCloud学习笔记.assets/image-20221104202642544.png)

![image-20221104203150106](SpringCloud学习笔记.assets/image-20221104203150106.png)

## [110、全文检索-ElasticSearch-进阶-两种查询方式10:53](https://www.bilibili.com/video/BV1np4y1C7Yf?p=110)

![image-20221104203427539](SpringCloud学习笔记.assets/image-20221104203427539.png)

![image-20221104205600227](SpringCloud学习笔记.assets/image-20221104205600227.png)

![image-20221104210015954](SpringCloud学习笔记.assets/image-20221104210015954.png)

## [111、全文检索-ElasticSearch-进阶-QueryDSL基本使用&match_all](https://www.bilibili.com/video/BV1np4y1C7Yf?p=111)

## [P112112、全文检索-ElasticSearch-进阶-match全文检索](https://www.bilibili.com/video/BV1np4y1C7Yf?p=112)

![image-20221104210414748](SpringCloud学习笔记.assets/image-20221104210414748.png)

全文检索的结果，会根据得分倒排：

![image-20221104210644021](SpringCloud学习笔记.assets/image-20221104210644021.png)

## [113、全文检索-ElasticSearch-进阶-match_phrase短语匹配01:58](https://www.bilibili.com/video/BV1np4y1C7Yf?p=113)

匹配完整短语：

<img src="SpringCloud学习笔记.assets/image-20221104210839635.png" alt="image-20221104210839635" style="zoom:50%;" />

![image-20221104211549567](SpringCloud学习笔记.assets/image-20221104211549567.png)

复合查询：

![image-20221104211740566](SpringCloud学习笔记.assets/image-20221104211740566.png)

满足should条件得分高，排序靠前：

![image-20221104211913515](SpringCloud学习笔记.assets/image-20221104211913515.png)

![image-20221104212014346](SpringCloud学习笔记.assets/image-20221104212014346.png)

![image-20221104213053529](SpringCloud学习笔记.assets/image-20221104213053529.png)

精确查询非文本字段时使用 term，全文检索时使用 match: 

![image-20221104213113420](SpringCloud学习笔记.assets/image-20221104213113420.png)

![image-20221104213751274](SpringCloud学习笔记.assets/image-20221104213751274.png)

## [118、全文检索-ElasticSearch-进阶-aggregations聚合分析](https://www.bilibili.com/video/BV1np4y1C7Yf?p=118)

![image-20221104213948817](SpringCloud学习笔记.assets/image-20221104213948817.png)

![image-20221104214432026](SpringCloud学习笔记.assets/image-20221104214432026.png)

![image-20221104215108374](SpringCloud学习笔记.assets/image-20221104215108374.png)

## [119、全文检索-ElasticSearch-映射-mapping创建](https://www.bilibili.com/video/BV1np4y1C7Yf?p=119)

![image-20221104215849885](SpringCloud学习笔记.assets/image-20221104215849885.png)

![image-20221104220044324](SpringCloud学习笔记.assets/image-20221104220044324.png)

![image-20221104220155167](SpringCloud学习笔记.assets/image-20221104220155167.png)

![image-20221104221016679](SpringCloud学习笔记.assets/image-20221104221016679.png)

可以修改 mapping:

![image-20221104221414407](SpringCloud学习笔记.assets/image-20221104221414407.png)

## [120、全文检索-ElasticSearch-映射-添加新的字段映射03:03](https://www.bilibili.com/video/BV1np4y1C7Yf?p=120)
index 指定该字段能否被索引：

![image-20221104221520910](SpringCloud学习笔记.assets/image-20221104221520910.png)

## [121、全文检索-ElasticSearch-映射-修改映射&数据迁移09:05](https://www.bilibili.com/video/BV1np4y1C7Yf?p=121)

![image-20221105151905473](SpringCloud学习笔记.assets/image-20221105151905473.png)

![image-20221105152947612](SpringCloud学习笔记.assets/image-20221105152947612.png)

![image-20221105153022209](SpringCloud学习笔记.assets/image-20221105153022209.png)

![image-20221105152718115](SpringCloud学习笔记.assets/image-20221105152718115.png)

![image-20221105153704938](SpringCloud学习笔记.assets/image-20221105153704938.png)

## [125、全文检索-ElasticSearch-整合-SpringBoot整合high-level-client19:48](https://www.bilibili.com/video/BV1np4y1C7Yf?p=125)

![image-20221105160058326](SpringCloud学习笔记.assets/image-20221105160058326.png)

![image-20221105160211350](SpringCloud学习笔记.assets/image-20221105160211350.png)

可参考官方文档。

## [126、全文检索-ElasticSearch-整合-测试保存13:03](https://www.bilibili.com/video/BV1np4y1C7Yf?p=126)

## [129、商城业务-商品上架-nested数据类型场景05:14](https://www.bilibili.com/video/BV1np4y1C7Yf?p=129)

数据类型为 nested时：

![image-20221105170249162](SpringCloud学习笔记.assets/image-20221105170249162.png)

![image-20221105170010770](SpringCloud学习笔记.assets/image-20221105170010770.png)

## [P139139、商城业务-nginx-搭建域名访问环境一（反向代理配置）24:52](https://www.bilibili.com/video/BV1np4y1C7Yf?p=139)

![image-20221105171431165](SpringCloud学习笔记.assets/image-20221105171431165.png)

![image-20221105171518856](SpringCloud学习笔记.assets/image-20221105171518856.png)

## [145、性能压测-性能监控-jvisualvm使用11:27](https://www.bilibili.com/video/BV1np4y1C7Yf?p=145)

![image-20221105200338188](SpringCloud学习笔记.assets/image-20221105200338188.png)

Jvisualvm 功能更强大，jdk1.6 后提供。

![image-20221105201357649](SpringCloud学习笔记.assets/image-20221105201357649.png)

![image-20221105202004860](SpringCloud学习笔记.assets/image-20221105202004860.png)

## [P148148、性能压测-优化-nginx动静分离13:23](https://www.bilibili.com/video/BV1np4y1C7Yf?p=148)

动静分离，提高性能。

![image-20221105205934281](SpringCloud学习笔记.assets/image-20221105205934281.png)

## [149、性能压测-优化-模拟线上应用内存崩溃宕机情况09:05](https://www.bilibili.com/video/BV1np4y1C7Yf?p=149)

压测的同时监控 gc

![image-20221106151041875](SpringCloud学习笔记.assets/image-20221106151041875.png)

## [150、性能压测-优化-优化三级分类数据获取07:20](https://www.bilibili.com/video/BV1np4y1C7Yf?p=150)

数据库多次查询优化。提前查询存内存。

## [151、缓存-缓存使用-本地缓存与分布式缓存15:37](https://www.bilibili.com/video/BV1np4y1C7Yf?p=151)
![image-20221106151515384](SpringCloud学习笔记.assets/image-20221106151515384.png)

![image-20221106152508521](SpringCloud学习笔记.assets/image-20221106152508521.png)

![image-20221106153717484](SpringCloud学习笔记.assets/image-20221106153717484.png)

具体操作如下：

![image-20221106153819152](SpringCloud学习笔记.assets/image-20221106153819152.png)

