# go-study

## 配置国内镜像代理
```
# 配置阿里云镜像
go env -w GOPROXY=https://mirrors.aliyun.com/goproxy/
# 验证镜像
go env|grep GOPROXY
```
## 常用命令
```
# 添加新 module
go mod tidy

# 查询指定包的所有版本
go list -m -versions github.com/sirupsen/logrus

# 依赖包降级
go mod edit -require=github.com/sirupsen/logrus@v1.7.0
go mod tidy

# 依赖包升级
go get github.com/sirupsen/logrus@v1.7.1

# vendor
go mod vendor
go build -mod=vendor
```

