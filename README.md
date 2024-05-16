# Installation 

**UBUNTU ONLY**

```sh
git clone https://github.com/CzarnowskiJ/home.git ~/tmp_home_repo
sudo chmod +x ~/tmp_home_repo/scripts/installShell
~/tmp_home_repo/scripts/installShell
```

Instalacja zakończy się ASCII artem oh my zsh i informacją o pomyślnie zainstalowanym zsh.
Następnie:

```sh
~/tmp_home_repo/scripts/installTools
```
i po zakończeniu działania:

```sh
mv -f ~/tmp_home_repo/.* ~/tmp_home_repo/* ~/
rm -rf ~/tmp_home_repo
source ~/.zshrc
```

Repozytorium `CzarnowskiJ\home.git`
* nadpisuje 
	* `p10k.zsh` plik konfiguracyjny dla motywu p10k
	* `.zshrc` plik konfiguracyjny dla zsh (dla dokumentacji zajrzyj do pliku `.zshrc` w repozytorium)
* dodaje linki do `fd` oraz `bat` w `.local\bin`

# Content

## Shell

Customizacja shell - zsh

### Zsh and oh-my-zsh

Oh-my-zsh https://github.com/ohmyzsh/ohmyzsh


### powerlevel10k zsh theme

Motyw powerlevel10k dla oh-my-zsh https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#oh-my-zsh

Wymagania:
* czcionka -nerd https://github.com/tonsky/FiraCode

**NOTE** Plik `.p10k.zsh` zawarty w repo `Czarnowskij/home.git` nadpisuje kofiguracje inicjalną motywu p10k!!

## Tools

### FZF 

FuzzyFinder https://github.com/junegunn/fzf

FZF-git

### FD 

fd-find https://github.com/sharkdp/fd

**NOTE** Potrzebny link do bin (zawarty w repo `CzarnowskiJ/home.git` -> `.local.bin`)

```sh
# in case 

ln -s /usr/bin/fdfind ~/.local/bin/fd
```

### bat 

bat = lepszy cat https://github.com/sharkdp/bat

```sh

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


### nvim 
```sh
TODO
```
