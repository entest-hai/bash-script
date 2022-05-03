# Vim basic sestup

### Note before defx

```
pip3 install --user pynvim
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
