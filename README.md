# Installation 

**UBUNTU ONLY**

## Shell

Customizacja shell - zsh

### Zsh and oh-my-zsh

Oh-my-zsh https://github.com/ohmyzsh/ohmyzsh

```sh
sudo apt update

sudo apt install zsh -y

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### powerlevel10k zsh theme

Motyw powerlevel10k dla oh-my-zsh https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh

Wymagania:
* czcionka -nerd https://github.com/tonsky/FiraCode

```sh
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
**NOTE** Plik `.p10k.zsh` zawarty w repo `Czarnowskij/home.git` nadpisuje kofiguracje inicjalną motywu p10k!!

## Tools

### FZF 

FuzzyFinder https://github.com/junegunn/fzf

```sh
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
FZF-git

```sh
#fzf-git
git clone https://github.com/junegunn/fzf-git.sh.git
```

### FD 

fd-find https://github.com/sharkdp/fd

```sh
sudo apt install fd-find
```

**NOTE** Potrzebny link do bin (zawarty w repo `CzarnowskiJ/home.git` -> `.local.bin`)

```sh
# in case 

ln -s /usr/bin/fdfind ~/.local/bin/fd
```

### bat 

bat = lepszy cat https://github.com/sharkdp/bat

```sh
sudo apt install bat

#Motyw wykorzystwany przez bat w pliku ~/.zshrc

mkdir -p "$(bat --config-dir)/themes"

cd "$(bat --config-dir)/themes"

curl -O https://raw.githubusercontent.com/folke/tokyonight.nvim/main/extras/sublime/tokyonight_night.tmTheme

bat cache --build
```

**NOTE** Potrzebny link do bin (zawarty w repo `CzarnowskiJ/home.git` -> `.local.bin`)

```sh
# in case 

ln -s /usr/bin/batcat ~/.local/bin/bat
```

### eza 

eza = lepszy ls https://github.com/eza-community/eza/blob/main/INSTALL.md

```sh
sudo apt install -y gpg
sudo mkdir -p /etc/apt/keyrings
wget -qO- https://raw.githubusercontent.com/eza-community/eza/main/deb.asc | sudo gpg --dearmor -o /etc/apt/keyrings/gierens.gpg
echo "deb [signed-by=/etc/apt/keyrings/gierens.gpg] http://deb.gierens.de stable main" | sudo tee /etc/apt/sources.list.d/gierens.list
sudo chmod 644 /etc/apt/keyrings/gierens.gpg /etc/apt/sources.list.d/gierens.list
sudo apt update
sudo apt install -y eza
```

### nvim 
```sh
TODO
```

### Clone this repository 

Repozytorium `CzarnowskiJ\home.git`
* nadpisuje 
	* `p10k.zsh` plik konfiguracyjny dla motywu p10k
	* `.zshrc` plik konfiguracyjny dla zsh (dla dokumentacji zajrzyj do pliku `.zshrc` w repozytorium)
* dodaje linki do `fd` oraz `bat` w `.local\bin`

```sh
git clone --depth 1 https://github.com/CzarnowkiJ/home.git ~/
```

