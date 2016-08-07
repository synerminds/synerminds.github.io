---
layout: post
title:  Importance of using the terminal?
meta:   August 02, 2016
author: Camilo Martinez
---
Under multiple platforms the Operating System has the GUIs (graphical user interfaces), where you can as a user point, click and drag on multiple components of the OS, which makes the user experience extremely easy and friendly. 

The traditional Unix environment are based into CLI (command line interface), where you as a user have the necessity to type commands to tell the computer what to do. Believe it or not, that is faster and more powerful to handle the Operating System.

So, with the review made before, please join us reading this post which has the purpose to give you an introduction to use the fantastic world of CLI (command line interface).

## Basic Concepts related to the CLI:

- **Console:** This is the system as a whole. This is both the command line as well as the output from previous commands.
- **Command Line:** This is the actual line in a console where you type your command.
- **Prompt:** This is the beginning of the command line. It usually provides some contextual information like who you are, where you are and other useful info. After the prompt is where you will be typing commands.
- **Terminal:** This is the actual interface to the console. The program we use to interact with the console is actually a **“terminal emulator”**, providing us the experience of typing into an old school terminal from the convenience of our modern graphical operating system.

## How to start/access the terminal:
### Linux:
- **Unity** 
    - Dash -> Search for Terminal
    - Dash -> More Apps -> 'See More Results' -> Terminal
    - Dash -> More Apps -> Accessories -> Terminal
    - Keyboard Shortcut: Ctrl + Alt + T
- **GNOME**
    - Applications menu -> Accessories -> Terminal.
    - Keyboard Shortcut: Ctrl + Alt + T
- **Xfce (Xubuntu)**
    - Applications menu -> System -> Terminal.
    - Keyboard Shortcut: Super + T
    - Keyboard Shortcut: Ctrl + Alt + T
- **KDE (Kubuntu)**
    - KMenu -> System -> Terminal Program (Konsole).
- **LXDE (Lubuntu)**
    - Menu -> Accessories -> LXTerminal.
    - Keyboard Shortcut: Ctrl + Alt + T
- **OSx:**
    - ⌘(Command) + Space, type “Terminal” and then hit “Enter”
    
## Let's get started:

**ls**

The command “ls” stands for (List Directory Contents), List the contents of the folder, be it file or folder, from which it runs.If you run ls without any additional parameters, the program will list the contents of the current directory in short form.

- **ls**

```sh
syner@synerpc:~$ ls
Desktop    Downloads         Music     Public     Videos
Documents  examples.desktop  Pictures  Templates
syner@synerpc:~$ 
```

- Detailed list: **ls -l** 

```sh
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

- Displays hidden files: **ls -a**

```sh
syner@camilopc:~$ ls -a
.              Downloads         Public
..             examples.desktop  .sudo_as_admin_successful
.bash_history  .gconf            Templates
.bash_logout   .gnupg            Videos
.bashrc        .ICEauthority     .Xauthority
.cache         .local            .xsession-errors
.config        Music             .xsession-errors.old
Desktop        Pictures
Documents      .profile
syner@camilopc:~$ 
```	

**pwd**

In the console, you are always working in a directory, or folder, on your computer. We call this your working directory. You can see where you are using pwd (short for print working directory)

```sh
syner@synerpc:~$ pwd
/home/syner
```

```sh
syner@synerpc:~/Desktop$ pwd
/home/syner/Desktop
```

**cd**

The **"cd"** command stands for (change directory), and what it does is allow you to change your current location. It always needs a parameter.

```sh
syner@synerpc:~$ ls 
Desktop    Downloads         Music     Public     Videos
Documents  examples.desktop  Pictures  Templates
syner@synerpc:~$ cd Desktop/
syner@synerpc:~/Desktop$ cd Test
syner@synerpc:~/Desktop/Test$ 
```

You can also, use multiple parameters at instead of going one by one like the following example:

```sh
syner@synerpc:~/Desktop/Test$ pwd
/home/syner/Desktop/Test
syner@synerpc:~/Desktop/Test$ 
```

**mkdir**

The “mkdir” (Make directory) command create a new directory with name path. 

```sh
camilo@camilopc:~/Desktop$ ls
Test
camilo@camilopc:~/Desktop$ mkdir CLIROCKS
camilo@camilopc:~/Desktop$ ls
CLIROCKS  Test
camilo@camilopc:~/Desktop$ 
```

**mv**		
The **“mv”** command moves a file from one location to another location.

```sh
syner@synerpc:~/Desktop$ ls
MovingFolder  Test
syner@synerpc:~/Desktop$ mv MovingFolder Test
syner@synerpc:~/Desktop$ ls
Test
syner@synerpc:~/Desktop$ cd Test
syner@synerpc:~/Desktop/Test$ ls
MovingFolder
syner@synerpc:~/Desktop/Test$ 
```

**Note:** You can also add the **"-i"** option after the **mv**, and basically if the file you are moving exist, you will be prompted before it is overwritten.

**cp**

This **"cp"** command it copies a file from one location to another location.

```sh
syner@synerpc:~/Desktop/Test$ ls
MovingFolder  testdoc
syner@synerpc:~/Desktop/Test$ cp testdoc testdocascopy
syner@synerpc:~/Desktop/Test$ ls
MovingFolder  testdoc  testdocascopy
```

You can also copy the file into a different location, using the right structure as the following example which copy the file to the Desktop folder

```sh
syner@synerpc:~/Desktop/Test$ cp testdoc ../testdocascopy
syner@synerpc:~/Desktop/Test$ cd ..
syner@synerpc:~/Desktop$ ls
Test  testdocascopy
syner@synerpc:~/Desktop$ 
```

**chmod**

The “chmod” command stands for (change file mode bits). chmod changes the file mode (permission) of each given file, folder, script, etc.. according to mode asked for.

There exist 3 types of permission on a file (folder or anything but to keep things simple we will be using file).

- **Read ( r ) = 4**
- **Write ( w ) = 2**
- **Execute ( x ) = 1**

**Example:**

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

You can use the history command to show a list of all the recently used commands, or the up/down arrows to loop through them.

```sh
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

