# jQuery.js-2-

<!doctype html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>jQuery元素选择器讲解</title>
</head>
<body>
<style>
    *{
        font-size:30px;

    }
</style>

    <div class="container">
        <div class="header">
            <div class="nav">
            </div>
            <div class="banner">
            </div>
        </div>
    </div>
    <div class="content">
        <ul>
            <li class="li-item">item1</li>
            <li class="li-item">item2</li>
            <li class="li-item">item3</li>
            <li class="li-item">item4</li>
            <li class="li-item">item5</li>
            <li>item-6</li>
            <li data-val="7">item-7</li>
            <li>item-8</li>
        </ul>
            <div class="content-left">
            </div>
            <div class="content-right">
            </div>
    </div>
    <div class="footer">

    </div>



    <div class="li-item">div-1</div>
    <div class="li-item">div-1</div>
    <div class="li-item">div-1</div>
    <div class="li-item">div-1</div>
    <div class="li-item">div-1</div>
    <script src="http://cdn.bootcss.com/jquery/3.0.0/jquery.min.js"></script>
    <script src="js/query.js"></script>
</body>

</html>

```javascript
  $('#id')//根据id选择一个标签.$=jQuery
  $('.class')//根据class的值选择多个元素
  document.getElementById()  //('ID')方法类似
  
  $('.class')//根据class的值选择多个元素
  $('span')//通过标签名
  $('div span') //选择 id为div的元素内的span标签
  $('#div span')//选择id为div的元素内的span标签
  $('li.li-item')//选择所有class = 'li-item'的li标签
   //选中的元素可以通过each进行遍历,获取每一个值
   //可以通过.text()获取或者设置元素的文本内容
   //可以通过.html()获取或者设置元素的html内容
   //可以通过.css()设置样式,两个参数(参数1:样式,参数2:样式值)
   
   //页面中的html元素全部加载完成后执行此种方法
   //同一个页面中可以包含很多这个方法
   $(function(){
   //console.log($('.li-item').length);
   
   
   //遍历选中的Li节点
   //选择页面中所有class='li-item'元素 不管元素的类型
   console.log($('.li-item').length);
   
   //选择页面中所有的class='li-item'.的div元素
   console.log($('div.li-item'.length));
   
   //选择页面中所有的class='li-item'的li元素
   console.log($('ul li.li-item').length);
   
   //选择ul中的所有Li元素
   console.log($(ul li).length);
   
   //父级空格子级
   //子级后面跟着一个.class是选择子级后面的class元素
   
   $('.li-item').each(function(index){})
     //console.log(index);
        //$(this).text();//获取当前元素的text值
        //$(this).text('当前值为1');修改当前的元素text值为1

        ///text标签文本元素,html表示内部的html内容
        //console.log('当前标签的text'+$(this).text('当前的li内容为:'+(index+1)+));
        //console.log('当前标签的html'+$(this).html('<a href="http:www.baidu.com">当前的li内容为:'+(index+1)+"</a>"));
   });
   //通过标签名 选择标签元素
   //$('ul').html()//输出ul节点内部的所有html内容
   //($('ul').text());//输出ul节点内部的所有文本标签
   //console.lig($('ul').text());
   //选择ul中所有的class='li-item'的li元素
    //$('ul .li-item')////1
    //$('li.li-item')////2

    //选择ul中所有的没有class的li元素
    //$("ul li[class!='li-item']")

    //选择ul中所有的包含data-val的li元素
    //$("ul li[data-val]")

    //根据表单的name值来选择元素
    //$("input[name='']")

    //选择li中所有class='li-item'设置颜色为红色
    $('ul li.li-item').css("color","yellow");
    //为.content元素这是背景颜色
    $('.content').css("background-color","red");
```
