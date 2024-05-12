# my-zsh-setup

## oh-my-zsh

```shell
https://ohmyz.sh/#install
```

Download

```shell
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## powerlevel10k

```shell
https://github.com/romkatv/powerlevel10k#installation
```

Download

```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

.zshrc

```shell
ZSH_THEME="powerlevel10k/powerlevel10k"
```

Update

```shell
git -C ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k pull
```

## zsh-autosuggestions

```shell
https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md
```

Download

```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

.zshrc

```shell
plugins=(zsh-autosuggestions)
```

## zsh-syntax-highlighting

https://github.com/zsh-users/zsh-syntax-highlighting

### download

```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

.zshrc

```
plugins=( [plugins...] zsh-syntax-highlighting)
```

## zsh-history-substring-search

https://github.com/zsh-users/zsh-history-substring-search

```shell
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```

.zshrc

```
bindkey '^[[A' history-substring-search-up
bindkey '^[[B' history-substring-search-down
```

## zoxide

### usage

```shell
z
z -
zi
z code 3d-pr

z code # press space, then tab

zoxide add code/3d-printer
zoxide query folder -s
zoxide remove /home/bassam/temp
zoxide edit
```

Download

```shell
curl -sS https://raw.githubusercontent.com/ajeetdsouza/zoxide/main/install.sh | bash
```

.zshrc

```sh
eval "$(zoxide init zsh)"
# eval "$(zoxide init --cmd cd zsh)"
```

## All

After omz is installed

```shell
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
```

.zshrc

```shell
ZSH_THEME="powerlevel10k/powerlevel10k"

plugins=(git zsh-autosuggestions zsh-syntax-highlighting zsh-history-substring-search)

# zoxide
eval "$(zoxide init zsh)"

# zsh-history `cat -v`
bindkey '^[[A' history-substring-search-up
bindkey '^[[B' history-substring-search-down
```

## aliases

```shell
alias bat=batcat
alias wtemp="watch -n 1 cat /sys/class/thermal/thermal_zone0/temp"
alias wspeed="watch -n 1 vcgencmd measure_clock arm"
alias getip="curl https://ipinfo.io/ip"
alias up="cd .."
alias l="exa --long --all"
alias chksyslog='cat /var/log/syslog | grep '
alias zshconfig='nano ~/.zshrc'
alias _zshconfig='source ~/.zshrc'
gitlogr='git log --all --graph --decorate --oneline --pretty=format:'\''%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset'\'
alias getip='curl icanhazip.com'
```
