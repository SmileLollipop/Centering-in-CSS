# Centering-in-CSS
css 实现居中

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
