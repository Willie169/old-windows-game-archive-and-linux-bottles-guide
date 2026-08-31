# old-windows-game-archive-and-linux-bottles-guide

This repo serves for two purposes:
- archiving some old Windows games and
- providing guide for Linux to run them in Bottles.

## Archive

In this repo, some old Windows games are archived in [`archive`](archive) folder. They are made solely for archiving purpose are subjected to their own copyright status.

By downloading or cloning them you agree that you have obtained the right to obtain them and that in no event shall the repo owner be liable for any claim, damages or other liability, whether in an action of contract, tort or otherwise, arising from, out of or in connection with the archive or the use or other dealings in the archive.

## Windows

1. Read [Archive](#archive).
2. The games can be run directly in Windows. Just download them or clone the repo: (git required)
    ```
    git clone --depth=1 https://github.com/Willie169/old-windows-game-archive-and-linux-bottles-guide.git
    ```
    and execute them. If you encountered broken font rendering or other problems and found a solution, it is encouraged to report to this repo's issue or make a pull request about it.

## Linux Bottles Guide

1. Read [Archive](#archive).
2. Clone this repo: (git required)
    ```
    git clone --depth=1 https://github.com/Willie169/old-windows-game-archive-and-linux-bottles-guide.git
    ```
3. If you haven't install Flatpak, install it: (Ubuntu/Debian for example)
    ```
    sudo apt update
    sudo apt install flatpak -y
    ```
    add Flathub:
    ```
    sudo flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo
    ```
    and reboot:
    ```
    sudo reboot
    ```
4. Install Bottles:
    ```
    flatpak install flathub com.usebottles.bottles
    ```
5. Launch Bottles:
    ```
    flatpak run com.usebottles.bottles
    ```
6. If `(ERROR) Unable to load libGLX_nvidia.so.0`, run
    ```
    flatpak update -y
    ```
    and launch Bottles again.
7. Click plus sign in the top left corner to Create New Bottles.
8. Give it a name, e.g., Games.
9. Select Gaming.
10. If the Runner shows `mcsoda-*`, change it to `protosoda-*`.
11. Click Create.
12. Click the Bottle.
13. Click Browse beside Browse C:/ drive.
14. Move the games you want to execute from the cloned repo into it. One Bottle can contain multiple games.
15. For each .exe file, click Add Shortcuts..., select it.
16. For [2D絕對武力CS](archive/2D絕對武力CS), [Pacman](archive/Pacman), [Same Game for Windows](archive/Same%20Game%20for%20Windows), [Mashmaro](archive/Mashmaro), and [企鵝丟冰塊](archive/企鵝丟冰塊), click three dots by the shortcut, click Change Launch Options > Command Arguments, and paste
    ```
    LC_ALL="zh_TW.UTF-8" %command%
    ```
17. For [スクルドのバグ退治ゲーム](archive/スクルドのバグ退治ゲーム), click three dots by the shortcut, click Change Launch Options > Command Arguments, and paste
    ```
    LC_ALL="ja_JP.UTF-8" %command%
    ```
18. For [スクルドのバグ退治ゲーム](archive/スクルドのバグ退治ゲーム), [企鵝丟冰塊](archive/企鵝丟冰塊), and any  other game if you encounter broken font rendering, go to Options > Dependencies, check cjkfonts, and click Install Selected.
19. If you still encounter broken font rendering, go to Options > Dependencies, check allfonts, and click Install Selected.
20. Run the game shortcut listed in Programs.

## License

This project is licensed under [MIT License](license.txt).

