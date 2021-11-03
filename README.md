<h1 align="center">H5 PDF Preview</h1>

#### 使用 方法

服务器静态页面
| 参数 | 值 |
| :-------: | :--------------------: |
| url | pdf 的地址 |
| height | 底部预留高度 |
| title | 页面标题 |

**url** 如果有参数，
**title** 如果是中文，

请在传递的时候一定要用 **encodeURIComponent** 编码。

#### URL 传参

- encodeURIComponent 传入编码
- decodeURIComponent 接收解码

#### 获取参数

```js
function getQueryVariable(variable) {
  var query = window.location.search.substring(1);
  var vars = query.split("&");
  for (var i = 0; i < vars.length; i++) {
    var pair = vars[i].split("=");
    if (pair[0] == variable) {
      return pair[1];
    }
  }
  return false;
}
```

#### 使用范畴

小程序 **WebView** 嵌套页面
