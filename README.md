## ✨ Neovim


## ⚡ Setup

### ⚙️ Requirements


### 💻 Installation

To install `Custom Neovim` clone the repo and setup the symlink

```bash
git clone https://github.com/FQ21176/nvim
```

On Linux and Mac

```bash
ln -sfnv $PWD/nvim $HOME/.config/nvim
```

On Windows Powershell

```powershell
New-Item -ItemType SymbolicLink -Path "$env:LOCALAPPDATA\nvim" -Target "$PWD\nvim" -Force
```

## 🚀 Usage



### 📦 Plugins

To add new plugins add it to the [plugins list](./lua/plugins/list.lua)

For plugin configs you can place them in these folders based on the functionality:

- [lang](./lua/plugins/lang/): Plugins related to language features, completions, lsp, debugging etc.
- [tools](./lua/plugins/tools/): General purpose tool plugins that aid in the editing experience.
- [ui](./lua/plugins/ui/): Cosmetic plugins that make neovim pretty.

### ⌨️ Keybindings

If you want to change functionality of a core keybinding, edit [core/keys](./lua/core/keys.lua)

To add new keybindings visit the [which-key config](./lua/plugins/tools/which-key.lua)

### 🎨 User Configs


#### 🤖 Auto Install

By default nvim2k will auto install a set of LSP servers and null-ls sources using mason, if you want to disable it make sure to add the following to your user module.

```lua
-- lua/user/init.lua
local user = {
    auto_install = true,
}

return user
```

To setup and access other user options you can use the `get_user_config(key, default)` method in `lib.util`

Example: `local auto_install = require('lib.util').get_user_value('auto_install', true)`

## 🧑‍💻 Behind The Code

I have been using vim/neovim for 7+ years now, I wanted to share my config for everyone to use

