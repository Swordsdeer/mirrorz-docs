## 自动安装方式

Docker 提供了一个自动配置与安装的脚本，支持 Debian、RHEL、SUSE 系列及衍生系统的安装。请注意，Docker 官方不建议在生产环境使用此脚本安装 Docker CE。

以下内容假定

- 您为 root 用户，或有 sudo 权限，或知道 root 密码；
- 您系统上有 curl 或 wget

<tmpl z-lang="bash">
export DOWNLOAD_URL="{{endpoint}}"
# 如您使用 curl
curl -fsSL https://raw.githubusercontent.com/docker/docker-install/master/install.sh | {{#sudo}}sudo -E {{/sudo}}sh
# 如您使用 wget
wget -O- https://raw.githubusercontent.com/docker/docker-install/master/install.sh | {{#sudo}}sudo -E {{/sudo}}sh
</tmpl>
