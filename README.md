# -关于小程序学习里的一些比较杂的知识点

<h2>模板</h2>
  在多个页面中都能用到的内容  可以新建一个文件夹新建wxml文件来写。然后在需要用到的页面WXML文件中引入  可用include（全部代码copy过来的方法）也可以用import。注意格式<include src="../templates/header"/>或者<import src="../templates/footer"/>  最后是要再加一个 / 的，  不然会报错。 </br>
  在模板wxml文件里用了<template>标签的话 在引入时一定要写<template is=""/>引号里写标签的name值。
  
<h2>相对定位和绝对定位</h2> 

相对定位是以自身原来的位置作参考再在top/bottom/left/right方向作移动，且原来的位置还被占用
绝对定位是以已定位的最近的父级容器作参考，没有原来的位置了

<h2>图片设置</h2>
在插入图片时 可以在WXSS中通过设置父级样式类名加空格加image （例如 .content image,其中content可以是上一级<view>的）height 100%和width 100%来保证图片的完整展示，但还是有可能会有拉伸

<h2>API调用返回参数</h2>
有些返回值不是标准的JSON格式  可以用JSON.parse(res)来标准化 如 console.log(JSON.parse(res.result).errcode);

<h2>数据库数据读取后的展示</h2>
  在JS文件中先定义一个数组 然后setData,再wxml中用<block wx:for"{{数组}}"> 内容</block>来在内容中展示获取的数据
