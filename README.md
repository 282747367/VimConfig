## VIM
说起配置Vim，首先要知道三个配置文件：vimrc，gvimrc和exrc。这些配置文件的位置油Vim的安装位置和操作系统决定。

vimrc

       vimrc是Vim最主要的配置文件，它有两个版本：全局版本（global）和用户版本（personal）。Michael建议修改用户版本。全局vimrc文件在Vim的安装目录中，我的电脑是Mac，所以其路径是

/usr/share/vim/vimrc

       假如你不知道全局vimrc的位置，可以打开Vim，在普通模式（Normal）下输入下面的命令得到它的位置：

echo  $VIM（注意大小写）

       用户版本的vimrc文件在当前用户的主目录下，主目录的位置依赖于操作系统。Mac下的用户vimrc文件路径为：

/Users/用户名/.vimrc（文件名前面的”.”代表这个文件是隐藏文件）

       你可以在Vim的普通模式下输入下面的命令，查找用户主目录的位置：

:echo  $HOME

       但是Mac下默认是没有用户vimrc的，所以需要你自己创建一个。

       不管怎么改用户版的vimrc文件，其中的内容都是是覆盖在全局vimrc文件中设置的内容，这就意味着你可以不需要去改变全局vimrc文件来进行配置vim，只需要修改用户vimrc文件。

# VIM Command
先敲入数字，然后敲入|，光标跳到指定列

# NERDTree
文件浏览器：NERDTree

项目地址：

https://github.com/scrooloose/nerdtree

[注意]必须预安装pathogen.vim，同样是参见该网页。

安装方法：

    进入.vim/bundle目录
    执行git clone git://github.com/scrooloose/nerdtree.git
    下载完成后，在bundle下会多出一个nerdtree的文件夹，所有相关插件都在该文件夹下
    在Vim中运行:Helptags来生成NERDTree的在线帮助tags
    (不要听网上说的那些将文件拷来拷去的，没有用)

# git config
Git 提供了一个叫做 git config 的工具（译注：实际是 git-config 命令，只不过可以通过 git 加一个名字来呼叫此命令。），专门用来配置或读取相应的工作环境变量。而正是由这些环境变量，决定了 Git 在各个环节的具体工作方式和行为。这些变量可以存放在以下三个不同的地方：

   * /etc/gitconfig 文件：系统中对所有用户都普遍适用的配置。若使用 git config 时用 --system 选项，读写的就是这个文件。
   * ~/.gitconfig 文件：用户目录下的配置文件只适用于该用户。若使用 git config 时用 --global 选项，读写的就是这个文件。
   * 当前项目的 Git 目录中的配置文件（也就是工作目录中的 .git/config 文件）：这里的配置仅仅针对当前项目有效。每一个级别的配置都会覆盖上层的相同配置，所以 .git/config 里的配置会覆盖 /etc/gitconfig 中的同名变量。

# ssh
sudo apt-get install openssh-server openssh-client


# Path List
1-Mac
vimrc: /usr/share/vim/vimrc (global); ~/.vimrc (user, create by yourself)
bashrc(for bash): /etc/bashrc, /etc/bashrc_Apple_Terminal (global); ~/.bash_rc (user create)
profile(for other shell): /etc/profile (global); ~/.profile (user create)
bash-completion: /usr/local/etc/bash_completion /usr/local/opt/bash-completion/etc/bash_completion [Be careful of 'bash-' and 'bash'_]
git-completion: /usr/local/etc/bash_completion.d/git-completion.bash /usr/local/opt/bash-completion/etc/bash_completion.d/git-completion.bash
