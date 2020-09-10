#### vscode中使用scss
1. 首先在vscode中安装插件 easySass
2. 在项目根目录创建 .vscode 文件夹
3. 在 .vscode 文件夹内创建 settings.json
4. settings.json 内容如下  
```json
{
  "easysass.formats": [
    {
      "format": "expanded", // 没有缩进的、扩展的css代码
      "extension": ".wxss" //转化的后缀名
    }
  ]
}
```
5. 顺便在.gitignore中也可添加忽略sass缓存文件
```
.sass-cache/
*.css.map
*.sass.map
*.scss.map
*.css
```
