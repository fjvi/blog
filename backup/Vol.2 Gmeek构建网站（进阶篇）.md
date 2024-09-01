## 一、主题配置

### 1. 手动模式（默认）
这种模式就是当访问者第一次打开博客页面时，呈现的是亮主题。
访问者可以通过页面右上角的按钮随意切换（亮/暗/跟随系统），当切换过后，会自动在浏览器存储目前的选择，之后访问者用同一浏览器再打开博客任何页面，则自动为上次选择的模式。
```
"themeMode":"manual",
"dayTheme":"light",
"nightTheme":"dark",
```

### 2. 固定模式
`themeMode`为`fix`，
`dayTheme`定义想要固定的主题，可以定义为`light`则永远为亮主题，定义为`dark`则永远为暗主题，用户无法切换
`nightTheme`定义的就是`utterances`评论框的永久固定主题。

#### 2.1. 固定亮主题
```
"themeMode":"fix",
"dayTheme":"light",
"nightTheme":"github-light",
```
#### 2.2. 固定暗主题
```
"themeMode":"fix",
"dayTheme":"dark",
"nightTheme":"dark-blue",
```
> [!TIP]
> 亮暗主题可以查看[github官方](https://github.com/settings/appearance)支持的主题，这里都支持
- 亮主题：`light` `light_high_contrast` `light_colorblind ` `light_tritanopia `
- 暗主题：`dark` `dark_high_contrast` `dark_colorblind` `dark_tritanopia` `dark_dimmed`

> [!TIP]
> [utterances](https://utteranc.es/)评论框的主题选择有：
`github-light` `github-dark` `preferred-color-scheme` `github-dark-orange` `icy-dark` `dark-blue` `photon-dark` `boxy-light` `gruvbox-dark`


## 二、提示标签
Github的语法里面有5中警报强调信息，分别是`NOTE` `TIP` `IMPORTANT` `WARNING` `CAUTION` 。在写文章的时候，适当使用可以提高文章的可读性

### 使用方式：
```
> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.
```

### 效果

> [!NOTE]
> Useful information that users should know, even when skimming content.

> [!TIP]
> Helpful advice for doing things better or more easily.

> [!IMPORTANT]
> Key information users need to know to achieve their goal.

> [!WARNING]
> Urgent info that needs immediate user attention to avoid problems.

> [!CAUTION]
> Advises about risks or negative outcomes of certain actions.















## 三、特殊设置
### 1. 导入以前的文章 
如需修改发布时间，可以在文章最后一行添加如下代码。里面的时间是采用时间戳的形式，可以用如下[时间形式转换网站](https://tool.lu/timestamp)转换。  
```html
<!-- ##{"timestamp":1490764800}## -->
```

### 2. 单篇文章自定义参数
自定义单篇文章页面的`style`和`script`
```html
<!-- ##{"style":"<style>#postBody{font-size:20px}</style>"}## -->
```
```html
<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>"}## -->
```

### 3. 单篇文章多种自定义参数
可同时一起添加多种自定义参数：  
```html
<!-- ##{"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>","style":"<style>#postBody{font-size:20px}</style>","timestamp":1490764800}## -->
```

### 4. 全局文章自定义参数
添加全局文章页面的`style`和`script`，在`config.json`文件中添加
```javascript
"style":"<style>#postBody{font-size:20px}</style>",
"script":"<script async src='//busuanzi.ibruce.info/busuanzi/2.3/busuanzi.pure.mini.js'></script>",
```

### 5. 置顶博客文章
只需要`Pin issue`后，手动全局生成一次即可。


### 6. 删除文章
只需要`Close issue`或者`Delete issue`后，再手动全局生成一次即可。


## 四、进阶教程

Gmeek的可定制化功能非常高，下面的链接是一些更加高级的设置教程，还有插件的使用等。
https://meekdai.github.io/tag.html#Gmeek

<!-- ##{"script":"<script src='https://blog.meekdai.com/Gmeek/plugins/GmeekTOC.js'></script>"}## -->










---
[Gmeek基礎](https://blog.meekdai.com/post/Gmeek-kuai-su-shang-shou.html)
[Gmeek进阶](https://blog.meekdai.com/tag.html#Gmeek)

<details>
    <summary>点我展开看代码</summary>
    <pre><code>
# 这里空一行，下面开始写代码
# 在这里写折叠的代码
# 最后这两行结束标签一定要顶格写且不能接在代码后面！！！
</code></pre>
</details>


# MarkDown
## h2
### h3
#### h4

# 图片img
`Gmeek-html<img src="https://picsum.photos/200">`

# 内嵌框架iframe-网站
`Gmeek-html<iframe src="https://music.meekdai.com/#61" width="100%" height="460px" frameborder="0" allowfullscreen="true"></iframe>`

# 内嵌框架iframe-歌曲
`Gmeek-html<iframe style='border-radius:12px' src='https://open.spotify.com/embed/track/0U3fV7K4WFfVRgLGEAKh3g?utm_source=generator' width='100%' height='152' frameBorder='0' allowfullscreen='' allow='autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture' loading='lazy'></iframe>`

# 内嵌框架iframe-视频
`Gmeek-html<iframe src="//player.bilibili.com/player.html?isOutside=true&aid=1604800941&bvid=BV1qm421M7Xs&cid=1557311907&p=1&autoplay=0" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="100%" height="460px"></iframe>`


