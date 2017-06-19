# INSTALL GUIDE

## Common
```bash
cd ~
git clone https://github.com/ybbarng/vim.git .vim
mv .vimrc .vimrc.backup
ln -s .vim/rc/vimrc .vimrc
cd .vim
git submodule init
git submodule update --remote
# cd bundle/Vundle.vim
# git checkout master
# git pull origin master
vim
```

```vim
:PluginUpdate
```

## NeoVim on Windows10
Do git clone https://github.com/ybbarng/vim.git vimfiles in %USERPROFILE%
Copy vimfiles\rc\vimrc to %USERPROFILE%\AppData\Local\nvim\ginit.vim
Copy vimfiles\colors to %USERPROFILE%\AppData\Local\nvim\
Edit rtp directory in ginit.vim
Do Common
