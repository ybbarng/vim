# INSTALL GUIDE

```bash
cd ~
git clone http://github.com/ybbarng/vim.git .vim
mv .vimrc .vimrc.backup
ln -s .vim/rc/vimrc .vimrc
cd .vim
git submodule init
git submodule update
cd bundle/Vundle.vim
git pull origin master
vim
```

```vim
:PluginUpdate
```
