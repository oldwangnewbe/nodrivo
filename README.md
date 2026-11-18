# Nodrivo

Nodrivo 授权版的官方二进制发行仓库。

本仓库仅提供一键安装脚本和经过签名、校验的 Release 制品，不包含 Nodrivo 源码、授权中心源码、授权记录或签名私钥。

## 一键安装

支持使用 systemd 的 Linux amd64 与 arm64 服务器。请以 root 权限运行：

```bash
curl -fsSL https://raw.githubusercontent.com/oldwangnewbe/nodrivo/main/distribution/install.sh | sudo bash
```

安装器会从本仓库下载最新授权版，校验 SHA-256 后完成安装。首次安装会进入交互式配置；未激活时为 5 用户基础版，之后可在面板的“版本与授权”页面激活许可证。
新安装默认连接 `https://lisence.nodrivo.com` 授权中心；旧授权域名暂时保留给已安装版本兼容使用。

## 安装指定版本

例如安装授权版 v1.3.9：

```bash
curl -fsSL https://raw.githubusercontent.com/oldwangnewbe/nodrivo/main/distribution/install.sh | sudo env SBP_VERSION=v1.3.9 bash
```

v1.3.9 Release 同时包含完整面板和轻量 Node 的签名制品。通过中心面板“添加服务器”生成的命令会为新服务器安装同版本轻量 Node；Node 不需要单独授权码，也不提供管理网页。完整面板可管理自己的域名证书及 HTTPS 登录入口。无域名的轻量 Node 可以直接使用 IP 安装，由中心验证节点的固定证书。

## 许可

Nodrivo 为专有软件。本仓库公开发行不代表开放源码；下载、使用和再分发限制见 [LICENSE](LICENSE)。第三方组件仍遵循各自许可证。
