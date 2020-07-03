启动参数 VM options:
-
* -Duser.region=US
* -Dfile.encoding=UTF-8
* -Dcatalina.home=/Users/mc/Documents/workspace/tomcat9/apache-tomcat-9.0.36-src/home
* -Dcatalina.base=/Users/mc/Documents/workspace/tomcat9/apache-tomcat-9.0.36-src/home
* -Djava.util.logging.manager=org.apache.juli.ClassLoaderLogManager
* -Djava.util.logging.config.file=/Users/mc/Documents/workspace/tomcat9/apache-tomcat-9.0.36-src/home/conf/logging.properties


JDTCompiler中CompilerOptions.VERSION_9等常量找不到(项目中已修改)
-
```
} else if(opt.equals("9") || opt.equals("1.9")) {
    settings.put(CompilerOptions.OPTION_Source,
                 CompilerOptions.VERSION_9);
} else if(opt.equals("10")) {
    settings.put(CompilerOptions.OPTION_Source,
                 CompilerOptions.VERSION_10);
} else if(opt.equals("11")) {
    settings.put(CompilerOptions.OPTION_Source,
                 CompilerOptions.VERSION_11);
} else if(opt.equals("12")) {
    settings.put(CompilerOptions.OPTION_Source,
                 CompilerOptions.VERSION_12);
```                       
直接注释代码块即可
      

访问localhost:8080报错解决方案：(项目中已修改)
-

```
ContextConfig类的configureStart()方法中的webConfig();后添加如下代码：

context.addServletContainerInitializer(new JasperInitializer(), null);
```
