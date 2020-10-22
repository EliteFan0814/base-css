##### 单行/多行省略：
```css
<!--单行省略-->
.single-lines-omit{
    width: 27em;
    white-space: nowrap;
    text-overflow: ellipsis;
    -o-text-overflow: ellipsis;
    overflow: hidden;
}
<!--多行省略-->
.multiple-lines-omit {
    overflow: hidden;
    display: -webkit-box;
    -webkit-line-clamp: 3;
    -webkit-box-orient: vertical;
}
```
##### 背景图片：
```css
.bg{
    background-color: #fff;
    background-image:url('fpc.png');
    background-repeat: no-repeat;
    background-size:100% 100%;
}
```
##### 绝对定位居中
```css
<!--水平居中-->
.horizontal-center{
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
}
<!--垂直居中-->
.vertical-center{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
}
<!--水平垂直居中-->
.absolute-center{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
```
##### 去除input默认样式(包括IOS中input的默认阴影)
```css
input{
  box-shadow:none; /*去除阴影*/
  outline: none;/*聚焦input的蓝色边框*/
  resize: none; /*textarea 禁止拖拽*/
  border: none; /*去除边框*/
  -webkit-appearance: none;/*常用于IOS下移除原生样式*/
  -webkit-tap-highlight-color: rgba(0,0,0,0); /*点击高亮的颜色*/
}
```
##### 取消父子元素的透明度传递
父元素使用rgba就可以避免：
```css
.parent{
  background:rgba(216,241,250,0.82);
}
.child{
  background:red;
}
```
##### 单行文字两边对齐(兼容ios)
*这里注意左边的 key 值是否带分号，分号也算一个字符！  
html 代码如下：
```html
  <div class="item-wrap">
    <div class="left-name">
      <div class="name">姓名</div>：
    </div>
    <div class="right-value">
      武大郎
    </div>
  </div>
  <div class="item-wrap">
    <div class="left-name">
      <div class="name">所在城市</div>：
    </div>
    <div class="right-value">
      李家窝棚
    </div>
  </div>
```
css 代码：
```css
.item-wrap,
.left-name {
  display: flex;
  font-size:24px;
  line-height:30px;
}
.left-name .name {
  width: 100px;  /* 这里一定要使用 width 不能使用 min-width max-width */
  height:30px;  /* 一定要限定高度，高度和 line-height 一致时为上下居中显示 */
  text-align: justify;
  text-align-last: justify;
  text-justify: inter-ideograph;
}
.left-name .name::after {
  display: inline-block;
  content: '';
  width: 100%;
}
```
##### 隐藏滚动条
```css
div{
 width: 24rem;
 height: 20rem;
 overflow: scroll;
}
div::-webkit-scrollbar {
 display: none;
}
```
##### 固定底部无限加载
```css
div{
 box-sizing: border-box;
 width: 100%;
 position: fixed;
 top: 10rem;
 bottom: 0;
 overflow-y: scroll;
}
```






























