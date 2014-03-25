# go.vim

An attempt to bring full featured Go support to Vim. All necessary
binaries(gocode, goimports, godef, etc..) are installed once at startup
automatically. Open an issue for bugs/improvements.

## Features

* Syntax highlighting
* Auto go fmt on save
* Automatically import packages with goimports
* Autocomplete with `<C-x><C-o>` (omnicomplete)

## Install

If you use pathogen, just clone it into your bundle directory:

```bash
$ cd ~/.vim/bundle
$ git clone git://github.com/fatih/go.vim.git
```

Autocompletion is enabled by default via `<C-x><C-o>`, to get real-time
completion (completion by type) install YCM:

```bash
$ cd ~/.vim/bundle
$ git clone git@github.com:Valloric/YouCompleteMe.git
$ cd YouCompleteMe
$ ./install.sh
```

## Customize

Disable auto go fmt on save

    let g:go_fmt_autosave = 0

Disable goimports

    let g:gofmt_command = "gofmt"

Change gocode path, disables automatic installing of goimports

    let g:goimports_bin="~/your/custom/goimports/path"

Change gocode path, disables automatic installing of gocode

    let g:gocode_bin="~/your/custom/gocode/path"