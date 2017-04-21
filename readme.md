## 64bit-gvim8.0 for windows

![](http://i.imgur.com/rkgpGFY.png)

## Install 
 1. Install [Git and Curl](https://github.com/VundleVim/Vundle.vim/wiki/Vundle-for-Windows)
 
 2. ``git clone`` to local directory. click ``vim80/install.exe``, choose d(do it). Add Path Variable, like
```
E:\ProgramFiles\Vim\
```
![](http://www.jhonsonlai.com/media/markdownx/img/5c2dd2bd-e2ed-40a1-bfe9-305ef131eb44.PNG)

 3. Install Vundle
```
$ cd vimfiles/bundle/
$ git clone https://github.com/VundleVim/Vundle.vim
```

 4.  open gvim and type ``:BundleInstall``, install all plugin
 
 5.  64-bit python([Anaconda](https://mirrors.tuna.tsinghua.edu.cn/anaconda/archive/) is recommended)
 
 6. ``pip install flake8`` for [w0rp/ale](https://github.com/w0rp/ale)
 7. ``pip install jedi`` for [jedi-vim](https://github.com/davidhalter/jedi-vim)

## FAQ

  * **``R6034: An application has made an attempt to load the C runtime library incorrectly``**
go to ``C:\Program Files (x86)\Microsoft SDKs\Windows\v7.0A\Bin``，type
```
mt.exe -inputresource:"C:\Users\JohnsonLai\Anaconda2\python.exe" -outputresource:"E:\ProgramFiles\Vim\vim80\gvim.exe"
```
Reference: [stackoverflow](http://stackoverflow.com/questions/9764341/runtime-error-with-vim-omnicompletion)、[microsoft-forum](https://social.msdn.microsoft.com/Forums/windowsdesktop/en-US/89419579-0097-45b3-b983-b8c24d0ff538/where-do-i-get-mtexe?forum=windowssecurity)、[vim-ipython-issue](https://github.com/ivanov/vim-ipython/issues/20)。
