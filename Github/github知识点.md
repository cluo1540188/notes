## 上传文件到github上出现的bug
#### A.git拉取github失败，Failed to connect to github.com port 443: Timed out
##### ==git config --global --unset http.proxy==
##### ==git config --global --unset https.proxy==

#### B.Git报错解决：fatal: unable to access ‘https://github.com/…’: OpenSSL SSL_read: Connection was reset, errno 10054

##### ==git config --global http.sslVerify "false"==

