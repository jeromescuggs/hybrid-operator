!hybrid-operator()

# hybrid operator: a modernized take on the timeless classic 

this is an update of *vim-hybrid*, a fantastic theme from Andrew Wong. his description, from the original repo:

>A dark colour scheme for Vim that combines the:
>
>-   Default palette from [Tomorrow-Night](https://github.com/chriskempson/vim-tomorrow-theme).
>-   Reduced contrast palette from [Codecademy](https://www.codecademy.com)'s
>    online editor.
>-   Syntax group highlighting scheme from [Jellybeans](https://github.com/nanotech/jellybeans.vim)
>-   Vimscript from [Solarized](https://github.com/altercation/vim-colors-solarized)

## Updates

## Requirements

the original requirements:
-   gVim 7.3+ on Linux, Mac and Windows.
-   Vim 7.3+ on Linux and Mac, using a terminal that supports 256 colours.

to make the best of my tweaks:
-   a terminal that supports 256 colors, as well as italics. 
-   WSL/Windows: i haven't tested it on any terminal besides wsltty, aka mintty running wsl-bridge. 


## Installation

1.  Copy colors/hybrid.vim to:

    ```
    ~/.vim/colors/hybrid.vim
    ```

    or alternatively, use a plugin manger such as
    [vim-plug](https://github.com/junegunn/vim-plug),
    [NeoBundle](https://github.com/Shougo/neobundle.vim),
    [Vundle](https://github.com/gmarik/Vundle.vim), or
    [Pathogen](https://github.com/tpope/vim-pathogen).

2.  Add to ~/.vimrc:

    ```vim
    set background=dark
    colorscheme hybrid
    ```

3. **(Alternate)** If using SpaceVim: 

    add the following to your `init.toml` or `init.vim`:
    ```vim 
    [[custom_plugins]]
    name = "jeromescuggs/vim-hybrid"
    ```

    restart vim, and let SpaceVim download and install the theme. restart SpaceVim, and either load it manually: 

    ```vim 
    :colorscheme hybrid 
    ```

    or set it as the default in `init.toml` / `init.vim`: 

    ```vim 
    colorscheme = "vim-hybrid"
    ```     

## Further configuration

the following is from the original README. although I do not need to do anything further after installation, the following might be useful for troubleshooting. 

## Define custom terminal colours 

Due to the limited 256 palette, colours in Vim and gVim will still be slightly
different.

In order to have Vim use the same colours as gVim (the way this colour scheme
is intended) define the basic 16 colours in your terminal.

#### Linux users: rxvt-unicode, xterm

1.  Add the default palette to ~/.Xresources:

    https://gist.github.com/3278077

    ![palette](http://dl.dropbox.com/u/23813887/Xresources-palette.png)

    or alternatively, add the reduced contrast palette to ~/.Xresources:

    https://gist.github.com/w0ng/16e33902508b4a0350ae

    ![palette](https://www.dropbox.com/s/0ny88dmfw84kcma/Xresources-palette-low.png?dl=1)

2.  Add to ~/.vimrc:

    ```vim
    let g:hybrid_custom_term_colors = 1
    let g:hybrid_reduced_contrast = 1 " Remove this line if using the default palette.
    colorscheme hybrid
    ```

#### OSX users: iTerm

1.  Import the default colour preset into iTerm:

    https://raw.githubusercontent.com/w0ng/dotfiles/master/iterm2/hybrid.itermcolors

    ![iterm_palette](http://i.imgur.com/wSWCyen.png)

    or alternatively, import the reduced contrast color preset into iTerm:

    https://raw.githubusercontent.com/w0ng/dotfiles/master/iterm2/hybrid-reduced-contrast.itermcolors

    ![iterm_palette_reduced](https://www.dropbox.com/s/mrvr3ftkmym0fok/iterm_palette_reduced.png?dl=1)


2.  Add to ~/.vimrc:

    ```vim
    let g:hybrid_custom_term_colors = 1
    let g:hybrid_reduced_contrast = 1 " Remove this line if using the default palette.
    colorscheme hybrid
    ```
![vim-spell](https://dl.dropboxusercontent.com/u/23813887/vim-spell.png)


