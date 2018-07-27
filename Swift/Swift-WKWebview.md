# Swift WKWebview
## 自定义 UserAgent 
iOS 9.0 以后可以通过customUserAgent 来定义UserAgent 
注意：通过此方法设置UserAgent将默认设置的UserAgent将被**清空**

```
/*! @abstract The custom user agent string or nil if no custom user agent string has been set.
*/
@available(iOS 9.0, *)
open var customUserAgent: String?
```
如果需要**添加**自定义的UserAgent可以通过以下方法设置

```
webView.evaluateJavaScript("navigator.userAgent") { [weak webView] (result, error) in
    if let webView = webView, let userAgent = result as? String {
        if #available(iOS 9.0, *) {
            webView.customUserAgent = userAgent + "/Custom Agent"
        }
   }
}
```
> 参考资料
> <https://stackoverflow.com/questions/26994491/set-useragent-in-wkwebview>


