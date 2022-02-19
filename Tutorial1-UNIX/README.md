# Tutorial 1 - The Command Line/Unix

On the more popular operating systems like Windows or Mac, we typically use our mouse or trackpad to click on icons to access files and applications. However, there are many other ways for us to communicate with our computers. The command line is a text-based interface that is quick, powerful and straight-to-the-point. It allows users to communicate with their computers or files directly. In other words, you can navigate to, open and modify files and folders on your computer without your mouse!

Unix is an operating system (similar to Windows or Mac OSX). It's made up of three parts: the <i>kernel</i>, the <i>shell</i> and the <i>programs</i>. 

#### If you're curious to know:

`kernel` - operating system hub which allocates time and memory to programs; handles file storage and system calls

`shell` - the interface between the user and the kernel; the command line interpreter (CLI) which interprets the user's commands and carries them out

`programs` - commands

## Getting Started
### Accessing a Unix-based OS
Download [Ubuntu for your Desktop](https://ubuntu.com/download/desktop).

Lost? Here's an excellent tutorial which guides Windows 10 users on Ubuntu installation:
[![How to Install Ubuntu 20.04 LTS on VirtualBox in Windows 10](http://img.youtube.com/vi/x5MhydijWmc/0.jpg)](https://www.youtube.com/watch?v=x5MhydijWmc)

When you have successfully installed and run Ubuntu on your computer, search for and open up the `Terminal`.

## Basic Commands
When you open the terminal, you start in your home directory by default. Your home directory may have the same name as your computer's username. This is where your files and folders are saved.

In the terminal, type:
```bash
pwd
```
This <i>prints your working directory</i>, or the directory that you are in presently. 

### Listing Files and Folders
`ls` lists the contents of your current working directory. 
To find out what is in your home directory, type:
```bash
ls
```
Hidden files begin with a dot (.) and usually contain important program configuation information. Don't change these contents unless you absolutely must! To view these hidden files, type the command with the option `-a`:
```bash
ls -a
```
`options` change the behaviour of a command. In Unix, options are specified by a dash `-` after the command name followed by letters, numebers or words.
For instance, `ls -l` will give a detailed list compared to just `ls`.


### Making & Moving Between Directories
A `directory` is interchangeable with the common word `folder`. 
To create a subdirectory in your home directory, use the `mkdir` command.
```bash
mkdir new_folder
```
List your home directory to see the new subdirectory.
```bash
ls
```

`cd` To navigate to your home folder by default, type
```bash
cd
```
or
```bash
cd ~
```
Hopefully, you find that `cd` and `cd ~` do the same thing - return you to your home directory. Try using `pwd` to confirm your results. 
Two dots `..` are used in Unix to refer to the <i>parent</i> directory. Every directory has a parent, except the root level.
Try navigating to the subdirectory `new_folder` and going back to your `home` directory using `..`:
```bash
cd ~
cd new_folder
pwd
cd ..
pwd
```
### Help?! There are too many commands and options.
If there are so many commands, and those commands have options, how would you ever know which one to use?
Luckily, every basic Unix command has a <i>manual</i> that can be accessed using the `man` command.
Try using `man` on some of the commands that you've learned so far:
```bash
man ls
man cd
man man    # even the man command has a manual!
```
### Creating Text Files
You can create new text files using `>filename.txt`. This will create an empty file.
```bash
>my_file.txt
```
You can also use the command `touch`. This creates a new, empty file.
```bash
touch my_other_file.txt
```
#### Nano
To edit this file, you can use a text editor like `nano`.
```bash
nano my_file.txt
```
You are now in the nano text editor and can enter your text as you'd like.
To save an exit, type `ctrl-o` then `ctrl-x`.

### Tidying Up - Removing Files & Folders
To remove directories you don't need, use the `rmdir` command. This can only be used if a directory is empty.
```bash
rmdir new_folder
```
To remove folders, use the `rm` command.
```bash
rm my_other_file.txt
```
<b>Important!</b> `rm` may be too simple and too easy -- once something is gone, it's permanently gone. Unlike with Windows and Mac, if you delete something with `rm` in Unix, it does not go to the trash/recycling can - it's permanently remoed. It's possible to delete everything in your home directory. It is highly advised to never use the `rm -fr` command (force delete). Careful what you type! (Read more: https://docstore.mik.ua/orelly/unix3/upt/ch14_03.htm)

### Viewing File Previews
Create a new text file, enter a couple lines of text using `nano`, save and exit.
```bash
>my_DNA.txt
nano my_DNA.txt
```
Say `my_DNA.txt` has the following text inside:
```bash
A
T
C
G
```
To quickly view the contents of your file, you can print them to the screen using a variety of commands:
```bash
cat my_DNA.txt
less my_DNA.txt
more my_DNA.txt
head my_DNA.txt
head -n 10 my_DNA.txt # first 10 lines of your file
tail my_DNA.txt
tail -n 10 my_DNA.txt # last 10 lines of your file
```
### File Size
To check the size of a file, use:
```bash
du my_DNA.txt
du -h my_DNA.txt       # in human-readable output (byte, kb, mb, etc.)
```
### Moving Files and Folders
Assume that we want to move some files to a new directory called `genome`. We can use the `mv` command:
```bash
mkdir genome
mv my_DNA.txt genome/
cd genome
ls
```
The `mv` command requires that we specify a source file or directory that we want to move, then its target location.

We can move more than file at once using the asterisk `*`. `*` is known as a <i>wild-card character</i>, meaning 'match anything'.
Let's see this in action. Navigate home and create more text files using `touch` and move them to your `genome` folder.
```bash
cd
touch my_bacteria.txt
touch my_viruses.txt


mv *bact* genome/    # match anything that contains 'bact' in the name
ls

mv *.txt genome/     # match anything with a name that ends in '.txt' 
ls

cd genome/
ls
```
### Renaming Files
`mv`, along with moving files and folders, can also be used to rename files and folders.
Let's rename the `genomes` folder to `organisms`:
```bash
cd
ls
mv genomes/ organisms/
ls
```
### Remote Access & File Transfer
Note: You might not have a second server to login to, and that's okay! It may be helpful to be familiar with the commands below.
`ssh` 
`scp` Allows you to copy files between servers
```bash
# Moving file.txt to a server
scp /path/to/file.txt username@remoteserver.com:/path/to/location/.
```
```bash
# Moving file.txt from a server
scp username@remoteserver.com:/path/to/file.txt /path/to/location/.
```


## Resources
* [Unix and Perl Primer for Biologists](http://korflab.ucdavis.edu/Unix_and_Perl/current.pdf)
* [Codecademy](https://www.codecademy.com/catalog/language/bash)
* [LabEx - Prctice Linux Commands](https://labex.io/courses/linux-basic-commands-practice-online)
* [Unix Tutorial for Beginners](http://www.ee.surrey.ac.uk/Teaching/Unix/)
