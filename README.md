# Yolks

可与翼龙的 Egg 系统(预设)一起使用的精选核心镜像合集。每个镜像都会定期重建，以确保依赖关系始终是最新的。

镜像托管在 `registry.cn-shanghai.aliyuncs.com` 上，并存在于 `games`、`installers` 和 `yolks` 空间下。 在确定镜像将位于哪个空间下时使用以下逻辑：

* `oses` — 包含核心包的基础镜像，帮助您入门。
* `games` — 存储库中 `games` 文件夹中的任何内容。这些是为运行特定游戏或游戏类型而构建的镜像。
* `installers` — `installers` 目录中的任何内容。这些镜像将被用于预设的安装脚本使用，而不是用于实际运行游戏服务器。这些镜像仅旨在通预安装常见的安装依赖项（例如 `curl` 和 `wget`）来减少安装时间和额外网络开支。
* `yolks` — 这些是更通用的图像，允许运行不同类型的游戏或脚本。它们通常只是特定版本的软件，并允许翼龙中的不同预设切换使用环境。例如用于运行机器人、Minecraft 服务器等 Java 或 Python 之类的环境。

所有这些镜像都可用于 `linux/amd64` 和 `linux/arm64` 版本，除非另有说明，要在 arm64 系统上使用这些镜像，不需要对它们的标签进行修改，它们应该可以正常工作。

## 贡献

当向现有镜像添加新版本时，例如 `java v42`，您需要将其添加到 `java` 的子文件夹中，例如 `java/42/Dockerfile`。还请更新正确的 `.github/workflows` 文件，以确保正确标记此新版本。

## 可用镜像

* [`base oses`](https://github.com/pterodactyl-china/yolks/tree/master/oses)
  * [`alpine`](https://github.com/pterodactyl-china/yolks/tree/master/oses/alpine)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:alpine`
  * [`debian`](https://github.com/pterodactyl-china/yolks/tree/master/oses/debian)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:debian`
* [`games`](https://github.com/pterodactyl-china/yolks/tree/master/games)
  * [`rust`](https://github.com/pterodactyl-china/yolks/tree/master/games/rust)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/games:rust`
  * [`source`](https://github.com/pterodactyl-china/yolks/tree/master/games/source)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/games:source`
  * [`hytale`](https://github.com/pterodactyl-china/yolks/tree/master/games/hytale)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/games:hytale`
* [`golang`](https://github.com/pterodactyl-china/yolks/tree/master/go)
  * [`go1.14`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.14)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.14`
  * [`go1.15`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.15)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.15`
  * [`go1.16`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.16`
  * [`go1.17`](https://github.com/pterodactyl-china/yolks/tree/master/go/1.17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:go_1.17`
* [`java`](https://github.com/pterodactyl-china/yolks/tree/master/java)
  * [`java8`](https://github.com/pterodactyl-china/yolks/tree/master/java/8)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_8`
  * [`java8 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/8j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_8j9`
  * [`java8 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/8zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_8zulu`
  * [`java11`](https://github.com/pterodactyl-china/yolks/tree/master/java/11)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_11`
  * [`java11 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/11j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_11j9`
  * [`java11 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/11zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_11zulu`
  * [`java16`](https://github.com/pterodactyl-china/yolks/tree/master/java/16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_16`
  * [`java16 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/16j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_16j9`
  * [`java16 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/16zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_16zulu`
  * [`java17`](https://github.com/pterodactyl-china/yolks/tree/master/java/17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_17`
  * [`java17 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/17j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_17j9`
  * [`java17 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/17zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_17zulu`
  * [`java18`](https://github.com/pterodactyl-china/yolks/tree/master/java/18)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_18`
  * [`java18 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/18j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_18j9`
  * [`java18 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/18zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_18zulu`
  * [`java19`](https://github.com/pterodactyl-china/yolks/tree/master/java/19)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_19`
  * [`java19 - OpenJ9`](https://github.com/pterodactyl-china/yolks/tree/master/java/19j9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_19j9`
  * [`java19 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/19zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_19zulu`
  * [`java21`](https://github.com/pterodactyl-china/yolks/tree/master/java/21)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_21`
  * [`java21 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/21zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_21zulu`
  * [`java25`](https://github.com/pterodactyl-china/yolks/tree/master/java/25)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_25`
  * [`java25 - Zulu`](https://github.com/pterodactyl-china/yolks/tree/master/java/25zulu)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:java_25zulu`
* [`nodejs`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs)
  * [`node12`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/12)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_12`
  * [`node14`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/14)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_14`
  * [`node15`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/15)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_15`
  * [`node16`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/16)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_16`
  * [`node17`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/17)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_17`
  * [`node18`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/18)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_18`
  * [`node20`](https://github.com/pterodactyl-china/yolks/tree/master/nodejs/18)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:nodejs_20`
* [`python`](https://github.com/pterodactyl-china/yolks/tree/master/python)
  * [`python3.7`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.7)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.7`
  * [`python3.8`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.8)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.8`
  * [`python3.9`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.9)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.9`
  * [`python3.10`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.10)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.10`
  * [`python3.11`](https://github.com/pterodactyl-china/yolks/tree/master/python/3.11)
    * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/yolks:python_3.11`

### 安装镜像

* [`alpine-install`](https://github.com/pterodactyl-china/yolks/tree/master/installers/alpine)
  * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/installers:alpine`

* [`debian-install`](https://github.com/pterodactyl-china/yolks/tree/master/installers/debian) (该镜像暂时不支持 `linux/arm64`)
  * `registry.cn-shanghai.aliyuncs.com/pterodactyl-china/installers:debian`
