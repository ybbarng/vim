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
cd %USERPROFILE%
git clone https://github.com/ybbarng/vim.git vimfiles
Copy vimfiles\rc\vimrc to %USERPROFILE%\AppData\Local\nvim\init.vim
Copy vimfiles\rc\ginit.vim to %USERPROFILE%\AppData\Local\nvim\ginit.vim
Copy vimfiles\colors to %USERPROFILE%\AppData\Local\nvim\colors
Edit rtp directory in init.vim
Do Common

### Patch vim-airline
Append ` && !has('nvim')` on the line of definition of s:is_win32term in bundle\vim-airline\autoload\airline\highlighter.vim
