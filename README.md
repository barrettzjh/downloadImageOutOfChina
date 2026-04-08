# downloadImageOutOfChina
下载国外镜像

## 使用方法

1. 编辑 `images.txt` 文件，添加需要下载的镜像
2. 提交并推送到 main 分支，自动触发构建

### images.txt 格式

```
# 直接同步，目标镜像名与源镜像相同
labring/kubernetes-docker:v1.29.5-arm64

# 自定义目标镜像名（源镜像=目标镜像）
# 下载后为: registry.cn-hangzhou.aliyuncs.com/zhangjinhui/nginx:latest
nginx:latest=nginx:latest

# 支持多个镜像，每行一个
busybox:latest
alpine:latest
redis:7-alpine
```

### 支持的镜像源
- Docker Hub
- GitHub Container Registry (ghcr.io)
- 其他公开镜像仓库
