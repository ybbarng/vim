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


### Windows10의 NeoVim-QT에서 잘 동작하도록 vim-airline 패치
[이 커밋](https://github.com/vim-airline/vim-airline/commit/57e564b22748e5ffcd7a4595864e0bff45fa55a0)이 패치되면 잘 해결될 것으로 보인다.
지금은 저 커밋에 따라서 `bundle\vim-airline\autoload\airline\highlighter.vim`의 s:is_win32term을 다음과 같이 변경한다.
```vim
let s:is_win32term = (has('win32') || has('win64')) &&
                   \ !has('gui_running') &&
                   \ (empty($CONEMUBUILD) || &term !=? 'xterm') &&
                   \ !(exists("+termguicolors") && &termguicolors)
```
