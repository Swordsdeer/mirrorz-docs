## 使用方法

使用以下命令启用 bazel-apt 仓库

<tmpl z-lang="bash">
{{sudo}}apt install apt-transport-https curl gnupg
curl -fsSL https://bazel.build/bazel-release.pub.gpg | {{sudo}}gpg --dearmor -o /usr/share/keyrings/bazel-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/bazel-archive-keyring.gpg] {{endpoint}} stable jdk1.8" | {{sudo}}tee /etc/apt/sources.list.d/bazel.list
</tmpl>

使用以下命令安装 bazel

<tmpl z-lang="bash">
{{sudo}}apt update && {{sudo}}apt install bazel
</tmpl>
