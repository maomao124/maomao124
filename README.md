每天一点代码，纪录自己成长

<br>

## 学习笔记

* **集信达短信平台学习笔记**         2022/12/14 - 2023/01/05  [点击进入](https://github.com/maomao124/sms_study_notes)
* **RocketMQ学习笔记**                2022/11/29 - 2022/12/12  [点击进入](https://github.com/maomao124/RocketMQ_study_notes)
* **LoadRunner学习笔记**             2022/11/24 - 2022/11/26   [点击进入](https://github.com/maomao124/LoadRunner_study_notes)
* **Xenu_Link_Sleuth学习笔记**   2022/11/24 - 2022/11/24   [点击进入](https://github.com/maomao124/Xenu_Link_Sleuth_study_notes)
* **MongoDB学习笔记**                  2022/11/14 - 2022/11/27   [点击进入](https://github.com/maomao124/MongoDB_study_notes)
* **通用权限系统实战学习笔记**     2022/10/26 - 2022/11/14   [点击进入](https://github.com/maomao124/authority_study_notes)
* **j2cache学习笔记**                      2022/11/05 - 2022/11/06   [点击进入](https://github.com/maomao124/j2cache_study_notes)
* **jwt学习笔记**                              2022/11/02 - 2022/11/03  [点击进入](https://github.com/maomao124/jwt_study_notes)
* **logback学习笔记**                     2022/10/31 - 2022/11/01   [点击进入](https://github.com/maomao124/logback_study_notes)
* **AntiSamy学习笔记**                 2022/10/30 - 2022/10/31   [点击进入](https://github.com/maomao124/AntiSamy_study_notes)
* **hibernate validator学习笔记**  2022/10/29 - 2022/10/29   [点击进入](https://github.com/maomao124/hibernate_validator_study_notes)
* **dozer学习笔记**                         2022/10/28 - 2022/10/29   [点击进入](https://github.com/maomao124/dozer_study_notes)
* **swagger学习笔记**                    2022/10/26 - 2022/10/27   [点击进入](https://github.com/maomao124/swagger_study_notes)
* **lombok学习笔记**                      2022/10/26 - 2022/10/26   [点击进入](https://github.com/maomao124/lombok_study_notes)
* **面试学习笔记**                             2022/10/16 -                       [点击进入](https://github.com/maomao124/interview_study_notes)
* **Android学习笔记**                     2022/09/17 - 2022/10/14    [点击进入](https://github.com/maomao124/Android_study_notes)
* **java并发编程学习笔记**            2022/08/26 - 2022/09/16   [点击进入](https://github.com/maomao124/java_concurrent_programming_study_notes)
* **java设计模式学习笔记**            2022/08/09 - 2022/08/25   [点击进入](https://github.com/maomao124/java_design_patterns_study_notes)
* **SpringSecurity学习笔记**        2022/07/31 - 2022/08/09   [点击进入](https://github.com/maomao124/SpringSecurity_studyNotes)
* **SpringCloud学习笔记**            2022/07/09 - 2022/07/30  [点击进入](https://github.com/maomao124/SpringCloud_StudyNotes)
* **redis学习笔记**                          2022/05/17 - 2022/06/29   [点击进入](https://github.com/maomao124/redisStudyNotes)
* **Linux学习笔记**                         2022/07/07 - 2022/07/17  [点击进入](https://github.com/maomao124/Linux_StudyNotes)
* **Git学习笔记**                              2022/06/30 - 2022/07/01  [点击进入](https://github.com/maomao124/GitStudyNotes)
* **MySql学习笔记**                        2022/05/11 - 2022/06/23   [点击进入](https://github.com/maomao124/MySql_study_notes)
* **Docker学习笔记**                     2022/05/31 - 2022/06/20   [点击进入](https://github.com/maomao124/Docker_studyNotes)
* **elasticsearch学习笔记**         2022/05/24 - 2022/06/05   [点击进入](https://github.com/maomao124/elasticsearch_studyNotes)
* **redis学习笔记**                        2022/05/17 - 2022/06/29   [点击进入](https://github.com/maomao124/redisStudyNotes)
* ......



<br>

<br>

<br>





## 项目

**小项目非常多，只列举一部分代码行数在5000行以上的项目**



<br>



#### 集信达短信平台

* 时间：2022/12/14 - 2023/01/05
* 项目名称：sms-backend
* 技术：SpringBoot、Nacos、Mybatis Plus、redis、Redission分布式锁等
* 项目地址：[点击进入](https://github.com/maomao124/sms-backend)
* 代码行数：55000行左右
* 项目介绍：一个统一入口、减少对接成本、同时兼顾多种短信业务、简单易行的操作与维护、高稳定、高可靠的短信平台。通过智能动态的通道评级、选举、降级、热插拔，增强了系统的健壮性，摆脱对单一通道的依赖。并且提供多种对接方式的短信发送和管理平台



项目模块：

```sh
sms-backend                      # 聚合工程，用于聚合parent、apps、tools等模块
  ├── parent				     # 父工程，nacos配置及依赖包管理
  ├── apps					     # 应用目录
  	   ├── auth				     # 权限服务父工程
  		   ├── auth-entity       # 权限实体
  		   ├── auth-server       # 权限服务
  	   ├── gateway			     # 网关服务
  	   ├── sms            	     # 短信平台父工程
  	        ├──sms-entity		 # 短信平台实体
  	        ├──sms-dao           # 短信平台的数据持久化模块，主要包括mybatis plus的mapper文件和mapper接口
  	        ├──sms-manage		 # 系统管理服务
  	        ├──sms-api			 # 短信接收服务，应用系统调用接口、发送短信
  	        ├──sms-server		 # 短信发送服务，调用短信通道、发送短信
  	        └──sms-sdk			 # 短信SDK，应用系统引入、发送短信
  └── tools				         # 工具工程
  	   ├── tools-common		     # 基础组件：基础配置类、函数、常量、统一异常处理、undertow服务器
  	   ├── tools-core		     # 核心组件：基础实体、返回对象、上下文、异常处理、分布式锁、函数、树
  	   ├── tools-databases	     # 数据源组件：数据源配置、数据权限、查询条件等
  	   ├── tools-dozer		     # 对象转换：dozer配置、工具
  	   ├── tools-redis-cache    # redis分布式缓存工具类和分布式锁服务，缓存工具类解决著名的3个缓存问题
  	   ├── tools-j2cache	     # 缓存组件：j2cache、redis缓存
  	   ├── tools-jwt             # JWT组件：配置、属性、工具
  	   ├── tools-log	         # 日志组件：日志实体、事件、拦截器、工具
  	   ├── tools-swagger2	     # 文档组件：knife4j文档
  	   ├── tools-user            # 用户上下文：用户注解、模型和工具，当前登录用户信息注入模块
   	   ├── tools-validator	     # 表单验证： 后台表单规则验证
  	   ├── tools-xss		     # xss防注入组件
```









<br>

<br>

<br>



#### 通用权限系统

* 时间：2022/10/25 - 2022/11/14
* 项目名称：authority
* 技术：SpringBoot、Zuul、Nacos、Fegin、Ribbon、Hystrix、JWT Token、Mybatis Plus、AntiSamy、j2cache、dozer等
* 项目地址：[点击进入](https://github.com/maomao124/authority)
* 代码行数：28900行左右
* 项目介绍：对于企业中的项目绝大多数都需要进行用户权限管理、认证、鉴权、加密、解密、XSS防跨站攻击等。这些功能整体实现思路基本一致，但是大部分项目都需要实现一次，这无形中就形成了巨大的资源浪费。本项目就是针对这个问题，提供了一套通用的权限解决方案。项目具备通用的用户管理、资源权限管理、网关统一鉴权、XSS防跨站攻击等多个模块，支持多业务系统并行开发，支持多服务并行开发，可以作为后端服务的开发脚手架去使用。



项目模块：

```sh
authority                    #聚合工程，用于聚合parent、apps、tools等模块
├── parent				     # 父工程，nacos配置及依赖包管理
├── apps					 # 应用目录
	├── auth				 # 权限服务父工程
		├── auth-entity      # 权限实体
		├── auth-server      # 权限服务
	├── gateway			     # 网关服务
└── tools				     # 工具工程
	├── tools-common		 # 基础组件：基础配置类、函数、常量、统一异常处理、undertow服务器
	├── tools-core		     # 核心组件：基础实体、返回对象、上下文、异常处理、分布式锁、函数、树
	├── tools-databases	     # 数据源组件：数据源配置、数据权限、查询条件等
	├── tools-dozer		     # 对象转换：dozer配置、工具
	├── tools-redis-cache    # redis分布式缓存工具类和分布式锁服务，缓存工具类解决著名的3个缓存问题
	├── tools-j2cache	     # 缓存组件：j2cache、redis缓存
	├── tools-jwt            # JWT组件：配置、属性、工具
	├── tools-log	         # 日志组件：日志实体、事件、拦截器、工具
	├── tools-swagger2	     # 文档组件：knife4j文档
	├── tools-user           # 用户上下文：用户注解、模型和工具，当前登录用户信息注入模块
	├── tools-validator	     # 表单验证： 后台表单规则验证
	├── tools-xss		     # xss防注入组件
```





<br>

<br>

<br>





#### 漫画app

* 时间：2022/10/12 - 2022/10/26
* 项目名称：CartoonApp
* 技术：Android
* 项目地址：[点击进入](https://github.com/maomao124/CartoonApp)
* 代码行数：11500行左右
* 项目介绍：一款基于安卓的观看漫画的app，实现了漫画排行榜、漫画目录、收藏夹、历史记录、漫画搜索、漫画更新推送服务等



<br>

<br>

<br>



#### 酒店管理项目

* 时间：2022/05/?? - 2022/06/04
* 项目名称：elasticsearch_hotel_management、elasticsearch_hotel_final
* 技术：elasticsearch、rabbitMQ、spring boot
* 项目地址：[elasticsearch_hotel_management](https://github.com/maomao124/elasticsearch_hotel_management) 、 [elasticsearch_hotel_final](https://github.com/maomao124/elasticsearch_hotel_final)
* 代码行数：前端1000行、后端4000行
* 项目介绍：写这个项目的目的是学习elasticsearch





<br>

<br>

<br>



#### 黑马点评项目

* 时间：2022/05/12 - 2022/05/21
* 项目名称：spring_boot_redis_hmdp_final
* 技术：redis、Redisson、spring boot
* 项目地址：[点击进入](https://github.com/maomao124/spring_boot_redis_hmdp_final)
* 代码行数：10821行
* 项目介绍：
* 这是一个以学习redis为目的的前后端分离的项目。
  学完本项目收获：
  1.分布式环境下基于token实现登录
  2.使用redis作为缓存来查询商户信息，解决缓存穿透、缓存雪崩、缓存击穿问题，封装缓存操作工具类
  3.缓存更新策略
  4.优惠券秒杀，超卖问题解决方案，乐观锁
  5.redisson分布式锁
  6.使用消息队列实现异步秒杀
  7.使用redis实现点赞功能
  8.使用redis实现好友共同关注
  9.使用redis的GEO数据结构实现查询附近商铺功能
  10.使用redis的bitmap数据结构实现用户签到



<br>

<br>

<br>



#### 数据库课程设计_基于mysql的学生信息管理系统javaWeb实现

* 时间：2022/01/31 - 2022/02/23
* 项目名称：Java_Web_Implementation_of_student_information_management_system_based_on_MySQL
* 技术：javaweb、JDBC、JDBC连接池、MySQL、servlet、jsp、jstl、HTML、CSS、js、animate动画库
* 项目地址：[点击进入](https://github.com/maomao124/Java_Web_Implementation_of_student_information_management_system_based_on_MySQL)
* 代码行数：33403行
* 项目介绍：数据库课程设计、目的是学习怎么使用JDBC去操作mysql数据库，写这个项目的目的是学习jdbc的操作、html、css、jsp等



<br>

<br>

<br>







#### java课程设计 Swing实现文本编辑器

* 时间：2021/12/07 - 2021/12/22
* 项目名称：java_course_design_Swing_implements_text_editor
* 技术：java swing
* 项目地址：[点击进入](https://github.com/maomao124/java_course_design_Swing_implements_text_editor)
* 代码行数：6044行
* 项目介绍：基于java swing实现的文本编辑器











