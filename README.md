# Omarchy dotfiles

The next are my dotfiles for Omarchy for a MacBook PRO Intel i9.

## Fix Visual Code

> NOTE: First check if the command `code` without disabling gpu works, if not then add the `--disable-gpu`.

Add `--disable-gpu` to the `code.desktop` file in `~/.local/share/applications/`.

```
[Desktop Entry]
Name=Visual Studio Code
Comment=Code Editing. Redefined.
GenericName=Text Editor
Exec=/usr/bin/code --disable-gpu %F
Icon=visual-studio-code
Type=Application
StartupNotify=false
StartupWMClass=Code
Categories=TextEditor;Development;IDE;
MimeType=application/x-code-workspace;
Actions=new-empty-window;
Keywords=vscode;

[Desktop Action new-empty-window]
Name=New Empty Window
Name[cs]=Nové prázdné okno
Name[de]=Neues leeres Fenster
Name[es]=Nueva ventana vacía
Name[fr]=Nouvelle fenêtre vide
Name[it]=Nuova finestra vuota
Name[ja]=新しい空のウィンドウ
Name[ko]=새 빈 창
Name[ru]=Новое пустое окно
Name[zh_CN]=新建空窗口
Name[zh_TW]=開新空視窗
Exec=/usr/bin/code --disable-gpu --new-window %F
Icon=visual-studio-code
```

## Hyprland configurations

Add the next entry at the end to the file `~/.config/hypr/hyprland.conf`

```
source = ~/.config/me-hypr/hyprland.conf
```

[Remove Windows Gaps](https://learn.omacom.io/2/the-omarchy-manual/102/common-tweaks#remove-window-gaps)

## Clojure

Omarchy offers install clojure trhough alt+super+space development menu.

But i installed with:

```
brew install clojure/tools/clojure
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

So I unsinstalled brew and clojure

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
# and delete the line in .bashrc
```

## Cursor

Installed via omarchy

`cp /usr/share/applications/cursor.desktop ~/.local/share/applications/`

Add the --disable-gpu
