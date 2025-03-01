# rickrollrc

Bash script which [rickrolls](http://en.wikipedia.org/wiki/Rickrolling) your
terminal by playing Rick Astley’s “Never Gonna Give You Up” with ANSI 256-color
coded UTF-8 characters + audio (if available).

## How to Roll
To start rickrollin’ immediately:

    curl -s -L https://raw.githubusercontent.com/dert1129/rickrollrc/master/roll.sh | bash

Here is the clandestine command you can give to your friends 😈

    curl -s -L http://tinyurl.com/mr486nnx | bash

![rickroll in xterm](http://i.imgur.com/ZAsQWtP.png)
![rickroll in mac](http://i.imgur.com/yDLaZna.png)

For the record: It is not actually a good idea to make a habit of

    curl $(random_script_from_the_internets) | bash"

Nevertheless, for the enhanced experience, I highly recommend the following:

    ./roll.sh inject

Which essentially just does:

    echo "curl -s -L http://bit.ly/10hA8iC | bash" >> ~/.bashrc

For a salutary lesson in the importance of taking care what you
execute in your terminal, inspired by the classic
[sl](http://www.tkl.iis.u-tokyo.ac.jp/~toyoda/index_e.html), save the
command in a shell script called `suod` somewhere on your `PATH`. It’s
recommended to download the script for faster startup, to avoid
spoiling the surprise when you accidentally execute it for the nth
time (and also, unless you really like living dangerously, for
security, in case we are demonically possessed to replace `roll.sh`
with something evil).

## Flipper Zero Integration

This is a fork of the original repository: https://github.com/keroserene/rickrollrc
I've added a short script that uses the Flipper Zero's BadUSB App to call the link on the host's computer to Completely Rick Roll them

## Flipper Zero installation
You MUST HAVE an SD card in order to install external scripts
1. Download the qFlipper app here: `https://flipperzero.one/update`
2. Open SD Card
3. Open badUSB and drop the .txt file(s) into the directory.
4. Rick roll everyone!


## Misc.

This has been tested on Arch, Debian, Ubuntu, Mac and Cygwin (so far).
To enable sound in Cygwin, install the **sox** package.

Since this is a colorful hobby, you need to ensure 256-color mode is enabled or
Astley will look sad.

For example, if you use GNU screen, ensure your ~/.screenrc contains something
like:

    termcapinfo xterm 'Co#256:AB=\E[48;5;%dm:AF=\E[38;5;%dm'
    defbce "on"

Kudos to jart for our lovely hiptext shenanigans.
Please see our sister project: [hiptext](https://github.com/jart/hiptext), which
generates ANSI color codes for any image or video.

<3,

~serene ([@kiserene](http://twitter.com/kiserene))
