## js工具
常用js工具类函数整理
### class相关
* hasClass：判断元素是否有某个class

```
/**
* hasClass
* @desc 判断元素是否有某个class
* @param {HTMLElement} ele
* @param {String} cls
* @return {Boolean}
*/
function hasClass (ele, cls) {
		return (new RegExp('(\\s|^)' + cls + '(\\s|$)')).test(ele.className);
}
```
* addClass：为元素添加class

```
/**
* addClass
* @desc   为元素添加class
* @param  {HTMLElement} ele
* @param  {String} cls
*/
function addClass (ele, cls) {
		if (!this.hasClass(ele, cls)) {
    			ele.className += ' ' + cls;
    }
}
```
* removeClass：为元素移除class

```
{
/**
* removeClass
* @desc 为元素移除class
* @param {HTMLElement} ele
* @param {String} cls
*/
function removeClass(ele, cls) {
  if (this.hasClass(ele, cls)) {
    var reg = new RegExp('(\\s|^)' + cls + '(\\s|$)');
    ele.className = ele.className.replace(reg, ' ');
  }
}
```

