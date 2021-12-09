# git指令記錄

1. git免輸入帳密，調整專案下.git的config檔：

    ```
    [remote "origin"]
            url = http://192.168.101.101/group/test.git
    ```

    改成增加`帳號:密碼@`

    ```
    [remote "origin"]
            url = http://account:pwd123@192.168.101.101/group/test.git
    ```

2. commit連結issue:
  * 在輸入commit內容時打上：close #1
  * 1為issue編號，井字號前面要有空白鍵
  * ![pic1.png](./img/pic1.png)

3. 遇到此錯誤訊息時，若信任該server，可先設定GIT_SSL_NO_VERIFY=1再進行連線
    ```
    fatal: unable to access 'https://PROJECT_URL': server certificate verification failed. CAfile: /etc/ssl/certs/ca-certificates.crt CRLfile: none

    ```
    輸入指令
    ```sh
    export GIT_SSL_NO_VERIFY=1
    ```


