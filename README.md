# gin-web-layout
gin web project layout



```golang
.
├── LICENSE
├── Makefile
├── README.md
├── api											// api 存放 openAPI  和 proto 文件, 用 CI 生成
│   └── app
│       ├── a.proto								// rpc 的 proto 文件
│       └── swagger.json
├── cmd
│   └── app										// 应用名
│       └── main.go								// 入口函数
├── configs										// 全局配置文件
│   └── app.yaml
├── deploy										// 部署 yaml 文件, 包含 k8s , docker-compose 等
│   ├── build
│   │   └── Dockerfile
│   ├── docker-compose
│   │   └── docker-compose.yaml
│   └── kubernetes
│       ├── app-deployment.yaml
│       └── app-service.yaml
├── go.mod
├── internal									// 内部业务逻辑, 按 app 划分
│   └── app
│       ├── controller							// mvc 的 c
│       ├── dao									// 操作数据库层
│       ├── dto									// request 和 response 转换
│       ├── ecode								// 业务错误code
│       ├── internal
│       ├── models								// model 层, 转换 数据库模型
│       ├── service								// service 层
│       └── test
│           └── testdata
├── pkg
│   ├── log
│   └── registry
└── third_party
    └── google
        └── api
            ├── annotations.proto
            ├── http.proto
            └── httpbody.proto
```