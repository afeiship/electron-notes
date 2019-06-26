# get-started

~~~
NW.js 和 Electron 都可以用前端的知识来开发桌面应用。NW.js 和 Electron起初是同一 个作者开发。后来种种原因分为两个产品。一个命名为 NW.js(英特尔公司提供技术支持)、 另一命名为 Electron(Github 公司提供技术支持)。
NW.js 和 Electron 可以用 Nodejs 中几乎所有的模块。NW.js 和 Electron不仅可以把 html 写的 web 页面打包成跨平台可以安装到电脑上面的软件，也可以通过 javascript 访问操作 系统原生的 UI 和 Api(控制窗口、添加菜单项目、托盘应用菜单、读写文件、访问剪贴板)。
~~~


## history
2013 年 4 月 Atom Shell 项目启动 。
2014 年 5 月 Atom Shell 被开源 。
2015 年 4 月 Atom Shell 被重命名为 Electron
2016 年 5 月 Electron 发布了 v1.0.0 版本


## update
Electron 的版本发布相当频繁。每当 Chromium、Node.js 有重要的 bug 修复，新 API 或是版本更新时 Electron 会发布新版本。


## core concept
Electron 的核心理念是:保持 Electron 的体积小和可持续性开发。
如:为了保持 Electron 的小巧 (文件体积) 和可持续性开发 (以防依赖库和 API 的泛滥) ， Electron 限制了所使用的核心项目的数量。
比如 Electron 只用了 Chromium 的渲染库而不是其全部组件。这使得升级 Chromium 更加容易，但也意味着 Electron 缺少了 Google Chrome 里的一些浏览器相关的特性。 添加到 Electron 的新功能应该主要是原生 API。 如果可以的话，一个功能应该尽可能的成 为一个 Node.js 模块。
