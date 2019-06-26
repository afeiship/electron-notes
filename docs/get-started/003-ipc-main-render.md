# ipc/main/render


## main process
- Electron 运行 package.json 的 main 脚本的进程被称为主进程.
- 在主进程中运行的脚本通过创建 web 页面来展示用户界面。 一个 Electron 应用总是有且只有一个主进程。
- 由于 Electron 使用了 Chromium(谷歌浏览器)来展示 web 页面，所以 Chromium 的 多进程架构也被使用到。 每个 Electron 中的 web 页面运行在它自己的渲染进程中。
- 主进程使用 BrowserWindow 实例创建页面。每个 BrowserWindow 实例都在自己的渲 染进程里运行页面。 当一个 BrowserWindow实例被销毁后，相应的渲染进程也会被终止

![](http://ww3.sinaimg.cn/large/006tNc79gy1g4exk5ur59j30oi0mejsd.jpg)
![](http://ww1.sinaimg.cn/large/006BC6kqgy1g4exkne9i9j30f40dejrj.jpg)


## process/thread
进程: 进程是计算机中的程序关于某数据集合上的一次运行活动，是 系统进行资源分配和调度的基本单位，是操作系统结构的基础。
线程: 在一个程序里的一个执行路线就叫做线程(thread)。更准确的定义是: 线程是“一个进程内部的控制序列”。
线程和进程: 一个程序至少有一个进程,一个进程至少有一个线程

## ipcMain/ipcRender

```js

const { ipcMain, ipcRenderer, BrowserWindow } = require('electron')
ipcMain.on('message',(sender,event)=>{});


ipcRenderer.send('message', {name:'poetries', age: 100});
```
