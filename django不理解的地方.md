# django不理解的地方

#### 1.url到底是如何匹配的，匹配后传入views中函数的request又是什么；

​		-接受request后，输入的网址即url按列表<u>顺序</u>（urlpatterns）<u>字符串或正则表达式</u>匹配，django.urls.path()的第一个参数。之后访问views函数，返回render（渲染）或HttpResponse的资源

​		-django.urls.path(route, view, kwargs=, name= )各个参数:

​				**route**: string or regax; 若包含尖括号，会将请求中captured变量传入views函数

​							route格式为(r'^xxx/<int:px>$')

​				**view**：视图函数，会以request作为第一个参数；captured变量作为关键字参数

​				**name**：命名URL，类似宏，防止硬编码



2.migration是什么，为什么要把模型迁移到<u>数据库</u>；







3.views中render()以及httpResponse()等函数的参数；







4.字段概念，外键，主键，以及创建模型的各api的参数？







5.单元测试的方法，与reverse()







6.HTML模板的用法(extends(继承) and include(引入))

​	1.定义一个模板HTML文件，在非共用部分用block标签标注(name不能重复)

```html
{% block name %}

{% endblock name %}
```

​	2.在子html文件开头加入{% extends "templates.html "%}

```html
{% extends "templates.html "%}
{% block name %}
	{{ block.super }}  <!--继承模板的共用部分-->
	<!-- 重写独有部分-->
{% endblock name %}
```



and



​	1.在template文件夹中新建一个include文件夹，新建form.html文件，写入模板表单

​	2.在要引用的地方写{% include ‘include/form.html’ %}

​	



7.{% csrf_token %}如何防止csrf攻击，以及csrf攻击是什么；（xss攻击/ddos攻击/sql注入/……）



8.熟悉Bootstrap4的api，class



9.it is impossible to add a non-nullable field



10.UNIQUE constraint failed

​	解决方式：python namage.py flush(慎用)

-

11.Django的forms表单类
