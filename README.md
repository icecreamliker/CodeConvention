Code Convention
==============

United JavaScript编码指南 *[UnitedStack JavaScript Style Guide]*

## JavaScript语言规范

### 编码
统一使用utf-8

### 命名规范

**变量声明**

  必须使用关键字var
  
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

  不要new基本包装类型（Boolean/Number/String）
  
**闭包**

  可以使用，但需要小心

**关联数组**

  不要使用Array去做 map/hash/associative 要做的事情，如果想用哈希映射等则推荐使用Object
  
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
  var _object = {};//创建对象
  var _array = [];//创建数组
  ```
  
**修改内置对象**

  应该尽可能避免修改内置对象原型
  






## JavaScript代码风格规范

**常量命名**

  用类似NAMES_LIKE_THIS这样的形式，如：
  ```javascript
  var ONE_MINUTE_COUNTS = 60;
  ```
    

##参考及致谢
* [Google JavaScript Style Guide] (http://google-styleguide.googlecode.com/svn/trunk/javascriptguide.xml?showone=var)
* [Dojo Style Guide] (http://dojotoolkit.org/community/styleGuide)
* [Arale编码规范] (http://www.aralejs.org/docs/rules.html)



