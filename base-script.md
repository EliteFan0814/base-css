h5 页面嵌入QQ客服代码  
```html
<a href="mqqwpa://im/chat?chat_type=wpa&uin={{yourQQNumber}}&version=1&src_type=web&web_src=oicqzone.com"></a>
```

将一个数组分为多个数组  
示例：[1,2,3,4,5,6,7,8,9,10] => [[1, 2, 3, 4], [5, 6, 7, 8], [9, 10]]

```js
const sliceArray = function(targetArray,number){
   const page = Math.ceil(targetArray.length / number)
   const returnArr = []
   for (let i = 0; i < page; i++) {
     returnArr[i] = targetArray.slice(i * number, (i + 1) * number)
   }
  return returnArr
}
```
