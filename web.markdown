ServletContext：web application的上下文对象

（1）通过对该对象获取web application

上下文路径：getContextPath()

web工程名称配置tomcat—>contextpath—>/当前web工程名

（2）全局管理者对象：在web.xml配置一些全局参数

全局参数的配置\<context>

​	参数和参数对应值

\<context>

（3）作为域对象：在多个servlet之间可以共享数据，保存数据，获取数据

request：

servletContext：最大的域对象

  setAttribut("名称",普通String/Object/集合数据):给域中保存数据

  getAttribute("名称")—>string/Object/遍历集合数据

.......

(4)页面跳转























会话技术：在浏览器中访问网站所产生的数据（上次登陆时间，账户密码，验证码等）

Cookie技术：在浏览器端进行保存

特点：(1)不适合敏感数据（用户登录密码等）

(2)浏览器端存储的cookie数据有限，一个站点的cookie数量（200~300个）

(3)通过服务器将cookie数据携带进数据

基本使用：Cookie的是由服务器端创建出来的

Cookie(String name,String value)：携带cookie的名称和cookie的值，浏览器端请求某个servlet的时候，将cookie的数据记录下来需要通过服务器携带回去

public void addCookie(Cookie cookie) //将指定cookie添加到响应，可多次调用此方法设置一个以上的cookie

response.addCookie("name"); //首先判断浏览器中有无cookie

public Cookie[] getCookie() //浏览器获取Cookie数据，返回包含客户端随此请求一起发送的所有Cookie对象的数组，如果没有发送任何cookie，则此方法返回null，return此请求中包含的cookie数组，如果该请求没有cookie，返回null

常用的方法：(1)String getName()：获取cookie名称

(2)String getValue()：获取cookie值

(3)Cookie内容的过期时间：默认是浏览器关闭的时候cookie就完了

setMaxAge(int time)：设置cookie的过期时间 

setPath(web application的上下文路径 + "/");

Servlet请求映射/a/b/hello      cookie路径path：以"/"项目名称开始，以"/"结束

Cookie不能跨浏览器，也不能存储中文（）









Session技术：在服务器端保存

特点：()

()

()