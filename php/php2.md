#   PHP

---


##  1.字符串函数

*   strlen()

```php
<?php
echo strlen("Hello world!");
?>
```
*  strpos() 用于检索字符串内指定的字符或文本。

```php
<?php
echo strpos("Hello world!","world");
?>
```

##  2.常量

常量是单个值的标识符（名称）。在脚本中无法改变该值。
有效的常量名以字符或下划线开头（常量名称前面没有 $ 符号）。
注释：与变量不同，常量贯穿整个脚本是自动全局的。

```php
<?php
define("GREETING", "Welcome to W3School.com.cn!");
echo GREETING;
?>
```

##  3.超全局

*   $GLOBALS — 引用全局作用域中可用的全部变量

```php
<?php 
$x = 75; 
$y = 25;
 
function addition() { 
  $GLOBALS['z'] = $GLOBALS['x'] + $GLOBALS['y']; 
  }
   
  addition(); 
  echo $z; 
  ?>
```

*    $_SERVER:$_SERVER 这种超全局变量保存关于报头、路径和脚本位置的信息。

```php
<?php 
echo $_SERVER['PHP_SELF'];
echo "<br>";
echo $_SERVER['SERVER_NAME'];
echo "<br>";
echo $_SERVER['HTTP_HOST'];
echo "<br>";
echo $_SERVER['HTTP_REFERER'];
echo "<br>";
echo $_SERVER['HTTP_USER_AGENT'];
echo "<br>";
echo $_SERVER['SCRIPT_NAME'];
?>
```

*   $_REQUEST 用于收集 HTML 表单提交的数据。
*   $_POST 广泛用于收集提交 method="post" 的 HTML 表单后的表单数据。$_POST 也常用于传递变量。
*   $_GET 也可用于收集提交 HTML 表单 (method="get") 之后的表单数据。
*
