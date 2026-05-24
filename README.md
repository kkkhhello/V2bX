- `install.sh`: 一键安装脚本，默认安装 `v0.4.0`。
- `V2bX.sh`: 安装后的管理命令脚本，会从本仓库更新自身和重新安装。
- `initconfig.sh`: 首次安装时可选的配置生成脚本。
- `release-assets/v0.4.0/`: 安装所需的 Linux 二进制 zip 包。
- `source/V2bX-v0.4.0.tar.gz`: v0.4.0 源码备份，不参与安装。
- `SHA256SUMS`: 已下载文件的 SHA256 校验值。

## 一键安装命令

上传完成后，在服务器 root 用户下执行：

```bash
bash <(curl -Ls https://raw.githubusercontent.com/kkkhhello/V2bX/main/install.sh) v0.4.0
```

也可以用下载安装脚本的方式：

```bash
curl -L -o install.sh https://raw.githubusercontent.com/kkkhhello/V2bX/main/install.sh
bash install.sh v0.4.0
```

## 如果仓库名或分支不同

脚本默认读取：

```text
GITHUB_USER=kkkhhello
GITHUB_REPO=V2bX
GITHUB_BRANCH=main
FIXED_VERSION=v0.4.0
```

如果你的仓库不是 `kkkhhello/V2bX`，可以改 `install.sh` 和 `V2bX.sh` 顶部的这些变量，或者安装时临时指定：

```bash
GITHUB_REPO=你的仓库名 bash <(curl -Ls https://raw.githubusercontent.com/kkkhhello/你的仓库名/main/install.sh) v0.4.0
```

