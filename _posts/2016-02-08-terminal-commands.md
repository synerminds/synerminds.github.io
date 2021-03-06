---
layout: post
title:  Importance of using the terminal?
meta:   August 02, 2016
author: Camilo Martinez
---

Nowadays, most Operating Systems (OS) include a Graphical User Interface (GUI), where users can point, click and drag on multiple components of the GUI, which makes it much easier for users to interact with the OS."

Traditional Unix environments are based into CLI (command line interface), where you as a user have the necessity to type commands to tell the computer what to do. Believe it or not, that is faster and more powerful to handle the Operating System.

Having said that, the purpose of this post is to give you an introduction to the CLI (command line interface).

### Basic Concepts related to the CLI:

- **Console:** This is the system as a whole. This is both the command line as well as the output from previous commands.
- **Command Line:** This is the actual line in a console where you type your command.
- **Prompt:** This is the beginning of the command line. It usually provides some contextual information like who you are, where you are and other useful info. After the prompt is where you will be typing commands.
- **Terminal:** This is the actual interface to the console. The program we use to interact with the console is actually a **“terminal emulator”**, providing us the experience of typing into an old school terminal from the convenience of our modern graphical operating system.
- **Command:** A command is a specific order from a user to the computer's operating systems or to an application to perform an action. Operating systems that do not have a graphical user interface (GUI) offer a simple command line interface in which you type the command on a designated line in a display panel. In operating systems with graphical user interface, you implicitly enter commands by selecting objects, word selections or simply clicking with the mouse button on them.

### How to start/access the terminal in different Operating Systems:

- Unity
    - Dash -> Search for Terminal
    - Dash -> More Apps -> 'See More Results' -> Terminal
    - Dash -> More Apps -> Accessories -> Terminal
    - Keyboard Shortcut: Ctrl + Alt + T
- GNOME
    - Applications menu -> Accessories -> Terminal.
    - Keyboard Shortcut: Ctrl + Alt + T
- Xfce (Xubuntu)
    - Applications menu -> System -> Terminal.
    - Keyboard Shortcut: Super + T
    - Keyboard Shortcut: Ctrl + Alt + T
- KDE (Kubuntu)
    - KMenu -> System -> Terminal Program (Konsole).
- LXDE (Lubuntu)
    - Menu -> Accessories -> LXTerminal.
    - Keyboard Shortcut: Ctrl + Alt + T
- OSx:
    - ⌘(Command) + Space, type “Terminal” and then hit “Enter”
   
### Let's get started:

**ls**

The command `ls` stands for (List Directory Contents), List the contents of the folder, be it file or folder, from which it runs. If you run `ls` without any additional parameters, the program will list the contents of the current directory in short form.

#### Examples:

```sh
# Basic usage
syner@synerpc:~$ ls
Desktop    Downloads         Music     Public     Videos
Documents  examples.desktop  Pictures  Templates
syner@synerpc:~$
 ```
 
 ```sh
# Detailed listing of contents
syner@synerpc:~$ ls -l
total 44
drwxr-xr-x 3 syner syner 4096 ago  2 17:54 Desktop
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Documents
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Downloads
-rw-r--r-- 1 syner syner 8980 ago  2 17:36 examples.desktop
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Music
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Pictures
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Public
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Templates
drwxr-xr-x 2 syner syner 4096 ago  2 17:47 Videos
syner@synerpc:~$ 
 ```
 
 ```sh
# Listing hidden contents
syner@synerpc:~$ ls -a
.              Downloads         Public
..             examples.desktop  .sudo_as_admin_successful
.bash_history  .gconf            Templates
.bash_logout   .gnupg            Videos
.bashrc        .ICEauthority     .Xauthority
.cache         .local            .xsession-errors
.config        Music             .xsession-errors.old
Desktop        Pictures
Documents      .profile
syner@synerpc:~$ 
```

**pwd**

In the console, you are always working in a directory, or folder, on your computer. We call this your working directory. You can see where you are using `pwd` (short for print working directory)

#### Examples:

```sh
# Current Position Syner
syner@synerpc:~$ pwd
/home/syner
# Current Position Desktop of Syner
syner@synerpc:~/Desktop$ pwd
/home/syner/Desktop
```

**cd**

The `cd` command stands for (change directory), and what it does is allow you to change your current location. It always needs a parameter.

#### Examples:

```sh
# Listing all the available elements under the current position
syner@synerpc:~$ ls 
Desktop    Downloads         Music     Public     Videos
Documents  examples.desktop  Pictures  Templates
# Changing the current position to Desktop
syner@synerpc:~$ cd Desktop/
syner@synerpc:~/Desktop$ cd Test
syner@synerpc:~/Desktop/Test$ 
```

You can also, use multiple parameters at instead of going one by one like the following example:

```sh
#Sending multiple parameters into the cd command
syner@synerpc:~$ cd Desktop/Test
syner@synerpc:~/Desktop/Test$
```

**mkdir**

The `mkdir` (Make directory) command create a new directory with name path. 

```sh
# Listing all the available elements under the current position
syner@synerpc:~/Desktop$ ls
Test
# Creating a new directory into the current position
syner@synerpc:~/Desktop$ mkdir CLIROCKS
syner@synerpc:~/Desktop$ ls
# Listing all the available elements under the current position
CLIROCKS  Test
syner@synerpc:~/Desktop$ 
```

**mv**	

The `mv` command moves a file from one location to another location.

```sh
# Listing all the available elements under the current position
syner@synerpc:~/Desktop$ ls
MovingFolder  Test
# Moving the "MovingFolder" into the "Test" folder
syner@synerpc:~/Desktop$ mv MovingFolder Test
# Listing all the available elements under the current position
syner@synerpc:~/Desktop$ ls
Test
# Changing the current position to Desktop
syner@synerpc:~/Desktop$ cd Test
# Listing all the available elements under the current position
syner@synerpc:~/Desktop/Test$ ls
MovingFolder
# Listing all the available elements under the current position
syner@synerpc:~/Desktop/Test$ 
```

**Note:** You can also add the `-i` option after the `mv`, and basically if the file you are moving exists, you will be prompted before it is overwritten.

**cp**

This `cp` command it copies a file from one location to another location.

```sh
# Listing all the available elements under the current position
syner@synerpc:~/Desktop/Test$ ls
MovingFolder  testdoc
# Creating a copy of "testdoc" with a new name
syner@synerpc:~/Desktop/Test$ cp testdoc testdocascopy
# Listing all the available elements under the current position
syner@synerpc:~/Desktop/Test$ ls
MovingFolder  testdoc  testdocascopy
```

You can also copy the file into a different location, using the right structure as the following example which copy the file to the Desktop folder

```sh
# Creating a copy of "testdoc" with a new name into a different location
syner@synerpc:~/Desktop/Test$ cp testdoc ../testdocascopy
# Going back one position from the current position 
syner@synerpc:~/Desktop/Test$ cd ..
# Listing all the available elements under the current position
syner@synerpc:~/Desktop$ ls
Test  testdocascopy
syner@synerpc:~/Desktop$ 
```

**chmod**

The `chmod` command stands for (change file mode bits). chmod changes the file mode (permission) of each given file, folder, script, etc.. according to mode asked for.

There exist 3 types of permission on a file (folder or anything but to keep things simple we will be using file).

- **Read ( r ) = 4**
- **Write ( w ) = 2**
- **Execute ( x ) = 1**

**Examples:**

```shsyner
syner@synerpc:~# chmod syner.py
rwxr-x--x   syner.py
```

To change its permission and provide read, write and execute permission to owner, group and world.

```sh
syner@synerpc:~# chmod 777 syner.py
```

only read and write permission to all three.

```sh
syner@synerpc:~# chmod 666 syner.py
```

read, write and execute to owner and only execute to group and world.

```sh
syner@synerpc:~# chmod 711 syner.py
```

**history**

You can use the `history` command to show a list of all the recently used commands, or the up/down arrows to loop through them.

```sh
# Listing all the commands used
syner@synerpc:~$ history
    1  ls
    2  cd Desktop/
    3  ls
    4  ls
    5  ls -l
    6  ls -a
    7  pwd
    8  mkdir CLIROCKS
    9  mv CLIROCKS Test
    10  cp testdoc testdocascopy
    11  cp testdoc ../testdocascopy
    12  history
```

## References:
- [Rapidtables](http://www.rapidtables.com/code/linux/index.htm)
- [Basic UNIX commands](http://mally.stanford.edu/~sr/computing/basic-unix.html)
- [Important Linux Commands](https://www-uxsup.csx.cam.ac.uk/pub/doc/suse/suse9.0/userguide-9.0/ch24s04.html)
- [Basic Linux Commands](http://www.comptechdoc.org/os/linux/usersguide/linux_ugbasics.html)
