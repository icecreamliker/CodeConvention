Code Convention
==============

UnitedStack JavaScript编码指南第二版 *[UnitedStack JavaScript Code Style Guide]*

## 编码

统一使用utf-8

## JavaScript语言规范


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

  使用 *variableNamesLikeThis* 这样驼峰命名形式，如：
  ```javascript
  var age = 24;
  var isChecked = false;
  ```

> 类命名

  用类似 *ClassNamesLikeThis* 这样的形式，如：
  ```javascript
  function Persion() {
    //...
  };
  class Person {
    constructor() {
      //...
    }
  }
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

  默认缩进2个空格，如果使用tab则设置为2空格(根据个人习惯和团队风格，可以设置为4个空格)

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
> JSON对象

 对于JSON对象，如在JS文件中定义，则使用单引号`'`或不使用，但在一个文件中中需要保证格式统一，如：
  ```javascript
  var obj = {
    key: 1,
    name: 2
  }
  ```
  但在JSON文件中，则需要使用`"`包括key值，如：
  ```javascript
  {
    "KEY": "VALUE"
  }
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
  头注释并不是强制使用，一切为了可维护而生
  
**单文件大小**

  每个单独文件的代码行数（LOC, Line of Code）需控制在200以内；特殊情况下，可控制在300行内或更多（但不建议）
  
## JavaScript ES6使用规范

**变量定义**

  块作用域下，使用`let`替代`var`，例如：
  ```javascript
  for (let i = 0; i < 10; i++) {
    //...
  }
  ```
  对于常量，使用`const`来定义
  对于模版，应如下使用，以保证代码高可读性：
  ```javascript
  var tmpl = `
    <div>
     <span></span>
    </div>`;
  ```
  任何类的定义都使用`class`，并且使用`extends`来实现继承

  import或者export模块时，尽量优先使用ES6标准方法
 

##参考及致谢
* [Google JavaScript Style Guide] (http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=var)
* [Dojo Style Guide] (http://dojotoolkit.org/community/styleGuide)
* [Arale编码规范] (http://www.aralejs.org/docs/rules.html)
* [广发证券编码规范] (https://github.com/gf-rd/es6-coding-style/blob/master/README.md)


