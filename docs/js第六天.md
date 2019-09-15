# 我的笔记

## js基础第六天：

#  内置对象

*对象：属性和方法的集合体;**知道如何使用就可以**

*内置：js语法封装好了一些对象，里面有很多使用也经常用的属性和方法；

## Math

- ### Math.random()：生成一个[0-1]之间随机浮点数;

````js
<script>
    //先定义一个变量
    
    while (true) {
    var a = Math.random();
        alert(a);
    }
    //这里我设置了无限循环，和一个可以显示a所代表的随机小数提示框
</script>
````

- Marh.floor(x)：把一个浮点进行向下取整

  ````js
  <script>
      var a = Math.floor(3.1415926);
      //设置变量a的变量值为向下取整
      console.log(a);
      var b = Math.random();
      //b取-的随机小数
      b = b*9;
      //b的值*9，现在取值范围从0-1扩大到了0-9
      //也可以简洁的写var b = Math.random()*9;
      var b = Math.floor(b);
      console.log(b);
      // console.log(Math.floor(Math.random()*20));
      //取一个0-1的随机浮点数，让他*20;让他的值随机向下取整，并打印在控制台上。这种写法过于简洁，不能推荐
  </script>
  ````

  - 案例：刷新页面，页面改变颜色

    ````js
    <script>
    //思路：颜色的rgb表示法，是由三组0-255之间的数组合而成。要实刷新页面随机改变颜色，说白了就是通过rgb改成随机数，从而改变颜色
    //定义一个函数，方便调用
    function color() {
        return Math.floor(Math.random() * (255 + 1));
        //定义一个函数，返回值是0-255之间的随机整数;因为不需要设置实参参与函数体里面的运算，只需要把函数体里面的值返回给外面就好了;因为下标的排列时从0开始的，所以要255+1;
    }
    function blackcolor() {
        var r = color();
        var g = color();
        var b = color();
        var bgc = 'rgb(' + r + ',' +  g + ',' + b + ')';
        return bgc;
        //设置一个rgb的随机数函数,里面的r，g，b都使用上面的函数做让他成为0-255的随机数;然后设置一个变量来把rgb给组合起来，把这个函数的返回值设置成组合起来的rgb那个变量，也就是bgc。
    }
    console.log(blackcolor());
        
        for (var a = 0; a <=72; a++) {
            document.write(`<div style="background:${blackcolor()}"></div>`);
            //把设置的div样式输出到页面中
            //循环多次
            
        }
    </script>
    ````

  - Math.round(x)：把一个浮点数进行四舍五入取整

    ````js
    <script>
        console.log(Math.round(7.86)); //输出值：8
        console.log(Math.round(5.24));//输出值；5
        var a = Math.random() * 100;
        console.log(Math.round(a));
        //a定义成一个0-100随机小数的变量，然后打印四舍五入的a
    </script>
    ````

  - Math.ceil(x)：把一个浮点数进行向上取整

    ````js
    <script>
        console.log(Math.ceil(4.12));//取值结果为：5;不管小数后面是多少，都会上升1
        var a = Math.random() * 30;
        console.log(Math.ceil(a));
        //设置a为0-30的随机小数，打印a向上取整
    </script>
    ````

    









