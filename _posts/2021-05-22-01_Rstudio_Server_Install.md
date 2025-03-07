---
layout: single_v2
title:  "Rstudio Server 설치"
tags : [R,Rstudio,Server]
---


# Rstudio Server (Ubuntu)
---

### 1. R install
```bash
sudo apt-get update
sudo apt-get install r-base
```
  
> Error 발생시
```bash
 sudo cp /etc/bash_completion.d/R /user/share/bash-completion/completions/R
 sudo apt-get -f install r-base
```

### 2. R Studio-server install 
```bash
sudo apt-get install gdebi-core
sudo apt-get install libapparmor1

wget 
https://download2.rstudio.org/rstudio-server-1.0.136-amd64.deb sudo gdebi rstudio-servr-1.0.136-amd64.deb
```

### 3. R studio-server 실행
```bash
sudo rstudio-server verify-installation
```

### 4. R studio-server 접속
- 서버IP:8787 로 접속
- 서버 계정과 비밀번호로 로그인

### 5. Reference
- [http://bizadmin.tistory.com/entry/ubuntu-%EC%97%90-R-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0](http://bizadmin.tistory.com/entry/ubuntu-%EC%97%90-R-%EC%84%A4%EC%B9%98%ED%95%98%EA%B8%B0) # R studio-server 설명
- [https://www.rstudio.com/products/rstudio/download-server/](https://www.rstudio.com/products/rstudio/download-server/) # R studio-server 다운로드
- [http://askubuntu.com/questions/855013/safely-cleanup-apt-get-after-a-failed-r-installation-from-an-added-repo](http://askubuntu.com/questions/855013/safely-cleanup-apt-get-after-a-failed-r-installation-from-an-added-repo) # Error 발생시 해결

