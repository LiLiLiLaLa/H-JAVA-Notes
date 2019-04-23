JSP：java server page：可以书写Java的HTML页面

一般情况：jsp，servlet担当自己的角色

JSP—>展示数据的（view：视图层）

​		能写Java代码，实际开发中，后台Java代码和JSP的数据完全分离

Servlet—>处理后台的

​		调用service层（Model：业务逻辑层）—>service业务接口—>service业务层—>service层又要调用dao层（接口）（数据库访问层）—>dao层的具体实现—>Controller层（控制器）

​		使用service相关的东西

​		和前端进行交互



JSP其实就是一个servlet，

—>（1）书写jsp文件—>tomcat服务器进行翻译—>XXX.java文件

（2）XXX.java文件中，会调用相关jsp的服务方法

​	JSP中java代码的输出/成员变量的定义/jsp输出调用

（3）由JVM将java编译成XXX.class文件

（4）由反射机制完成构造调用，成员方法调用.....



JSP脚本格式：

​	Java片段：可以书写java代码<%   %>

​		<%=%>		<%!%>



JSP将内容数据（从后台传递的数据）和当前页面的信息分离

——————————————————————————————————————————————————

JSP的三大指令：

重点指令:<%@page/include/taglib %>

Page：规定当前jsp里面相关的属性：是否启动自动刷新/是否启用重要属性

​	（1）

​	（2）

​	（3）221538914924  

​	（1）和（2）哪一个起作用：如果同时出来，一般都以pageEncoding为主准，（1）和（2）不管哪个出现，都是默认的以当前某一个格式进行编码

Include

Taglib: