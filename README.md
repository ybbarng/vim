# INSTALL GUIDE

## Unix
```bash
cd ~
git clone https://github.com/ybbarng/vim.git .vim
mv .vimrc .vimrc.backup
ln -s .vim/rc/vimrc .vimrc
cd .vim
vim
```

## NeoVim on Windows10
cd %USERPROFILE%
git clone https://github.com/ybbarng/vim.git vimfiles
Copy vimfiles\rc\vimrc to %USERPROFILE%\AppData\Local\nvim\init.vim
Copy vimfiles\rc\ginit.vim to %USERPROFILE%\AppData\Local\nvim\ginit.vim
Copy vimfiles\colors to %USERPROFILE%\AppData\Local\nvim\colors
Copy vimfiles\autoload to %USERPROFILE%\AppData\Local\nvim\autoload
plugin_path를 OS에 맞게 변경


## Install Plugins
```vim
:PlugUpdate
```


## plugin_path
* Unix: ~/.vim/plugged
* Unix NeoVim: ~/.local/share/nvim/plugged
* Windows: $USERPROFILE/vimfiles/plugged


## plug_path
* Unix: ~/.vim/autoload
* Unix NeoVim: ~/.local/share/nvim/site/autoload
* Windows: $USERPROFILE/vimfiles/autoload
* Windows NeoVim: $USERPROFILE/AppData/Local/nvim/autoload


### Patch vim-airline
Append ` && !has('nvim')` on the line of definition of s:is_win32term in bundle\vim-airline\autoload\airline\highlighter.vim
