# shell-command記錄
## 以下為linux指令，mac不適用
### 查找並替換字串
* 將路徑下所有檔案中有string1的字串都替換成string2
	```sh
	find ./ -type f -exec sed -i 's/string1/string2/g' {} \;
	```
* 將路徑下所有shell檔案都賦予+x權限
	```sh
	find ./ -type f -name "*.sh" -exec chmod +x {} \;
	```
 * 指令中有變數
	```sh
	str=$(grep -h "$(REGISTRY_LOCATION)" ${SERVICE_K8S_YAML_FOLDER} -r)
        image_tag=$(echo "$str" | cut -d ':' -f 3)
 	find ${SERVICE_K8S_YAML_FOLDER} -type f -exec sed -i "s/$(printf '%q' "${image_tag}")/$(printf '%q' "$(COMMIT_HASH)")/g" {} \;
	```
### 查看憑證資訊
* You can display the contents of a PEM formatted certificate under Linux, using openssl:
```sh
openssl x509 -in acs.cdroutertest.com.pem -text
```

