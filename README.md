# busuanzi-modified

基于不蒜子2.3官网数据自定义站点访问量(site_pv, site_uv, page_pv)。Customize your site view count based on busuanzi.

## 修改

你可以自定义`busuanzi.pure.js`中的第75, 80, 85行，分别对应了站点访问量、独立访客和文章阅读量。取一个你喜欢的数字，然后自行压缩并托管。

根据你提供的代码和需求，你想自定义站点访问量、独立访客和文章阅读量的初始值。你可以按照以下步骤进行修改：

1. 选择你喜欢的数字作为初始值。假设你选择的数字分别为站点访问量（site_pv）、独立访客（site_uv）和文章阅读量（page_pv）。

2. 将选定的数字替换到相应的行中。根据你提供的代码，分别是第75、80和85行。

   - 对于站点访问量（site_pv），将数字替换到第75行的 `(parseInt(Date.now() * 0.0000005 - 8.25 * Math.pow(10, 5)) + parseInt(a[b]))` 部分。
   - 对于独立访客（site_uv），将数字替换到第80行的 `(parseInt(Date.now() * 0.0000005 - 8.27 * Math.pow(10, 5)) + parseInt(a[b]))` 部分。
   - 对于文章阅读量（page_pv），将数字替换到第85行的 `(parseInt(Date.now() * 0.000000005 - 8.1 * Math.pow(10, 3)) + parseInt(a[b]))` 部分。

   例如，假设你选择的数字分别为站点访问量为1000、独立访客为500和文章阅读量为2000，那么你可以进行如下替换：

   - 第75行：`parseInt(Date.now() * 0.0000005 - 8.25 * Math.pow(10, 5))` 替换为 `1000`。
   - 第80行：`parseInt(Date.now() * 0.0000005 - 8.27 * Math.pow(10, 5))` 替换为 `500`。
   - 第85行：`parseInt(Date.now() * 0.000000005 - 8.1 * Math.pow(10, 3))` 替换为 `2000`。

3. 修改完成后，保存文件并进行压缩。

4. 最后，你可以选择将压缩后的文件托管到你喜欢的位置，如GitHub、CDN等。

请注意，修改这段代码只会更改初始值，实际的访问量和阅读量数据还是需要通过其他方式进行统计和更新。这段代码只是用于展示初始值，并不能真实反映实际的访问量和阅读量。


## 部署

将你的网站从`busuanzi.ibruce.info`引用的`busuanzi.pure.mini.js`替换为新的js地址，如本仓库的`https://raw.githubusercontent.com/Pil0tXia/busuanzi-modified/main/busuanzi.pure.mini.js`

你也可以使用CDN加速访问：

- jsDelivr: `https://cdn.jsdelivr.net/gh/Pil0tXia/busuanzi-modified/busuanzi.pure.mini.js`

- 渺软公益CDN：`https://jsd.onmicrosoft.cn/gh/Pil0tXia/busuanzi-modified/busuanzi.pure.mini.js`

- 我自用的CDN（不作任何SLA承诺）：`https://static.pil0txia.com/assets/busuanzi/2.3/busuanzi.pure.mini.js`

如果你正在使用 Hexo 的 Butterfly 主题，请参考[这篇文档](https://butterfly.js.org/posts/4aa8abbe/#%E8%A8%AA%E5%95%8F%E4%BA%BA%E6%95%B8-busuanzi-UV-%E5%92%8C-PV)修改地址。

## 建议

建议将其用来迁移站点历史访问量即可，例如从@记录迁移到了www，却丢失了以前的访问量。数字改得太大，SEO指数却很低，会被人笑话的。这只是一个建议。
