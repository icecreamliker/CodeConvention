Code Convention
==============

United JavaScript编码指南 *[UnitedStack JavaScript Style Guide]*

## 编码

统一使用utf-8

## JavaScript语言规范

**变量声明**

  必须使用关键字 __var__    
  如果同时声明多个变量，可按个人喜好，但务必简洁，可读性强
  
**分号**

  尽可能在每一句的结尾都加上分号
  
**嵌套函数**

  可以使用

**异常处理**

  支持使用(并且可以使用自定义异常)，特别是使用Node.js的时候，要尽量捕捉可能出现的异常

**标准特性**

  优于非标准特性的使用，如：
  ```javascript
  var a = 'abcdefg';
  a.slice(1);//优先使用
  a.substr(1);//不建议使用
  ```

**基本包装类型**

  不要 __new__ 基本包装类型（Boolean/Number/String）
  
**闭包**

  可以使用，但需要小心

**关联数组**

  不要使用 __Array__ 去做 map/hash/associative 要做的事情，如果想用哈希映射等则推荐使用 __Object__
  
**多行字符串字面量**
  
  建议不要使用 *\\* 进行字符串拼接
  ```javascript
  var a = 'abcdefg' +
      'hijklmn' +
      'opqrstuvwxyz';
  ```
  
**Array和Object字面量**
  
  尽可能不要使用new Array()和new Object()来创建数组和对象
  ```javascript
  var object = {};//创建对象
  var array = [];//创建数组
  ```
  
**修改内置对象**

  应该尽可能避免修改内置对象原型
  
**eval和with**

  不允许使用eval和with




## JavaScript代码风格规范

**命名**

通常，使用类似于 *functionNamesLikeThis*, *variableNamesLikeThis*, *ClassNamesLikeThis*, *methodNamesLikeThis*, 和 *SYMBOLIC_CONSTANTS_LIKE_THIS* 这样的命名方式（驼峰式）

> 函数和方法命名

  用类似 *functionNamesLikeThis*, *methodNamesLikeThis* 这样的形式，如：
  ```javascript
  var getName = function() {
    //...
  }
  function checkName() =  {
    //...
  }
  ```
  
> 变量命名

  用类似 *variableNamesLikeThis* 或者 *variable_name_like_this* 这样的形式，如：
  ```javascript
  var age = 24;
  var i_am_age =24;
  ```

> 类命名

  用类似 *ClassNamesLikeThis* 这样的形式，如：
  ```javascript
  function Persion() {
    //...
  };
  ```
  
> 常量命名

  用类似 *NAMES_LIKE_THIS* 这样的形式，如：
  ```javascript
  var ONE_MINUTE_COUNTS = 60;
  ```
  
> 属性和方法

  + __私有的属性__，变量和方法（在文件或类中）都应该改以下划线开头
  + __受保护的属性__，变量和方法不需要用下划线（和公开的一样）

  ```javascript
  function method() {
    var _privateName = 'xxx';
    var _privateFunction = function() {};
  }
  ```

> 模块命名

  模块命名都使用小写单词
  
> 其他

  命名需要语义化，如初始化方法可以使用init，如果是布尔判断则可以使用isSomeName等等

**缩进**

  默认缩进4个空格，如果使用tab则设置为4空格

**代码格式化**
  
> 大括号

  大括号应如下书写：
  ```javascript
  if () {
    //...
  } else {
    //...
  }
  ```

> 数组和对象初始化

  以整洁为目标，如下所示：
  ```javascript
  //数组初始化
  var arr = [1, 2, 3];
  var obj = {a: 1, b: 2, c: 3};
  //对象初始化
  var box = {
    width: 10,
    height: 20
  };
  ```
> 代码宽度
  
  为保持可读性，每行不超过80个字符
  
> 函数参数及传递匿名函数

  以简洁清楚为目标，建议缩进2或4空格：
  ```javascript
  function foo(veryDescriptiveArgumentNumberOne, veryDescriptiveArgumentTwo,
             tableModelEventHandlerProxy, artichokeDescriptorAdapterIterator) {
    // ...
  }
  
  prefix.something.reallyLongFunctionName('whatever', function(a1, a2) {
    if (a1.equals(a2)) {
      someOtherLongFunctionName(a1);
    } else {
      andNowForSomethingCompletelyDifferent(a2.parrot);
    }
  });
  ```
  
> 换行

  可以用来区分逻辑块

> 空格

  操作符之间尽可能使用空格，增强代码可读性
  
> 逗号

  如在object中使用，建议使用传统的后置逗号，不要使用前置逗号
  
> 三元操作符
  
  尽可能放在一行
  
**字符串**

  建议使用单引号 __'__ 取代 __"__
  
**注释**

  一般建议使用Backbone风格注释，即以描述功能为主，如 [Backbone代码] (https://github.com/documentcloud/backbone/blob/master/backbone.js)    
  但是，如果是涉及到接口或者API则建议使用JSDoc风格注释
  
  每个单独js文件的开始，必须标明作者，时间，最后修改时间和功能
  ```javascript
  /**************************************
   * Author      : XXX
   * Function    : XXX
   * Time        : XXX
   * Last Update : XXX
   **************************************/
  ```
  
##参考及致谢
* [Google JavaScript Style Guide] (http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=var)
* [Dojo Style Guide] (http://dojotoolkit.org/community/styleGuide)
* [Arale编码规范] (http://www.aralejs.org/docs/rules.html)



