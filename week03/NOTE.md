# 学习总结

## JavaScript 里有哪些对象是我们无法实现

- 答：javascript中的**原生对象**是无法用纯javascript代码实现的，如下：

基本类型 | 基本功能和数据结 | 错误类型 | 二进制操作 | 带类型的数组
--      | --       | --             | --                | --
Boolean | Array    | Error          | ArrayBuffer       | Float32Array
String  | Date     | EvalError      | sharedArrayBuffer | Float64Array
Number  | RegExp   | RangeError     | DataView          | Int8Array
Symbol  | Promise  | ReferenceError |                   | Int16Array
Object  | Proxy    | SyntaxError    |                   | Int32Array
|       | Map      | TypeError      |                   | Unit8Array
|       | WeakMap  | URIError       |                   | Unit16Array
|       | Set      |                |                   | Unit32Array
|       | WeakSet  |                |                   | Unit8ClampedArrray
|       | Function |                |                   | 


### 对象包括内置对象、宿主对象

##### 宿主对象
- 由宿主环境提供的对象，比如浏览器环境中window、document

##### 内置对象：固有对象、原生对象
- 固有对象：由标准规定，在javacript运行时创建的对象实例，150+
- 原生对象：通过javascript语言本身的构造器创建的对象，被称为原生对象。例如Date、RegExp等，可以通过new运算符创建，但是无法用纯JavaScript实现
