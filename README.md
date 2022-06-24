## A Quick Introduction to Hydra.nvim - Neovim Sub Mode Plugin  

## Links:

- https://github.com/anuvyklack/hydra.nvim

## Hydra Window Switch / Resize example:

```lua
local Hydra = require("hydra")

Hydra({
	name = "Change / Resize Window",
	mode = { "n" },
	body = "<C-w>",
	config = {
		-- color = "pink",
	},
	heads = {
		-- move between windows
		{ "<C-h>", "<C-w>h" },
		{ "<C-j>", "<C-w>j" },
		{ "<C-k>", "<C-w>k" },
		{ "<C-l>", "<C-w>l" },

		-- resizing window
		{ "H", "<C-w>3<" },
		{ "L", "<C-w>3>" },
		{ "K", "<C-w>2+" },
		{ "J", "<C-w>2-" },

		-- equalize window sizes
		{ "e", "<C-w>=" },

		-- close active window
		{ "Q", ":q<cr>" },
		{ "<C-q>", ":q<cr>" },

		-- exit this Hydra
		{ "q", nil, { exit = true, nowait = true } },
		{ ";", nil, { exit = true, nowait = true } },
		{ "<Esc>", nil, { exit = true, nowait = true } },
	},
})
```

## My Ctrl+J and Ctrl+K remap

```lua
vim.keymap.set("n", "<C-j>", [[:keepjumps normal! j}k<cr>]], {noremap = true, silent = true})
vim.keymap.set("n", "<C-k>", [[:keepjumps normal! k{j<cr>]], {noremap = true, silent = true})
```
