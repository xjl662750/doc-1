> # Quick Start

> ## Step 1：Install git
> ```
> git config --global --list
> git config --global user.name "snoredude"
> git config --global user.email "caffeine.dude.go@gmail.com"
> git config --global --unset http.cookiefile
> ```
> 

> ## Step 2：Install go

> ## Step 3：Install vscode

> ## Step 4：Start project
> ```
> git clone https://github.com/snoredude/doc.git
> cd /project/doc
> go version
> go env
> go env -w GO111MODULE=on
> go env -w GOPROXY=https://goproxy.cn,direct
> go mod init doc
> ```
> - go 版本 1.11 以上才能使用 go modules  
> - GO111MODULE=on 开启 go modules  
> - go env -w 会将配置信息写到环境变量 GOENV 中，可以用 `go env` 命令查看 go 的环境变量
> - 在 main.go 的同级目录下执行：`go mod init project_name` ，可以生成该项目的 go.mod 文件，  go.mod 会自动对项目进行依赖管理
> - 使用 go mod 管理项目时，依赖包存放在 `$GOPATH/pkg` 目录下，并且允许同一个依赖包有多个不同的版本存在
> - 多个项目可以共享 `$GOPATH/pkg` 目录下依赖包缓存
> - 在 windows 系统中，`$GOPATH/pkg` 目录的文件结构为：
>   1. mod
>   2. sumdb
>   3. windows_amd64

