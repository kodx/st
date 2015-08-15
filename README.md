# st - simple terminal
st is a simple terminal emulator for X which sucks less from [suckless.org](http://suckless.org).
[Original site](http://st.suckless.org/)
Original version - 0.6 (2015-07-07)

## Requirements

In order to build st you need:

- Xlib header files - location of these might differ, edit config.mk
- xft lib headers.


## Installation

Edit config.mk to match your local setup (**st** is installed into the **/usr/local** namespace by default).

**NOTE:** to have unicode character support, install **freetype2** library headers.

### Ubuntu required libraries

    apt-get install libx11-dev libxext-dev libxft-dev

Afterwards enter the following command to build and install st (if
necessary as root):

    make clean install

Install st to ~/bin:

    make
    make home

## Running st

If you did not install st with make clean install, you must compile
the st terminfo entry with the following command:

    tic -s st.info

Run it with tmux:

    st -e /bin/sh -c 'tmux a || tmux'

See the man page for additional details.

## Credits

Based on Aurélien APTEL <aurelien dot aptel at gmail dot com> bt source code.
