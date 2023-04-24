## gitlab runner
### 開發環境的gitlab runner經常下載docker image好像會造成此錯誤
* https://www.dianbanjiu.com/post/gitlab-runner-%E8%BF%90%E8%A1%8C%E6%8A%A5%E9%94%991/
```
WARNING: Failed to pull image with policy "always": Error response from daemon: Get "https://registry-1.docker.io/v2/": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers) (manager.go:237:35s)
ERROR: Job failed: failed to pull image "docker:20.10.16-dind" with specified policies [always]: Error response from daemon: Get "https://registry-1.docker.io/v2/": net/http: request canceled while waiting for connection (Client.Timeout exceeded while awaiting headers) (manager.go:237:35s)
```
* 可以調整/etc/tf-ci-gitlab-runner成pull_policy = ["if-not-present"]
* 有時候docker login也會變成可正常下載
### CI/CD時一直出現莫名其妙的錯誤
```
fatal: bad config line 14 in file /builds/TEST/workspace/.gitmodules
```
* 刪掉gitlab runner並且重新建立
