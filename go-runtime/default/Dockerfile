FROM golang:1.16

ADD https://github.com/cdr/code-server/releases/download/v3.10.2/code-server-3.10.2-linux-amd64.tar.gz /usr/local/code-server
# https://github.com/cdr/code-server/releases/tag/v3.10.2

# 添加go 语言插件

# 下载插件

ADD https://marketplace.visualstudio.com/_apis/public/gallery/publishers/golang/vsextensions/Go/0.26.0/vspackage /root/

ENV code-server /usr/local/code-server/code-server-3.10.2-linux-amd64/

RUN ${code-server}/bin/code-server code --install-extension /root/golang.Go-0.26.0.vsix

# 启动服务器

CMD ${code-server}/bin/code-server

