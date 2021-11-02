# vue electron-builder

## 使用vue plugin(適用於vue3)
* vue-cli-plugin-electron-builder
* 在vue專案下`vue add electron-builder`指令，即可安裝electron builder
* 再根據package.json script下打包指令，就會產生執行檔

## guthub範例：[A simple electron-vue project to test electron updates with github releases](https://github.com/alondanoch/electron-builder-auto-update-example)
* 此設定檔可使程式在linux與wondows做安裝
* out.zip為linux上的操作影片
* 在linux安裝後，可到`/home/$USER/.local/share/applications`刪除應用程式