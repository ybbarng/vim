# INSTALL GUIDE

```bash
cd ~
git clone http://github.com/ybbarng/vim .vim
mv .vimrc .vimrc.backup
ln -s .vim/rc/vimrc .vimrc
cd .vim
git submodule init
git submodule update
vim
```

```vim
:PluginUpdate
```
