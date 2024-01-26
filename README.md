!> 文档模板

## 命令行启动
  * python2：``` python2 -m SimpleHTTPServer ```
  * python3：``` python3 -m http.server ```
  * nodejs：``` npx http-server ```
  * php：``` php -S localhost:8000 ```
  * ...

## 说明
  * github个人主页部署参见：[链接](https://docsify.js.org/#/zh-cn/deploy?id=github-pages)
  * 模板基于docsify，支持常规markdown语法、代码高亮、代码折叠、代码复制、图片缩放等功能；另有需可自行增减功能
  * 如docsify基本功能+插件无法满足需求，可考虑vuepress等开源文档工具
  * 不怎么变量的静态资源文件可放入`_static`目录，用户上传其他图片等资源文件可放入`_media`目录
  * 内网部署可将CDN静态资源文件地址改为指向./_static/asset/目录下，然后nginx配置类似如下：
    ```nginx
    location / {
      alias /文档目录
      index index.html;
      autoindex on;
    }
    ```

## 增删改查
  * 新增主题目录：
    * 目录创建于`docs/`下、建议英文
    * `index.html`修改`alias`和`nameLink`，其中`nameLink`按需如有点击标题跳转那就改，否则不动
    * 新主题目录下新增 `_sidebar.md` 作为右侧菜单栏，且和 `/_navbar.md` 对应主题下拉菜单大类尽量保持一致
    * 新主题目录下可创建一个 `README.md` 文件来作为路由的默认网页
  * 更改删除：参见新增的步骤对应操作