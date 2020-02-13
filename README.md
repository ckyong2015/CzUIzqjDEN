
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
- [`javaScriptEnabled`](README.md#javascriptenabled)
- [`domStorageEnabled`](README.md#domstorageenabled)
- [`userAgent`](README.md#useragent)
- [`cacheEnabled`](README.md#cacheEnabled)
- [`textZoom`](README.md#textZoom)
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

### `javaScriptEnabled`

Boolean value to enable JavaScript in the `WebView`.

| Type | Required |
| ---- | -------- |
| bool | No       |

---

### `domStorageEnabled`

Boolean value to control whether DOM Storage is enabled. Used only in Android.

| Type | Required |
| ---- | -------- |
| bool | No       |

---

### `userAgent`

Sets the user-agent for the `WebView`.

| Type   | Required |
| ------ | -------- |
| string | No       |

---

### `cacheEnabled`

Sets whether WebView should use browser caching.

| Type    | Required |
| ------- | -------- |
| boolean | No       |

---

### `textZoom`

If the user has set a custom font size in the Android system, an undesirable scale of the site interface in WebView occurs.

| Type   | Required |
| ------ | -------- |
| number | No       |
