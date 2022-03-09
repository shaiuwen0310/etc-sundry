# shell-command記錄
### 查找並替換字串
* 將路徑下所有檔案中有string1的字串都替換成string2
	```sh
	find ./ -type f -exec sed -i 's/string1/string2/g' {} \;
	```
* 將路徑下所有shell檔案都賦予+x權限
	```sh
	find ./ -type f -name "*.sh" -exec chmod +x {} \;
	```
### 查看憑證資訊
* You can display the contents of a PEM formatted certificate under Linux, using openssl:
```sh
openssl x509 -in acs.cdroutertest.com.pem -text
```

