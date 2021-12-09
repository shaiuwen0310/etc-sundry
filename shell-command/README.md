# shell-command記錄
### 指令
* 將路徑下所有檔案中有string1的字串都替換成string2
	```sh
	find ./ -type f -exec sed -i 's/string1/string2/g' {} \;
	```
* 將路徑下所有shell檔案都賦予+x權限
	```sh
	find ./ -type f -name "*.sh" -exec chmod +x {} \;
	```

