#  php


---

##  1.PHP 脚本以 <?php 开头，以 ?> 结尾：

```php
<?php
// 此处是 PHP 代码
?>>
```


##  2.一个简单的 PHP 文件，其中包含了使用内建 PHP 函数 "echo" 在网页上输出文本 "Hello World!" 的一段 PHP 脚本：

```php
<!DOCTYPE html>
<html>
<body>

<h1>我的第一张 PHP 页面</h1>h1>

<?php
echo "Hello World!";
?>

</body>body>
</html>html>
```

##  3.php的三种注释：

```php
<!DOCTYPE html>
<html>
<body>

<?php
// 这是单行注释

# 这也是单行注释

/*
这是多行注释块
它横跨了
多行
*/
?>
 
</body>body>
</html>html>

```

##  4.PHP 大小写敏感:

*   在 PHP 中，所有用户定义的函数、类和关键词（例如 if、else、echo 等等）都对大小写不敏感。
*   不过在 PHP 中，所有变量都对大小写敏感。

##  5.PHP变量
*   PHP 没有创建变量的命令。
*   变量会在首次为其赋值时被创建
    
```php
<?php
$x=5;
$y=6;
$z=$x+$y;
echo $z;
?>>

```

##  6.变量规则：
*   变量以 $ 符号开头，其后是变量的名称
*   变量名称必须以字母或下划线开头
*   变量名称不能以数字开头
*   变量名称只能包含字母数字字符和下划线（A-z、0-9 以及 _）
*   变量名称对大小写敏感（$y 与 $Y 是两个不同的变量）


##  7.变量作用域：

在PHP 中，可以在脚本的任意位置对变量进行声明。

变量的作用域指的是变量能够被引用/使用的那部分脚本。

PHP 有三种不同的变量作用域：
*   local（局部）
*   global（全局）
*   static（静态）

Local 和 Global 作用域
函数之外声明的变量拥有 Global 作用域，只能在函数以外进行访问。
函数内部声明的变量拥有 LOCAL 作用域，只能在函数内部进行访问。

##  8.global 关键字
global 关键词用于访问函数内的全局变量。
要做到这一点，请在（函数内部）变量前面使用 global 关键词：

```php
<?php
$x=5;
$y=10;

function myTest() {
  global $x,$y;
    $y=$x+$y;
    }
    
    myTest();
    echo $y; // 输出 15
    ?>
```
 
PHP 同时在名为 $GLOBALS[index] 的数组中存储了所有的全局变量。下标存有变量名。这个数组在函数内也可以访问，并能够用于直接更新全局变量。

上面的例子可以这样重写：

```php
<?php
$x=5;
$y=10;

function myTest() {
  $GLOBALS['y']=$GLOBALS['x']+$GLOBALS['y'];
  } 
  
  myTest();
  echo $y; // 输出 15
  ?>
```

##  9.PHP static 关键词
通常，当函数完成/执行后，会删除所有变量。不过，有时我需要不删除某个局部变量。实现这一点需要更进一步的工作。
要完成这一点，请在您首次声明变量时使用 static 关键词：

```php
<?php

function myTest() {
  static $x=0;
    echo $x;
      $x++;
      }
      
      myTest();
      myTest();
      myTest();
      
      ?>
```


##  10.数据类型:
字符串、整数、浮点数、逻辑、数组、对象、NULL。

数组：
```php
<?php 
$cars=array("Volvo","BMW","SAAB");
var_dump($cars);
?>
```

对象：对象是存储数据和有关如何处理数据的信息的数据类型。

*   在 PHP 中，必须明确地声明对象。
*   首先我们必须声明对象的类。对此，我们使用 class 关键词。类是包含属性和方法的结构。
*   然后我们在对象类中定义数据类型，然后在该类的实例中使用此数据类型

```php
<?php
class Car
{
  var $color;
    function Car($color="green") {
        $this->color = $color;
    }
    function what_color() {
      return $this->color;
    }
}
?>
```
