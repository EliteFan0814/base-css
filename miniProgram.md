#### vscode中.scss实时转换为.wxss / vscode中使用scss
1. 首先在vscode中安装插件 easySass
2. 在vscode首选项中找到 settings.json 配置文件
3. 在settings.json配置文件中添加如下代码 
```json
{
  "easysass.formats": [
    {
      "format": "expanded", // 转化样式：没有缩进的、扩展的css代码
      "extension": ".wxss" // sass/scss文件要转化的后缀名
    }
  ]
}
```
4. 同时也支持转化为.css .min.css等格式，只需再次添加配置就行：
```json
{
  "easysass.formats": [
   // ~~~省略~~~
    {
      "format": "expanded",
      "extension": ".css"
    },
    {
      "format": "compressed",
      "extension": ".min.css"
    }
  ]
}
```
5. 顺便在.gitignore中也可添加忽略sass缓存文件的配置
```
.sass-cache/
*.css.map
*.sass.map
*.scss.map
*.css
```

#### 小程序中 px 和 rpx 互相转化
```
px = rpx / 750 * wx.getSystemInfoSync().windowWidth  
rpx = px * 750 / wx.getSystemInfoSync().windowWidth  
```
注：  
wx.getSystemInfoSync().windowWidth 单位为 px  
[小程序获取系统信息](https://developers.weixin.qq.com/miniprogram/dev/api/base/system/system-info/wx.getSystemInfoSync.html)  
