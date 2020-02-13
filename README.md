
# react-native-tencentx5

## Getting started

`$ npm install react-native-tencentx5 --save`

### Link native dependencies

From react-native 0.60 autolinking 

`$ react-native link react-native-tencentx5`


## Usage
```javascript
import { X5WebView } from 'react-native-tencentx5';

<X5WebView
  url={"https://www.google.com"}
  style={{ flex: 1 }}
/>
```

## Props Index

- source
- style 
- onPageStarted
- onPageFinished
- onReceivedTitle
- onProgressChanged
- onGoBack
- [`onMessage`](README.md#onmessage)
- javaScriptEnabled
- domStorageEnabled
- userAgent
- cacheEnabled
- textZoom
- scalesPageToFit
- applicationNameForUserAgent
- allowFileAccessFromFileURLs
- allowUniversalAccessFromFileURLs
- mixedContentMode
- allowFileAccess
- geolocationEnabled
---

# Reference

## Props

### `onMessage`

Function that is invoked when the webview calls `window.WebViewJavascriptBridge.postMessage`. Setting this property will inject this global into your webview.

`window.WebViewJavascriptBridge.postMessage` accepts one argument, `data`, which will be available on the event object, `event.nativeEvent.data`. `data` must be a string.

| Type     | Required |
| -------- | -------- |
| function | No       |


---
