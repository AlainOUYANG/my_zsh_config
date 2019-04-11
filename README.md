# iTerm2 外观配置

前几天在使用 iTerm2 的时候，发现配色很久没有换过，慢慢已经看腻了，于是决定重新进行外观配置。步骤如下：

**Prerequisite:** Homebrew，[下载](https://brew.sh/index_zh-cn)

## 逐步配置过程
1. 安装 [iTerm2](https://www.iterm2.com/)

	iTerm2 比 mac 自带的 Terminal 好很多，关于两者的比较，网上已经有众多讨论，在此不再赘述。

2. 安装 zsh

	```bash
	brew install zsh
	```

	[这里](https://rick.cogley.info/post/use-homebrew-zsh-instead-of-the-osx-default/)有一篇非常好的讲解如何安装 zsh 的文章。
3. 安装 [oh-my-zsh](https://ohmyz.sh) 插件

	![](https://ohmyz.sh/img/OMZLogo_BnW.png)

	复制这一行到你的命令行窗口，然后静静等待它运行完毕就可以了：

	```bash
	sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
	```
4. 为 oh-my-zsh 安装 [powerlevel9k](https://github.com/bhilburn/powerlevel9k) 主题

	在命令行窗口运行这一行代码：
	```bash
	git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
	```
5. 安装字体

	在 [Nerd Font](https://nerdfonts.com/#downloads) 网站找到 Meslo 这个字体，下载解压。

	打开「字体册」这个 App，将解压好的字体全部拖进去，Mac 会自动为你安装好所有的字体。

	打开 iTerm2，打开 Preference，选择 Profile，选一个你自己的 Profile（默认是 Default），选择 Text 栏，在 Font 中选择刚刚安装的 Meslo 字体（注意这里应该是 Nerd Font Complete），调整适合自己的字体大小。选号字体之后，勾选「Use a different font for non-ASCII text」和「Anti-aliased」，之后会出现「Non-ASCII Font」这个选项，点击选择 Melso 字体，同样勾选「Anti-aliased」。
	
	![](https://ws3.sinaimg.cn/large/006tNc79gy1g1z4jy6pysj319b0u07ko.jpg)
6. 为 iTerm2 安装 Material Design Theme

	根据 [Material Design Theme](https://github.com/MartinSeeler/iterm2-material-design) 进行下载安装。
7. 为 zsh 安装两个额外的插件
- 语法高亮：
	```bash
	git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting
	```
- 自动建议：
	```bash
	git clone https://github.com/zsh-users/zsh-autosuggestions $ZSH_CUSTOM/plugins/zsh-autosuggestions
	```
8. 替换 .zshrc 文件

	去我的 [Github](https://github.com/AlainOUYANG/my_zsh_config) 下载 .zshrc 文件，复制第 89 行（包含）之后的内容，粘贴到你的 .zshrc 中去。

最终效果：
![](https://ws2.sinaimg.cn/large/006tNc79gy1g1z5ul36zgj31b80rudly.jpg)
