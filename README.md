# Installation 

## Zsh and oh-my-zsh

```sh
sudo apt update

sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

## powerlevel10k zsh theme


```sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

## FZF 

```sh
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install

# Set up fzf key bindings and fuzzy completion
source <(fzf --zsh)
```

```sh
#fzf-git
git clone https://github.com/junegunn/fzf-git.sh.git
```

## FD 

```sh
sudo apt install fd-find
```

## bat 

```sh
sudo apt install bat

mkdir -p "$(bat --config-dir)/themes"

cd "$(bat --config-dir)/themes"

curl -O https://raw.githubusercontent.com/folke/tokyonight.nvim/main/extras/sublime/tokyonight_night.tmTheme

bat cache --build
```

## eza
```sh
sudo apt install -y gpg
sudo mkdir -p /etc/apt/keyrings
wget -qO- https://raw.githubusercontent.com/eza-community/eza/main/deb.asc | sudo gpg --dearmor -o /etc/apt/keyrings/gierens.gpg
echo "deb [signed-by=/etc/apt/keyrings/gierens.gpg] http://deb.gierens.de stable main" | sudo tee /etc/apt/sources.list.d/gierens.list
sudo chmod 644 /etc/apt/keyrings/gierens.gpg /etc/apt/sources.list.d/gierens.list
sudo apt update
sudo apt install -y eza
```

## nvim 
```sh
TODO
```

## Clone this repository 
```sh
TODO
```

