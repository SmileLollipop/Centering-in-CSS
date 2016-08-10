# Centering-in-CSS
css 实现居中
```html
<!-- 1.如何居中一个浮动元素 -->

<!-- 父元素和子元素同时左浮动，然后父元素相对左移动50%，再然后子元素相对右移动50%，或者子元素相对左移动-50%也就可以了。 -->


<style type="text/css">
    .p{
        position:relative;
        left:50%;
        float:left;
    }
    .c{
        position:relative;
        float:left;
        right:50%;
    }
</style>


<div class="p">

    <h1 class="c">Test Float Element Center</h1>

</div>



<!-- 2.css实现水平垂直居中 -->

<style type="text/css">
    .align-center{
        /**
         * 负边距+定位：水平垂直居中（Negative Margin）
         * 使用绝对定位将content的定点定位到body的中心，然后使用负margin（content宽高的一半），
         * 将content的中心拉回到body的中心，已到达水平垂直居中的效果。
         */
        position:absolute;
        left:50%;
        top:50%;
        width:400px;
        height:400px;
        margin-top:-200px;
        margin-left:-200px;
        border:1px dashed #333;
    }
</style>

<!-- 2.css实现水居中 -->
<!--传统的水平居中样式 margin: 0 auto; 这个方法要求使用这个样式的dom元素,必须同时定义宽度width. 如果dom元素内容是不固定的,那么就无法定义宽度.所以这个地方就很难弄.-->
<style type="text/css">
.SecondMenuBody{
    display: table; /*重点就是这个属性,这个样式会告知浏览器当前元素的宽度,采用最小的宽度.不是默认全宽*/
    margin: 0 auto; 
}
    
</style>

<div id="parent" >
   <div class="SecondMenuBody">这里的内容永远相对父元素水平居中</div>
</div>


```
