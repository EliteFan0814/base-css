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
