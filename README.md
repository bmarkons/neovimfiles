Strika's Neovim configuration
==========================

Thanks to these guys:

* [Drew Neil](http://vimcasts.org)
* [Gary Bernhardt](http://destroyallsoftware.com)
* [Janus project](https://github.com/carlhuda/janus)
* [Mislav Marohnić](http://mislav.uniqpath.com/)
* [Tim Pope](http://tbaggery.com)

## Installation:

Prerequisites: git, ack.

1. Move your existing configuration somewhere else:
   `mv ~/.config/nvim* nvim_backup`
2. Clone this repo into ".config/nvim":
   `git clone https://github.com/bmarkons/neovimfiles ~/.config/nvim`
3. Go into ".config/nvim" and run "install":
   `cd ~/.config/nvim && ./install`

This will create temp and backup directories and install plugins. If plugin
installation fails for any reason, open Neovim and run `:PlugInstall`.

## Features:

* 2 spaces, no tabs
* 'Leader' character mapped to " " (space)
* `<CR>` - remove highlighting after search
* `<C-j/k/h/l>` - switch between splits (no need to prepend `<C-w>`)
* relative line numbers by default
* `<C-n>` switches between relative and absolute line numbers
* `Q` - format lines
* `  ` (space, space) - alternates between two most recent buffers
* `<leader>f` - opens file search with :CtrlP plugin:
  * `<leader>b` - search in directory of current buffer
  * `<leader>gl` - in `lib/`
  * `<leader>gm` - in `app/models`
  * `<leader>gv` - in `app/views`
  * `<leader>gc` - in `app/controllers`
  * `<leader>gs` - in `specs`
* `:KillWhitespace` - strip trailing whitespace
* `<leader>s` opens spec
* `<leader>v` opens spec in split view

### Ack

* `:Ack -w foo_bar --no-js --no-css`
* `:Ack!` - search, but don't jump to first match
* `:AckFromSearch`
* `:AckAdd` - append to existing quickfix list
* `<leader>a` - opens Ack with cursor between ""
* `<leader>A` - opens Ack and searches for the word below cursor

### Surround

* `cs"'` - change string from double to single quotes
* `ds(` - delete surrounding parentheses
* `ysiW]` - surround current WORD with square brackets
* `ysst` - surround current line in a HTML tag
* `ysip<c-t>` - nest current paragraph in a HTML tag

Visual mode: `S`. Insert mode: `<c-s>`.

Surround + rails.vim:

* `-` → `<% -%>`
* `=` → `<%= %>`
* `#` → `<%# %>`
* `e` - nest block and append `end` keyword
* `E` - like `e`, but prompt for text to prepend before block

### Commentary

* `\\{motion}` - comment/uncomment lines that {motion} moves over
* `\\\` - comment/uncomment [count] lines
* `{Visual}\\` - comment/uncomment the highlighted lines
* `\\u` - uncomment the current and adjacent commented lines

### ruby.vim

Motions:

* `]m` / `[m` - next / previous method
* `]M` / `[M` - end of method definition
* `]]` / `[[` - next / previous class/module
* `][` / `[]` - end of class/module

Text objects:

* `am` - a method
* `im` - inner method
* `aM` - a class
* `iM` - inner class

### matchit.vim

`%` alternates between matching HTML tags, class/control flow statements and
matching `end` in Ruby, and more. Also works in visual mode.

### Tabular

In visual mode:

* `:Tabularize assignment`
* `:Tabularize argument_list`
* `:Tabularize /=>`

### Fugitive

* `:Gcommit`
* `:Gstatus`
  * jump between lines that represent files with `<c-n>`, `<c-p>`
  * `-` - add/reset file (visual mode too)
  * `<Enter>` - open current file in the window below
  * `p` - run `git add --patch` for current file
  * `C` - invoke `:Gcommit`
* `:[range]Gbrowse! -` - copy GitHub URL for code that's currently selected
* `:[range]Gblame`
* `:Gedit feature:%` - version of the current file in the "feature" branch
* `:Gwrite` - `add %`
* `:Gread` - `checkout %`
* `:Gremove` - `rm %`
* `:Gmove <dest>` - `mv % <dest>`

## Plugins:

* ack.vim
* ctrlp.vim
* gruvbox
* neomake
* rename.vim
* ri.vim
* splitjoin.vim
* tabular
* vim-airline
* vim-airline-themes
* vim-commentary
* vim-endwise
* vim-es6
* vim-fugitive
* vim-numbertoggle
* vim-polyglot
* vim-rails
* vim-reek
* vim-repeat
* vim-surround
* vim-test
* vim-textobj-rubyblock
* vim-textobj-user

## Included colorschemes:

* gruvbox
