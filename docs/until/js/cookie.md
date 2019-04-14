## js工具
常用js工具类函数整理
### cookie相关
* getCookie：根据name读取cookie

```
/**
* getCookie
* @desc 根据name读取cookie
* @param  {String} name
* @return {String}
*/
function getCookie(name) {
  var arr = document.cookie.replace(/\s/g, "").split(';');
  for (var i = 0; i < arr.length; i++) {
    var tempArr = arr[i].split('=');
    if (tempArr[0] == name) {
      return decodeURIComponent(tempArr[1]);
    }
  }
  return '';
}
```
* setCookie：设置Cookie

```
/**
 * setCookie
 * @desc  设置Cookie
 * @param {String} name
 * @param {String} value
 * @param {Number} days
 */
function setCookie(name, value, days) {
  var date = new Date();
  date.setDate(date.getDate() + days);
  document.cookie = name + '=' + value + ';expires=' + date;
}
```
* removeCookie：根据name删除cookie

```
/**
 * removeCookie
 * @desc 根据name删除cookie
 * @param  {String} name
 */
function removeCookie(name) {
  // 设置已过期，系统会立刻删除cookie
  this.setCookie(name, '1', -1);
}
```
