# Vim

Useful Material: https://docs.oracle.com/cd/E19683-01/806-7612/editorvi-43/index.html


## [0] Useful Pluggin
```bash
have a look at init.vim file
```



## [1]

```bash
i # insert mode
o # insert mode from the next line
I # insert mode from the first line
A # insert mode from the last line

dd # delete the line
D  # delete the characters next to the cursor
cc # delete and activate insert mode at the same time
C  # delete the characters next to the cursor then activate insert mode
ciw# delete the word and start inserting
dG # delete the whole text
dw # delete the word
yy # copy the line
yiw# copy the word
p  # paste the line
r  # replace the word on the cursor

u        # undo
Ctrl + R # redu

v # visual mode to drag 

[Moving]
NUM + [j/k] # move the lines with the gap of NUM
b           # move backward
w           # move forward

0           # move to beginning
$           # move to the last point
%           # jump between bracket
```


## [] Make Vim Beautiful
edit vimrc
```bash
vi ~/.vimrc
```

## Install Neovim
```bash
Best Guide Video: https://www.youtube.com/watch?v=JWReY93Vl6g&t=179s

# Install Neovim
sudo apt update
sudo apt install neovim

`supplement thing: ~/.config/nvim$`
sudo apt install git
sudo apt install exuberant-ctags
sudo apt install nodejs
sudo apt install npm

# Make config file (keep in mind our directory is in ~)
~$ mkdir .config
~$ cd .config
~/.config$ mkdir nvim
~/.config$ cd nvim/
~/.config/nvim$ nvim init.vim

# Plugins setting
1. go to this repository: https://github.com/junegunn/vim-plug
~/.config/nvim$ PASTE_HERE

2. We can add plugins into our init.vim file between "call plug#begin()" and "call plug#end()"

3. After add Plugins, type ":PlugInstall" in init.vim file

# coc setting 
1. find plugged folder
I found it from "~/.local/share/nvim/plugged/coc.nvim$"

2. ~/.local/share/nvim/plugged/coc.nvim$ sudo npm install -g yarn

3. ~/.local/share/nvim/plugged/coc.nvim$ yarn install

  [Encountered Problems]
  (base) chicago@chicago-com:~/.local/share/nvim/plugged/coc.nvim$ yarn install
  yarn install v1.22.17
  [1/5] Validating package.json...
  error coc.nvim-master@0.0.80: The engine "node" is incompatible with this module. Expected version ">=12.12.0". Got "10.19.0"
  error Found incompatible module.
  info Visit https://yarnpkg.com/en/docs/cli/install for documentation about this command.
  
  [Solution]:Node 업데이트
  $ sudo npm cache clean -f # 강제캐시삭제
  $ sudo npm install -g n # n 모듈 설치
  $ sudo n stable # or sudo n 12.14.0 (버전명)
  $ node -v # 버전 확인


4. ~/.local/share/nvim/plugged/coc.nvim$ yarn build

5. ~/.config/nvim$ nvim init.vim

6. :CocInstall coc-python

etc.
1. For coc setting
~/.config/nvim$ pip3 install jedi
~/.config/nvim$ nvim init.vim

2. When there is an error for :TerminalSplit bash
~/.config/nvim$ python3 -m pip install --user --upgrade pynvim
```

coc cpp: https://tyanjournal.com/tips/neovim-c-ide/


## Install Vim Bindings in Jupyter Noterbook

```bash
1. conda install -c conda-forge jupyter_contrib_nbextensions
2. jupyter contrib nbextension install --user
3. jupyter --data-dir
4. MOVE TO DIRECTORY (/home/kaai/.local/share/jupyter)
5. cd nbextensions
6. ~/.local/share/jupyter/nbextensions$ git clone https://github.com/lambdalisue/jupyter-vim-binding.git
7. ~/.local/share/jupyter/nbextensions$ jupyter nbextension enable jupyter-vim-binding/vim_binding
```


<!--
Basic directory for config setting
$ nvim ~/.config/nvim/init.vim


-->
