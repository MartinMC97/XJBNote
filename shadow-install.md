### 安装 shadow
由于未能解决的原因，这次 shadow 安装就用docker镜像的那个了。（也算不上是安装）

#### 安装步骤
1. 安装 Docker 。安装过程就不在这BB了，教程很多。 这里放一个教程做为参考。[链接](https://yeasy.gitbooks.io/docker_practice/content/install/ "链接")
2. 点击 [这里](https://security.cs.georgetown.edu/shadow-docker-images/shadow-tor.tar.gz "这里") 下载官方提供的 Docker 镜像。
3. 加载镜像
```shell
gunzip -c shadow-tor.tar.gz | docker load
```
4. 运行
```shell
docker run -t -i -u shadow shadow-tor /bin/bash
```
5. 对容器做完修改后记得用 `docker commit` 命令保存更改。

### 配置 shadow 的 Tor 插件
使用名为 `shadow-plugin-tor` 的插件可以在本地创建一个Tor网络并模拟数据传输。
