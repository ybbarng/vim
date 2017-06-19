# INSTALL GUIDE

```bash
cd ~
git clone http://github.com/ybbarng/vim.git .vim
mv .vimrc .vimrc.backup
ln -s .vim/rc/vimrc .vimrc
cd .vim
git submodule init
git submodule update --remote
cd bundle/Vundle.vim
git checkout master
git pull origin master
vim
```

```vim
:PluginUpdate
```
