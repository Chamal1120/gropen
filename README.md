<div align=center>

# Gropen

</div>

#### What is GROPEN?
Gropen is a simple bash script that can open the remote repo of your CWD's git repo from your browser.

#### How to install (Manual)
1. Place the script in one of your `PATH`s.
2. Source your shell configuration.
3. That's it! (Try typing `gropen` inside a git directory)

#### For maximum productivity
1. Map a keybind in your shell configuration file.

Example for zsh:

```bash
# Run gropen with ctrl + g
bindkey -s '^g' 'gropen\n'
```

2. Add custom command to your terminal IDE.

Example for neovim:

```lua
-- Add this to your init.lua 

-- Create a custom command for gropen
vim.api.nvim_create_user_command("Gropen", function()
  vim.fn.jobstart({ "gropen" })
end, {})

-- Create a keybind for the custom command (Run gropen with ctrl + g)
vim.keymap.set("n", "<C-g>", ":Gropen<CR>", { noremap = true, silent = true })
```

#### TODO
 - [ ] Add support for multiple remotes.
 - [ ] Add an install script.
 - [ ] Switch to bubble tea for better UX.

