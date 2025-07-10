**Computer Science Linux & Unix Class Note**

Command that use for connect to university Linux Server\
old//ssh nattapol36@sukreep.cs.sci.ku.ac.th (if login at KU)\
old//ssh nattapol36@sukreep.cs.sci.ku.ac.th -p 23522 (if login outside KU)

new//ssh 6710450830@sukreep.cs.sci.ku.ac.th\
new//password: pwd.<username>

connect to something//scp -P 23522 6710450830@sukreep.cs.sci.ku.ac.th.

password is pwd.user36


**VIM note**
* use *:+q* to save file (type w first and then file name)\
* use *shift + zz to* exit\
* use *q + !* to exit without save

* use *vimtutor* to see tutorial for vim

* when command success there will be no sign
* when in cursor mode use *i* to back in type mode

* in cursor use *x* to delete incorrect text (stay in cursor mode to use it)\
* use *0* to return to the left

**VIM note 08/07/2025**\
_Shell_: part of unix that visible to users used to interprete command read commands and works with kernel to execute commands and shell allows a programmer to write/run shell script\
_Kernel_: core component that manages the computer's resources and acts as the bridge between hardware and software. It's the first program loaded when a computer starts and handles essential tasks like memory management, process management and device control.\
_bash_: is a command-line interpreter and scripting language widely used in Unix-like operating systems like Linux and macOS. It allows users to interact with the operating system by executing commands and writing scripts to automate tasks.

* using command 'man man' to open manual in vim\
* using command 'help' to open command menu\
* you can use 'man' and 'help' to do combo like you open 'help' to find what \command you want to use and use 'man [command]' to see what that command can do and how to use that command

Note: 'less' is the better version of 'more' command

**VIM note 10/07/2025**
* save file by *sav filename* in command mode (this is just save it not quit automatically)
* you can use *wq* to save and quit too
* use *esc* to switch to normal mode 
* you can enter command mode by using *:* in normal
* use *i* to switch to insert mode to type text

Note: when you accidentally get stuck in GNU Nano use Ctrl+x to exit

* if you want to pull file from server use this:\
scp username@server:/home/folder/filename D:\folderONlocal\
Example: scp -P 23522 6710450830@sukreep.cs.sci.ku.ac.th:/home/6710450830/test.txt D:\VIM
* using command vim filename.txt to open new file on vim but if there's the same file name in that folder it\
will open that folder instead
* use *set nocompatible* to unlocks all the modern Vim goodies
* use *set textwidth=[number]* to set range of the line to make it enter new line automatically
* in vim you can use *w* to jump from word to next word
* use *0* to jump at the first text in line
* use *dd* to delete an entire line
* use *yy* to copy line (in normal mode) and your cursor has to stay at that line to copy you can also copy multiple line by add number in front of *yy*\
example: 2yy to copy the line your cursor stay and one line below
* use *p* to paste the copy you can paste multiple line by *[number]p*\
example: 3000p to paste that line three thousand times (all of this method do in normal mode)
* use *o* to insert new line in normal mode 