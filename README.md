# VSCode Settings and Keybinds
## Motivation
To create a neovim-like, keyboard-driven, development experience for VSCode. While recognisably slower than neovim, VSCode has access to a lot more built-in functionality (no dealing with neovim LSPs...). The two parts I enjoyed most from neovim was how uncluttered the screen was and my keybinds from neovim.

## Dependencies: 
- Required extensions
- Fonts:
  - Cousine Nerd Font Mono (default)

## Extensions:
#### Required:
- Vim by vscodevim
#### Themes:
- Intellij C++ Theme (Dark) by Kleysley
#### Extras:
- vscode-pdf by tomoki1207
- Markdown All in One by Yu Zhang
- Jupyter Notebook Packages by Microsoft
- Live Server by Ritwick Dey
- Tailwind Fold by Stivo
#### Interested:
- Periscope (slow previews currently)

## Config VCS Setup
1. Create a `~/.config/vscode/` directory if needed (typical user config directory may depend on your OS).
    ```
    mkdir -p ~/.config/vscode/
    ```
2. Clone this repo into your `~/.config/vscode/` directory (or wherever your .config directory is)
    ```
    git clone git@github.com:ethan-dean/VSCode-Config.git ~/.config/vscode/
    ```
3. **CLOSE** any instances of **VSCode** you have running (it will regenerate settings.json after we delete it if we have any running sessions)
4. Back up(optionally) then delete your current settings.json and keybindings.json files
    ```
    # MacOS
    rm ~/Library/Application\ Support/Code/User/{settings|keybindings}.json
    ``` 
5. Set up a symlink between your `~/.config/vscode/` directory and the VSCode directory
    ```
    # MacOS
    ln -s ~/.config/vscode/settings.json ~/Library/Application\ Support/Code/User/settings.json;
    ln -s ~/.config/vscode/keybindings.json ~/Library/Application\ Support/Code/User/keybindings.json;
    ```