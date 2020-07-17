##### h5 页面嵌入QQ客服代码  
```html
<a href="mqqwpa://im/chat?chat_type=wpa&uin={{yourQQNumber}}&version=1&src_type=web&web_src=oicqzone.com"></a>
```

##### 将一个数组分为多个数组  
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
##### 将对象转换为数组
###### 方式1
示例：{userName:'elite',local:'china'} =>[{name:'userName',value:'elite'},{name:'local',value:'china'}]
```js
const objTransToArray = function(obj){
   let arr = [];
   Object.keys(obj).forEach(itemKey => {
     let o = {};
     o.name = itemKey
     o.value = obj[itemKey]
     arr.push(o)
   })
    return arr
}
```
###### 方式2
示例：{userName:'elite',local:'china'} =>[{userName:'elite'},{local:'china'}]
```js
const objTransToArray = function(obj){
   let arr = [];
   Object.keys(obj).forEach(itemKey => {
     let o = {};
     o[itemKey] = obj[itemKey]
     arr.push(o)
   })
    return arr
}
```









