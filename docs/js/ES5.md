## ES5
* `use strict`
  * 严格模式
* `Array`
  * `isArray`
  * `every`
  * `some`
  * `forEach`
  * `filter`
  * `indexOf`
  * `lastIndexOf`
  * `map`
  * `reduce`
  * `reduceRight`
* `Object`
  * `Object.create(proto, [ propertiesObject ])`
    * 新建对象
    * `propertiesObject`
      * `value` : 设置属性的值
      * `writable` : 布尔值,设置属性是否可以被重写,默认属性值为false(不能被重写)
      * `enumerable` : 布尔值,设置属性是否可以被枚举,默认属性值为false(不能被枚举)
      * `configurable` : 布尔值,设置属性是否可以被删除，默认属性值为false(不能被删除)
  * `Object.defineProperty(obj)` \ `Object.defineProperties(8bj)`
    * 设置属性\设置多个属性
  * `Object.getPrototypeOf()`
  * `Object.getOwnPropertyDescriptor()`
  * `Object.preventExtensions()`
  * `Object.isExtensible()`
  * 遍历属性
    * `Object.keys()`
    * `Object.getOwnPropertyNames()`
  * 冻结对象
    * `Object.seal()` \ `Object.isSealed()`
    * `Object.freeze()` \ `Object.isFrozen()`
    
