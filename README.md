
# react-native-tencentx5

## Getting started

`$ npm install react-native-tencentx5 --save`

### Link native dependencies

From react-native 0.60 autolinking 

`$ react-native link react-native-tencentx5`


## Usage
```javascript
import { WebView } from 'react-native-tencentx5';

<WebView
  url={"https://facebook.github.io/react-native"}
  style={{ flex: 1 }}
/>
```

## Props Index

- [`url`](README.md#url)
- [`style`](README.md#style)
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

### `url`

Loads static URI in the WebView.

| Type   | Required |
| ------ | -------- |
| string | No       |

Example:

```jsx
<WebView
  url={'https://facebook.github.io/react-native'}
/>
```

---

### `style`

A style object that allow you to customize the `WebView` style.

| Type  | Required |
| ----- | -------- |
| style | No       |

Example:

```jsx
<WebView
  source={{ uri: 'https://facebook.github.io/react-native' }}
  style={{ flex: 1 }}
/>
```

---

### `onMessage`

Function that is invoked when the webview calls `window.WebViewJavascriptBridge.postMessage`. Setting this property will inject this global into your webview.

`window.WebViewJavascriptBridge.postMessage` accepts one argument, `data`, which will be available on the event object, `event.nativeEvent.data`. `data` must be a string.

| Type     | Required |
| -------- | -------- |
| function | No       |


---
