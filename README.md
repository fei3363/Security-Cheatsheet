# Security-Cheatsheet



## install docker & docker-compose
1. 更新 Ubuntu 套件庫
    - `sudo apt-get update`
2. 安裝所需套件
    - `sudo apt-get install apt-transport-https ca-certificates curl software-properties-common`
3. 透過 curl 下載外部 docker 來源的金鑰
    - `wget https://download.docker.com/linux/ubuntu/gpg`
4. 並匯入該金鑰
    - `sudo apt-key add gpg`
5. 將外部的 `repository` 來源匯入
    - `sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"`
6. 接著開始安裝Docker套件
    - `sudo apt-get install docker-ce`
7. 最後加入使用者的帳號進入 docker 群組
    - `sudo gpasswd -a ${USER} docker`
8. 確認安裝後的 Docekr 服務是否執行 (兩者擇一即可)
    - `sudo service docker status`
    - `sudo systemctl status docker`
9. 最後我們要重啟我們的 terminal
    - `bash`
10. 從 docker 的 compose 專案拉檔案下來
    - `sudo curl -L "https://github.com/docker/compose/releases/download/1.25.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`
11. 增加執行權限
    - `sudo chmod +x /usr/local/bin/docker-compose`
