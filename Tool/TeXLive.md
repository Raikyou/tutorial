\# 1. 安装

\#\#\# 1.1 网络文件安装

\`\`\` 

wget https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/install-tl-unx.tar.gz

tar -xzf install-tl-unx.tar.gz

cd install-tl-\*

sudo ./install-tl -repository https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/tlnet/

\`\`\`

\#\#\# 1.2 ISO 安装

\`\`\` 

wget https://mirrors.tuna.tsinghua.edu.cn/CTAN/systems/texlive/Images/texlive\[0-9\].iso

sudo mount -o loop texlive\[0-9\]\{4\}.iso /mnt

cd /mnt 

\# txt 模式安装

sudo ./install-tl

\#\#\#\#\#\#\#\#\# 图形界面安装 \#\#\#\#\#\#\#\#\#\#

\# 安装 gui 支持包

\# sudo apt-get install perl-tk

\# 进入gui 安装界面 

\# sudo ./install-tl -gui

\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#

\# 安装完后卸载 ISO

sudo umount /mnt

\`\`\`



\# 2 配置环境变量

打开 \`~/.bashrc\` 文件，添加以下内容：

\`\`\`

export PATH=/usr/local/texlive/2018/bin/x86\_64-linux:$PATH

export MANPATH=/usr/local/texlive/2018/texmf-dist/doc/man:$MANPATH

export INFOPATH=/usr/local/texlive/2018/texmf-dist/doc/info:$INFOPATH

\`\`\`

使配置快速生效：

\`\`\` 

source ~/.bashrc

\`\`\`

使开启 sudo 模式后路径仍然可用：

\`\`\`

sudo visudo

\`\`\`

找到如下一段代码

\`\`\`

Defaults        secure\_path="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"

\`\`\`

替换为

\`\`\`

Defaults        secure\_path="/usr/local/texlive/2018/bin/x86\_64-linux:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin"

\`\`\`



\# 3. 字体设置

要在整个系统中使用 TeX 字体，还需要将 TeX 自带的配置文件复制到系统目录下。命令行中执行

\`\`\`

sudo cp /usr/local/texlive/2018/texmf-var/fonts/conf/texlive-fontconfig.conf /etc/fonts/conf.d/09-texlive.conf

sudo fc-cache -fv           \# 刷新字体数据库

\`\`\`



\# 4. 检查

\#\#\# 基本命令

\`\`\`

tlmgr --version

pdftex --version

xetex --version

luatex --version

\`\`\`

\#\#\# 包管理器

\`\`\`

\# 待更新包

sudo tlmgr update --list

\# 更新 tlmgr 自身和全部包

sudo tlmgr update --self --all

\`\`\`

可以添加 -repository url 参数来自定义距离最近 CTAN 镜像



\# 5. 测试 Hello World

编写 test.tex

\`\`\`

% test.tex

\documentclass\[UTF8\]{ctexart}

\begin{document}

欢迎来到 \TeX{} 世界！

\end{document}

\`\`\`

用 xelatex 或 lualatex 编译生成 PDF :

\`\`\`

xelatex test

lualatex test

\`\`\`

编译得到的 PDF 文件如果显示正常，则说明 TeX Live 基本工作正常。



\# 6. 安装编辑器

\#\#\# 6.1 TexWork 



在 windows 系统中安装 TexLive 后自带 TexWork，在 Linux 系统中需要额外安装。



如果直接从源 \`apt\` 安装 TexWork，则会重新安装 TeX 的依赖，使已安装的 TeXLive 失效，因此应添加参数：

\`\`\`

sudo aptitude install texworks --without-recommends

\`\`\`

\#\#\# 6.2 TexStudio

\`\`\`

sudo apt install texstudio 

\`\`\`



\# Reference

1. Karl Berry. 江疆 译. 2018:04. \*\[TEX Live 指南—2018\]\(http://tug.org/texlive/doc/texlive-zh-cn/texlive-zh-cn.pdf\)\*

2. stone-zeng. 2018:05. \*\[在 Ubuntu 中安装 TeX Live 2018\]\(https://stone-zeng.github.io/fduthesis/2018-05-13-install-texlive-ubuntu/\)\*

3. 始终. 2014:09. \*\[一份其实很短的 LaTeX 入门文档\]\(https://liam0205.me/2014/09/08/latex-introduction/\)\*



