Dockerfile 库

# 进入到pwn目录中, build一个新镜像:
$ cd pwn
$ sudo docker build -t ubuntu:stack1 .

# 随机端口启动 -P
$ sudo docker run --name stack1 -it -d -P ubuntu:stack1

# 固定端口启动 -p
$ sudo docker run --name stack1 -it -d -p 10001:10001 -p 10002:10002 -p 10003:10003 -p 10004:10004 -p 10005:10005 ubuntu:stack1

# 停止、删除镜像
$ sudo docker stop stack1;sudo docker rm stack1;
