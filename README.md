1. Instalacja ZSH (shella alternatywnego do basha)
```
$ sudo apt update
$ sudo apt install zsh
```
2. Instalacja oh-my-zsh (pozwalającego na ustawianie tematów i innych fajnych rzeczy w ZSH):
```
$ sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
3. Instalacja potrzebnych czcionek (wg https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k):
    1. Pobrać czcionki:
       1. https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
       2. https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf
       3. https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf
       4. https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20Italic.ttf
    2. Na każdą czcionkę kliknąć dwa razy. Powinna się pojawić możliwość instalacji. Jeśli jedna z czcionek się nie instaluje to nie szkodzi - to jest jakiś bug ale nic się potem nie psuje.
    3. Czcionki (MesloLGS NF) ustawiamy we wszyskich terminalach których będziemy używać (gnome terminal, terminal wbudowany w vscode, terminal wbudowany w pycharma etc). Dokładniejsze instrukcje tu: https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k
4. Instalujemy temat (powerlevel10k) do oh-my-zsh:
   1. Wykonujemy `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
   2. W pliku `~/.zshrc` znajdujemy miejsce gdzie jest ustawiana zmienna `ZSH_THEME`. Zmieniamy tę linijkę na `ZSH_THEME="powerlevel10k/powerlevel10k"`
5. Otwieramy nowe okno terminala. Powinniśmy być teraz spytani o to jak chcemy, żeby nasz shell wyglądał.