[![dotvim][1]][2]
[1]: http://www.vim.org/images/vim_editor.gif
[2]: http://www.vim.org/ "Click to visit vim.org"

## Prerequisites

* [Vim](http://www.vim.org/) 7.3 or newer

* [Git](http://git-scm.com/) 1.5 or newer

* [POSIX shell](http://pubs.opengroup.org/onlinepubs/009695399/utilities/sh.html) POSIX Shell

## Mac OS X (Unix-like)

    cd ~

Clone the repository

    git clone https://github.com/billinux/dotvim.git ~/dotvim

Backup your Vim config

    mv ~/.vimrc{,.bak}
    mv ~/.vimrc.before{,.bak}
    mv ~/.vimrc.before.local{,.bak}
    mv ~/.vim{,.bak}

Symlink files

    ln -sfn ~/dotvim/.vimrc ~/.vimrc
    ln -sfn ~/dotvim/.vimrc.before ~/.vimrc.before

Create your own local environment

    touch ~/.vimrc.before.local

Install Bundles

    cd ~/.vim
    git submodule update --init
    vim +qall

Compile vimproc according your achitecture (x86, x64)


## Windows

As administrator (or mklink doesn't work)

    cmd
    cd %HOMEPATH%

Clone the repository

    git clone https://github.com/billinux/dotvim.git dotvim

Symlink files

    mklink .vimrc dotvim\.vimrc
    mklink .vimrc.before dotvim\.vimrc.before
    mklink /D .vim dotvim\.vim

Create your own local environment

    copy .vimrc.before.local

Install bundles

    cd .vim
    git submodule update --init
    vim +qall

After installing the bundles

    cd bundle\vimproc.vim
    Compile vimproc according your architecture

## Author

[Bill Linux](mailto:b.linux@laposte.net)
