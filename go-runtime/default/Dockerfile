FROM golang:1.16

ADD https://github.com/cdr/code-server/releases/download/v3.10.2/code-server-3.10.2-linux-amd64.tar.gz /usr/local/code-server/

# 解压

WORKDIR /usr/local/code-server

RUN tar -xzf code-server-3.10.2-linux-amd64.tar.gz

# https://github.com/cdr/code-server/releases/tag/v3.10.2

# 添加go 语言插件

# 下载插件

ADD golang.Go-0.26.0.vsix /root/

ENV code_server /usr/local/code-server/code-server-3.10.2-linux-amd64/

RUN ${code_server}/bin/code-server --install-extension /root/golang.Go-0.26.0.vsix

# 启动服务器

EXPOSE 8080

ENTRYPOINT ${code_server}/bin/code-server

