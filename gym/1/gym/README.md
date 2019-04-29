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
 [toc]   
│  .gitattributes  
│  .gitignore  
│    
└─gym  
    │  .classpath  
    │  .gitignore  
    │  .project  
    │  mvnw  
    │  mvnw.cmd  
    │  pom.xml                                                       //maven管理文件  
    │  README.md                                                     //文档  
    │    
    ├─.mvn  
    │  └─wrapper  
    │          maven-wrapper.jar  
    │          maven-wrapper.properties  
    │          MavenWrapperDownloader.java  
    │        
    ├─src  
    │  ├─main  
    │  │  ├─java                                                    //代码  
    │  │  │  └─edu  
    │  │  │      └─bjtu  
    │  │  │          └─ee4j  
    │  │  │              └─gym  
    │  │  │                  │  GymApplication.java                 //程序入口  
    │  │  │                  │    
    │  │  │                  ├─config  
    │  │  │                  │      SecurityConfig.java             //security权限管理：拦截未认证请求+密码加密  
    │  │  │                  │        
    │  │  │                  ├─controller                           //页面访问控制  
    │  │  │                  │      AuthController.java             //登录注册  
    │  │  │                  │      PageController.java             //测试文件  
    │  │  │                  │      PostController.java             //表单管理：实现spring cache连接windows redis对请求结果进行缓存  
    │  │  │                  │        
    │  │  │                  ├─exception                            //异常处理  
    │  │  │                  │      PostExceptionHandler.java  
    │  │  │                  │      PostNotFoundException.java  
    │  │  │                  │        
    │  │  │                  ├─model                                //实体类  
    │  │  │                  │      Post.java  
    │  │  │                  │      PostShares.java  
    │  │  │                  │      User.java  
    │  │  │                  │      UserAuth.java  
    │  │  │                  │        
    │  │  │                  ├─repository                           //数据访问接口  
    │  │  │                  │      AuthRepository.java  
    │  │  │                  │      PostRepository.java  
    │  │  │                  │      UserRepository.java  
    │  │  │                  │        
    │  │  │                  ├─service                              //数据服务  
    │  │  │                  │      AuthService.java                //权限管理  
    │  │  │                  │      PostService.java                //表单管理  
    │  │  │                  │      UserDetailsServiceImpl.java     //用户详细管理  
    │  │  │                  │      UserService.java                //用户管理  
    │  │  │                  │        
    │  │  │                  └─util                                 //工具类  
    │  │  │                          StringUtil.java                //字符串相关工具  
    │  │  │                            
    │  │  └─resources                                               //静态文件  
    │  │      │  application.properties                             //配置文件  
    │  │      │    
    │  │      └─templates                                           //静态页面  
    │  │              login.html                                    //登录页面  
    │  │              post.html                                     //表单管理  
    │  │              test.html                                     //测试页面  
    │  │                
    │  └─test  
    │      └─java  
    │          └─edu  
    │              └─bjtu  
    │                  └─ee4j  
    │                      └─gym  
    │                              GymApplicationTests.java  
    │                                
    └─target                                                        //maven生成  
        ├─classes  
        │  │  application.properties                                //配置文件  
        │  │    
        │  └─templates  
        │          login.html                                       //登录网页  
        │          post.html                                        //表单管理  
        │          test.html                                        //测试页面  
        │            
        └─test-classes                                                
 [toc]     
##小组人员

|姓名|学号|
|---|---|
|迟成|16301001|
|潘雅欣|16301014|
|沈晓宇|16301017|