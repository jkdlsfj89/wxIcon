# vue-weixin-emojis
【声明】
本repo仅可以用于学习用途
cdn已挂，请手动存放图片素材

微信表情包插件，查看[在线实例](https://codesandbox.io/s/wizardly-curie-h7mn7?file=/src/App.vue)

<div align=center>
    <img src="https://github.com/goforu/vue-weixin-emojis/raw/main/resources/demo.gif" height="400">
</div>

## 安装
```
npm i vue-weixin-emojis -S
```

### 引入包
``` javascript
// 引入安装包和样式
import WeixinEmojis from 'vue-weixin-emojis'
import 'vue-weixin-emojis/dist/vue-weixin-emojis.css'
Vue.use(WeixinEmojis)
```
**可选项**

如果你希望表情图片放在你们的服务器中，可将图片qqface.png放在项目的静态文件夹中（如: /public 或 /src/statics目录下）。并将url参数改成你放置的图片的位置。
``` javascript
Vue.use(WeixinEmojis, {url: 'path/to/qqface.png'})
```
图片素材 [qqface.png](https://github.com/goforu/vue-weixin-emojis/blob/main/public/qqface.png)

### 使用
表情面板组件，展示所有微信表情，点击会自动给value赋上相应表情key值
``` html
<emoji-picker v-model="value" height="300px" button/>
```
在转换成表情的地方使用以下方法
``` javascript
// 需要在vue组件（实例）中调用
this.value = this.$string2emoji(this.value)
// 修改已发出的表情，使用以下方法
this.value = this.$emoji2string(this.value)
```
### 作者与应用

<div align=center>
    <img src="https://github.com/goforu/vue-weixin-emojis/raw/main/resources/me_qrcode.jpeg" height="300">
    <p>欢迎添加作者微信</p>
</div>
