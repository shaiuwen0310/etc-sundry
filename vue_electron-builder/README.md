# vue electron-builder

## 使用vue plugin(適用於vue3)
* vue-cli-plugin-electron-builder
* 在vue專案下`vue add electron-builder`指令，即可安裝electron builder
* 再根據package.json script下打包指令，就會產生執行檔

## guthub範例：[A simple electron-vue project to test electron updates with github releases](https://github.com/alondanoch/electron-builder-auto-update-example)
* 此設定檔可使程式在linux與wondows做安裝
* out.zip為linux上的操作影片
* 在linux安裝後，可到`/home/$USER/.local/share/applications`刪除應用程式

## npm相關
* [npm init](https://www.cnblogs.com/WD-NewDemo/p/11141384.html)
* [弄懂 npm install 的 –save 與 –save-dev](https://chriskang028.wordpress.com/2017/07/05/%E5%BC%84%E6%87%82-npm-install-%E7%9A%84-dependencies-v-s-devdependencies/)
* [npm 如何查看一个包的版本信息？](https://blog.csdn.net/cvper/article/details/79543262)
* [What npm run do?](https://stackoverflow.com/questions/49275342/what-npm-run-do)
* [npm 基本指令](http://dreamerslab.com/blog/tw/npm-basic-commands/)
* [npm start 与 node app.js 的区别？](https://www.jianshu.com/p/e20831ad3185)
* [前端开发：运行项目提示XXX packages are looking for funding run npm fund for...的解决方法](https://juejin.cn/post/6970348539356381198)：npm install --no-fund
* 安裝yarn