# Vim

47:30


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
# Install Neovim
sudo apt update
sudo apt install neovim

# Make config file
~$ mkdir .config
~$ cd .config
~/.config$ mkdir nvim
~/.config$ cd nvim/
~/.config/nvim$ nvim init.vim
```


<!--
Basic directory for config setting
$ nvim ~/.config/nvim/init.vim

-->
