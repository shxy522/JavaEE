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
> .gitattributes  
> .gitignore  
> gym   
>> .gitignore  
>> mvnw  
>> mvnw.cmd  
>> pom.xml &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//maven管理文件  
>> README.md &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//文档      
>> .mvn  
>>> wrapper  
>>>> maven-wrapper.jar  
>>>> maven-wrapper.properties  
>>>> MavenWrapperDownloader.java   
>>  
>> src  
>>> main  
>>>> java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//代码  
>>>>> edu  
>>>>>> bjtu  
>>>>>>> ee4j  
>>>>>>>> gym  
>>>>>>>>> GymApplication.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//程序入口  
>>>>>>>>> config  
>>>>>>>>>> SecurityConfig.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//security权限管理：拦截未认证请求+密码加密    
>>>>>>>>>
>>>>>>>>> controller &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//页面访问控制  
>>>>>>>>>> AuthController.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//登录注册  
>>>>>>>>>> PageController.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//测试文件  
>>>>>>>>>> PostController.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//表单管理：实现spring cache连接windows redis对请求结果进行缓存  
>>>>>>>>>
>>>>>>>>> exception &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//异常处理  
>>>>>>>>>> PostExceptionHandler.java  
>>>>>>>>>> PostNotFoundException.java   
>>>>>>>>>
>>>>>>>>> model &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//实体类  
>>>>>>>>>> Post.java  
>>>>>>>>>> PostShares.java  
>>>>>>>>>> User.java  
>>>>>>>>>> UserAuth.java  
>>>>>>>>>
>>>>>>>>> repository &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//数据访问接口  
>>>>>>>>>> AuthRepository.java  
>>>>>>>>>> PostRepository.java  
>>>>>>>>>> UserRepository.java   
>>>>>>>>>
>>>>>>>>> service &emsp;&emsp;&emsp;&emsp;&emsp;//数据服务  
>>>>>>>>>> AuthService.java &emsp;&emsp;&emsp;//权限管理  
>>>>>>>>>> PostService.java &emsp;&emsp;&emsp;//表单管理  
>>>>>>>>>> UserDetailsServiceImpl.java &emsp;//用户详细管理  
>>>>>>>>>> UserService.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//用户管理    
>>>>>>>>>
>>>>>>>>> util &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//工具类  
>>>>>>>>>> StringUtil.java &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//字符串相关工具  
>>>> 
>>>> resources &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//静态文件  
>>>>> application.properties &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//配置文件   
>>>>> templates &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//静态页面  
>>>>>> login.html &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//登录页面  
>>>>>> post.html &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//表单管理  
>>>>>> test.html &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//测试页面    
>>> 
>>> test  
>>>> java  
>>>>> edu  
>>>>>> bjtu  
>>>>>>> ee4j  
>>>>>>>> gym  
>>>>>>>>> GymApplicationTests.java   
>>
>> target &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;//maven生成  
>>> classes  
>>>> application.properties    
>>>> templates  
>>>>> login.html  
>>>>> post.html  
>>>>> test.html    
>>>
>>> test-classes       
***                                           
##小组人员

|姓名|学号|
|---|---|
|迟成|16301001|
|潘雅欣|16301014|
|沈晓宇|16301017|