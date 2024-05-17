# What it is? 

This is my home dir configuration with all CLI tools that I use. It's created to config my setup from any ubuntu machine I work.  
I have not created any of those tools, I just simply use them because they are great.  

# Content 

## Shell

* Oh-my-zsh 	https://github.com/ohmyzsh/ohmyzsh
* powerlevel10k	https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh  

## Tools
* fzf		https://github.com/junegunn/fzf
* fzf-git	https://github.com/junegunn/fzf-git.sh
* fd-find	https://github.com/sharkdp/fd
* bat		https://github.com/sharkdp/bat
* eza		https://github.com/eza-community/eza
* zsh-autosuggestions	https://github.com/zsh-users/zsh-autosuggestions

## Requirements

* Any -nerd font but I use this: https://github.com/tonsky/FiraCode

# Installation 

## UBUNTU 20.04 and higher ONLY

```sh
git clone https://github.com/CzarnowskiJ/home.git ~/tmp_home_repo
~/tmp_home_repo/scripts/installShell
```
Script is done when you see the Oh My Zsh ASCII art and empty prompt. 
Proceed with:

```sh
~/tmp_home_repo/scripts/installTools
```
Final:

```sh
mv -f ~/tmp_home_repo/.* ~/tmp_home_repo/* ~/
rm -rf ~/tmp_home_repo
source ~/.zshrc
```

Scripts install all tools listed above in **Content** section then:
* overwrite 
	* `p10k.zsh` config file
	* `.zshrc` config file (check the file to see the config of tools) 
* create links to `fd` and `bat` in `.local\bin`

```sh
# in case links don't work
ln -s /usr/bin/fdfind ~/.local/bin/fd
ln -s /usr/bin/batcat ~/.local/bin/bat
```

# Tweaks

### bat tokyonight_night theme

```sh

mkdir -p "$(bat --config-dir)/themes"

cd "$(bat --config-dir)/themes"

curl -O https://raw.githubusercontent.com/folke/tokyonight.nvim/main/extras/sublime/tokyonight_night.tmTheme

bat cache --build
```


### nvim 
```sh
TODO
```
