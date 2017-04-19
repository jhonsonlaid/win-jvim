## gvim for windows
---

1. [vim下载](http://www.vim.org/download.php#pc)：python的同学，要注意自己是32位的python还是64位的，下载**同样位数**的vim，否则``jedi-vim``等插件不能正常使用。要想使用w0rp-ale插件需要8.0或以上版本。

2. [安装gvim基本教程](http://www.huangdc.com/421)：包括vim下载安装和vundle的安装，和NERDTree的安装。**环境变量**，创建VIM变量，值为
```
E:\ProgramFiles\Vim\
```

![](http://www.jhonsonlai.com/media/markdownx/img/5c2dd2bd-e2ed-40a1-bfe9-305ef131eb44.PNG)

3. [vundle for windows官方教程](https://github.com/VundleVim/Vundle.vim/wiki/Vundle-for-Windows)：需要安装git和curl，方便安装和管理vim的各种插件，**[常用命令](https://github.com/VundleVim/Vundle.vim)**,在gvim打开情况下，
```
安装插件:BundleInstall
更新插件:BundleUpdate
清除不再使用的插件:BundleClean
列出所有插件:BundleList
查找插件:BundleSearch
```
4. [vim打开中文文件乱码解决](http://lxs647.iteye.com/blog/1994010)

5. [YouCompleteMe官方教程](https://github.com/Valloric/YouCompleteMe#windows)

6. [w0rp/ale](https://github.com/w0rp/ale)：类似syntastic的异步检测版本，无卡顿, 但只支持8.0以上。按照链接安装完以后没有报错，但不能正常运行的原因可能是没有安装相关语言的语法检查包，比如python要安装**flake8**或者**pylint**，更多依赖包在连接里有相关表格。

7. [jedi-vim 安装](https://github.com/davidhalter/jedi-vim)：Python的自动补全，需要预先安装``jedi``.

8.  **``R6034: An application has made an attempt to load the C runtime library incorrectly``问题**
cd到``C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin``文件夹，运行
```
mt.exe -inputresource:"C:\Users\JohnsonLai\Anaconda2\python.exe" -outputresource:"E:\ProgramFiles\Vim\vim80\gvim.exe"
```
即可解决，参考链接[1](http://stackoverflow.com/questions/9764341/runtime-error-with-vim-omnicompletion)、[2](https://social.msdn.microsoft.com/Forums/windowsdesktop/en-US/89419579-0097-45b3-b983-b8c24d0ff538/where-do-i-get-mtexe?forum=windowssecurity)、[3](https://github.com/ivanov/vim-ipython/issues/20)。