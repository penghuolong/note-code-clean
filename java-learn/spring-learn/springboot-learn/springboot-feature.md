# spring boot 特性
## 自动配置
1. 原理   
     基于添加的JAR依赖自动对spring boot 应用进行配置（主要是 spring-boot-autoconfiguration），此jar包里面会取得spring.factories 文件里面的自动配置类名称，然后加载相应的自动配置类。主要实现是通过各种各样的 @Contional 注解   
     命令行 --debug 可以查看自动配置结果  

2. 简单使用 
    @EnableAutoConfiguration(exclude = Class<?>[])
    @SpringBootApplication（） 包含有开启自动配置注解  
3. 自定义自动配置  
    * 使用 @Configuration 注解定义一个配置类
    * 使用 @Conditional 相应注解给自动配置添加配置条件        
    * 定位自动配置 在 META-INF/spring.fatories 声明自动配置类
4.  @Conditional 相关注解  
    * Bean条件   
    @ConditionalOnBean
    @ConditionalOnMissingBean
    @ConditionOnsingleCandidate

    * 资源条件
    @ConditionalOnResource
    
    * web应用注解
    @ConditionalOnWebApplication

    * 其他条件
    @ConditonalOnExpression
5.  自动配置执行顺序相关注解
    * @AutoConfigureBefore
    * @AutoConfigureAfter
    * @AutoConfigureOrder  
6.  在低版本spring3.x实现自动配置
    可能遇到问题：
    1. 3.x版本没有条件注解 
       使用 BeanFactoryPostProcessor 进行条件判断
    2. 无法自动定义需要加载的自动配置
       编写Java config 类， 然后通过 component-scan 或者 XML文件import
## starter 简化项目配置
## 内嵌服务器
## 生产级监控
## 命令行界面