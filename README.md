
#
# WKWebview
#

最近因為在試如何能讓JS <-> APP 互相交握 , 所以需要如何判斷網頁是開在 iOS 的WKWebview 中。
下面的程式是在網路上找到的，記錄一下，怕會忘記。
var iOS = (navigator.userAgent.match(/(iPad|iPhone|iPod)/g) ? true : false);
var isWKWebView = false;
if (window.webkit && window.webkit.messageHandlers) {
    isWKWebView = true;
}
參考網址：https://stackoverflow.com/questions/28795476/detect-if-page-is-loaded-inside-wkwebview-in-javascript
