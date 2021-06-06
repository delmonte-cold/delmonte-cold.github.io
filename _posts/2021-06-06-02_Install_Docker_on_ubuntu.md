---
layout: single_v2
title:  "Docker 설치 (Ubuntu)"
tags : [Docker,Server]
---



### 2. pytorch container 생성
```bash
sudo docker run --name pytorch -v pytorch:/home -it pytorch/pytorch
```

### Reference
- [https://docs.docker.com/engine/install/ubuntu/](https://docs.docker.com/engine/install/ubuntu/)
