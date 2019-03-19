# -关于小程序学习里的一些比较杂的知识点

<h1>模板<h1>：在多个页面中都能用到的内容  可以新建一个文件夹新建wxml文件来写。然后在需要用到的页面WXML文件中引入  可用include（全部代码copy过来的方法）也可以用import。注意格式<include src="../templates/header"/>或者<import src="../templates/footer"/>  最后是要再加一个 / 的，  不然会报错。 

