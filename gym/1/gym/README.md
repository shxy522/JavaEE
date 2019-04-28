GYM DEMO
===========================
##功能总览
* 登录注册
* 跳转登录页面
* 发帖删帖
* 页面待完成

##项目依赖
* JDK:1.8
* maven:4.0.0
* spring boot:2.1.4
* mysql:5.7.20
* redis:3.2.100

##技术总览
* jpa
    * 使用jpa标准接口默认hibernate框架实现数据库建表和存储
* security
    * 使用spring security拦截未认证请求
    * 密码加密后入库
    * 多角色权限管理 ***待完成***
* cache
    * 实现spring cache连接windows redis对请求结果进行缓存
    
##目录结构说明
│  .gitattributes
│  .gitignore
│  
└─gym
    │  .classpath
    │  .gitignore
    │  .project
    │  mvnw
    │  mvnw.cmd
    │  pom.xml
    │  README.md                                                        //文档
    │  
    ├─.mvn
    │  └─wrapper
    │          maven-wrapper.jar
    │          maven-wrapper.properties
    │          MavenWrapperDownloader.java
    │          
    ├─.settings
    │      org.eclipse.core.resources.prefs
    │      org.eclipse.jdt.apt.core.prefs
    │      org.eclipse.jdt.core.prefs
    │      org.eclipse.m2e.core.prefs
    │      
    ├─src
    │  ├─main
    │  │  ├─java
    │  │  │  └─edu
    │  │  │      └─bjtu
    │  │  │          └─ee4j
    │  │  │              └─gym
    │  │  │                  │  GymApplication.java                    //应用入口
    │  │  │                  │  
    │  │  │                  ├─config
    │  │  │                  │      SecurityConfig.java                //security权限管理：拦截未认证请求+密码加密
    │  │  │                  │      
    │  │  │                  ├─controller
    │  │  │                  │      AuthController.java
    │  │  │                  │      PageController.java                //测试文件
    │  │  │                  │      PostController.java                //表单管理：实现spring cache连接windows redis对请求结果进行缓存
    │  │  │                  │      
    │  │  │                  ├─exception                               //异常处理
    │  │  │                  │      PostExceptionHandler.java
    │  │  │                  │      PostNotFoundException.java
    │  │  │                  │      
    │  │  │                  ├─model
    │  │  │                  │      Post.java
    │  │  │                  │      PostShares.java
    │  │  │                  │      User.java
    │  │  │                  │      UserAuth.java
    │  │  │                  │      
    │  │  │                  ├─repository
    │  │  │                  │      AuthRepository.java
    │  │  │                  │      PostRepository.java
    │  │  │                  │      UserRepository.java
    │  │  │                  │      
    │  │  │                  ├─service
    │  │  │                  │      AuthService.java
    │  │  │                  │      PostService.java
    │  │  │                  │      UserDetailsServiceImpl.java
    │  │  │                  │      UserService.java
    │  │  │                  │      
    │  │  │                  └─util
    │  │  │                          StringUtil.java
    │  │  │                          
    │  │  └─resources
    │  │      │  application.properties                             //变量配置
    │  │      │  
    │  │      └─templates
    │  │              login.html                                    //登录页面
    │  │              post.html                                     //表单管理
    │  │              test.html                                     //测试
    │  │              
    │  └─test
    │      └─java
    │          └─edu
    │              └─bjtu
    │                  └─ee4j
    │                      └─gym
    │                              GymApplicationTests.java
    │                              
    └─target
        ├─classes
        │  │  application.properties
        │  │  
        │  └─templates
        │          login.html
        │          post.html
        │          test.html
        │          
        └─test-classes

##小组人员

|姓名|学号|
|---|---|
|迟成|16301001|
|潘雅欣|16301014|
|沈晓宇|16301017|