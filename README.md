# gemini-cli

[![Mentioned in Awesome Gemini CLI](https://awesome.re/mentioned-badge.svg)](https://github.com/Piebald-AI/awesome-gemini-cli)

A Neovim plugin to seamlessly integrate the Gemini CLI.

<https://github.com/user-attachments/assets/a40b8bab-9a9c-4654-878e-c6f03577585c>

## Features

- Toggle the Gemini CLI in a vertical split window.
- Automatically checks if the `gemini` CLI is installed on startup.
- Prompts to install the `gemini` CLI if it's missing.
- Sets the `EDITOR` environment variable to `nvim` for the Gemini CLI session, so you can use Neovim to edit files from within Gemini.

## Requirements

- Neovim >= 0.7.0
- [Node.js and npm](https://nodejs.org/) (for the Gemini CLI)

## Installation

### [lazy.nvim](https://github.com/folke/lazy.nvim)

```lua
{
  "jonroosevelt/gemini-cli.nvim",
  config = function()
    require("gemini").setup()
  end,
}
```

### [packer.nvim](https://github.com/wbthomason/packer.nvim)

```lua
use {
  "jonroosevelt/gemini-cli.nvim",
  config = function()
    require("gemini").setup()
  end,
}
```

### [vim-plug](https://github.com/junegunn/vim-plug)

```vim
Plug 'jonroosevelt/gemini-cli.nvim'
```

And then in your `init.lua`:

```lua
require('gemini').setup()
```

## Usage

- Use the keymap `<leader>og` to open and close the Gemini CLI window.
- In visual mode, select one or more lines and use the keymap `<leader>sg` to send the selected text to the Gemini CLI. If the CLI window is not open, a floating message will prompt you to open it first.

When you first run the plugin, it will check if you have the `gemini` CLI installed. If not, it will prompt you to install it.
