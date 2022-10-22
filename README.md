该项目为 PsChina/wx-base64-qrcode 的fork版本，修复了不会随长度调整二维码版本的BUG
使用方法：下载 wxqrcode.js 到本地

可生成dataUrl,兼容性较好

# 小程序使用

```xml
<image src="{{imageSrc}}"></image>
```
```js
import QR from "./wxqrcode.js";
Page({
  data: {
      imageSrc:'',
  },
  onLoad(){
    const size = 100; //宽高

    const base64Data = QR.createQrCodeImg( 'any str code', size) // base64的数据

    this.setData({
        imageSrc:base64Data
    })
  }
})
```
