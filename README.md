[![dotvim][1]][2]
[1]: http://www.vim.org/images/vim_editor.gif
[2]: http://www.vim.org/ "Click to visit vim.org"

## Requirements

* [Vim](http://www.vim.org/) 7.3 or newer
* [Git](http://git-scm.com/) 1.5 or newer
* [POSIX shell](http://pubs.opengroup.org/onlinepubs/009695399/utilities/sh.html) POSIX Shell


## Mac OS X (Unix-like)

    $ cd ~

### Clone the repository

    $ git clone https://github.com/billinux/dotvim.git ~/dotvim

### Backup your Vim config

    $ mv ~/.vimrc{,.bak}
    $ mv ~/.vimrc.before{,.bak}
    $ mv ~/.vimrc.before.local{,.bak}
    $ mv ~/.vim{,.bak}

### Symlink files

    $ ln -sfn ~/dotvim/.vimrc ~/.vimrc
    $ ln -sfn ~/dotvim/.vimrc.before ~/.vimrc.before

### Create your own local environment

    $ touch ~/.vimrc.before.local

### Install Bundles

    $ cd ~/.vim
    $ git submodule update --init
    $ vim +qall

### Compile vimproc according your achitecture (i386, x86_64)
    $ cd ~/.vim/bundle/vimproc.vim

#### Linux, Mac OS X
    $ make
Note: if you want to build for multiple architectures, you can use *ARCHS* and *CC* variables
Build for i386 and x86_64:
    $ make ARCHS='i386 x86_64'
#### FreeBSD
    $ make
#### Solaris
    $ gmake
Note: if you want to use SUN compiler, you can use *SUNCC* variable
    $ gmake SUNCC=cc


## Windows

As administrator (or mklink doesn't work)

    > cmd
    > cd %HOMEPATH%

### Clone the repository

    > git clone https://github.com/billinux/dotvim.git dotvim

### Symlink files

    > mklink .vimrc dotvim\.vimrc
    > mklink .vimrc.before dotvim\.vimrc.before
    > mklink /D .vim dotvim\.vim

### Create your own local environment

    > copy .vimrc.before.local

### Install bundles

    > cd .vim
    > git submodule update --init
    > vim +qall

### After installing  bundles

    > cd bundle\vimproc.vim

### Compile vimproc according your achitecture (x86, x64)
Note: in Windows, using MinGW is recommanded
Note: if you have not "gcc" binary, you must change $CC value

    $ cd ~/.vim/bundle/vimproc.vim

#### Windows (Vim 32 bits)
    > mingw32-make -f make_mingw32.mak
#### Windows (Vim 32 bits) using cygwin
    > mingw32-make -f make_mingw32.mak CC=mingw32-gcc
#### Windows (Vim 64 bits)
    > mingw32-make -f make_mingw64.mak

## Dropbox
Supposed the dotvim directory is installed in *~/Dropbox/Safe/dotvim*

### Unix-like

#### Symlink files
    $ ln -sfn ~/Dropbox/Safe/dotvim/.vim ~/.vim
    $ ln -sfn ~/Dropbox/Safe/dotvim/.vimrc ~/.vimrc
    $ ln -sfn ~/Dropbox/Safe/dotvim/.vimrc.before ~/.vimrc.before

#### Create your own local environment
    $ touch ~/.vimrc.before.local

### Windows
    > mklink "C:\Users\YourUserName\.vimrc" "C:\Users\YourUserName\Dropbox\Safe\.vimrc"
    > mklink /D "C:\Users\YourUserName\.vim" "C:\Users\YourUserName\Dropbox\Safe\.vim"

## Author

[Bill Linux](mailto:b.linux@laposte.net)
