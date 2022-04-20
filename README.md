# barcode
基于 Canvas 2D 微信小程序生成一维码，支持同层渲染，防止原生组件在最上方导致的遮挡问题
# 使用示例
wxml
<canvas type="2d" id="barcode" style="width: 500rpx; height: 176rpx;"></canvas>
js
wx.createSelectorQuery().select('#barcode')
.fields({
  node: true,
  size: true
})
.exec((res) => {
  var canvas = res[0].node
  let width = res[0].width
  let height = res[0].height
  barcode.code128(canvas, "123456", width, height) // 123456为条码内容
})

![image](https://user-images.githubusercontent.com/13643077/164130578-6c175c30-dbd9-45df-a823-75e4228264d7.png)
![image](https://user-images.githubusercontent.com/13643077/164131249-70406bec-f3e2-434b-908b-9289c4086ed8.png)
