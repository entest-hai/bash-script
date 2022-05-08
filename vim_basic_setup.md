# Vim basic sestup

### Install neovim 

clone nvim 
```shell
https://github.com/neovim/neovim/releases/tag/v0.7.0
```

### Note before defx

```shell 
export PATH=/home/ec2-user/nvim-linux64/bin:$PATH
```
create configuration for nvim 
```
~/.config/nvim/init.vim 
```

and

```
UpdateRemotePlugins
```

### Install dein

```shell
curl https://raw.githubusercontent.com/Shougo/dein.vim/master/bin/installer.sh > installer.sh
```

```shell
sh ./installer.sh ~/.cache/dein
```

setup dein

```
" Required:
set runtimepath+=/Users/haimtran/.cache/dein/repos/github.com/Shougo/dein.vim

" Required:
call dein#begin('/Users/haimtran/.cache/dein')

" Let dein manage dein
" Required:
call dein#add('/Users/haimtran/.cache/dein/repos/github.com/Shougo/dein.vim')
```

open vim and run

```
: call dein#install()
```

### Configure vimrc

```
/.config/nvim/init.vim
~/.vim/vimrc
```
