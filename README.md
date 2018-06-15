
#
# WKWebview
#

# JS <-> APP 互相交握
最近因為在試如何能讓JS <-> APP 互相交握 , 所以需要如何判斷網頁是開在 iOS 的WKWebview 中。<br>
下面的程式是在網路上找到的，記錄一下，怕會忘記。<br>
```javascipt
var iOS = (navigator.userAgent.match(/(iPad|iPhone|iPod)/g) ? true : false);
var isWKWebView = false;
if (window.webkit && window.webkit.messageHandlers) {
    isWKWebView = true;
}
```
參考網址：https://stackoverflow.com/questions/28795476/detect-if-page-is-loaded-inside-wkwebview-in-javascript


#
# 如何在Javascript 新增 script 到html 去
#

## 只加上　Code 
```javascipt
    var script = document.createElement("script");
    script.type="text/javascript";
    script.innerHTML="window.dataLayer = window.dataLayer || [];";
    document.getElementsByTagName('head')[0].appendChild(script);
```
## 只加上 js file link 
```javascipt
    var script = document.createElement("script");
    script.type="text/javascript";
    script.src="xxxx.js";
    document.getElementsByTagName('head')[0].appendChild(script);
```
