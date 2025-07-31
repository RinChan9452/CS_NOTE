**Computer Science Linux & Unix Class Note**

Command that use for connect to university Linux Server\
old//ssh nattapol36@sukreep.cs.sci.ku.ac.th (if login at KU)\
old//ssh nattapol36@sukreep.cs.sci.ku.ac.th -p 23522 (if login outside KU)

new//ssh 6710450830@sukreep.cs.sci.ku.ac.th\
new//password: pwd.<username>

connect to something//scp -P 23522 6710450830@sukreep.cs.sci.ku.ac.th.

password is pwd.user36


**VIM note**
* use *:+q* to save file (type w first and then file name)
* use *shift + zz to* exit
* use *q + !* to exit without save

* use *vimtutor* to see tutorial for vim

* when command success there will be no sign
* when in cursor mode use *i* to back in type mode

* in cursor use *x* to delete incorrect text (stay in cursor mode to use it)
* use *0* to return to the left

**VIM note 08/07/2025**\
_Shell_: part of unix that visible to users used to interprete command read commands and works with kernel to execute commands and shell allows a programmer to write/run shell script\
_Kernel_: core component that manages the computer's resources and acts as the bridge between hardware and software. It's the first program loaded when a computer starts and handles essential tasks like memory management, process management and device control.\
_bash_: is a command-line interpreter and scripting language widely used in Unix-like operating systems like Linux and macOS. It allows users to interact with the operating system by executing commands and writing scripts to automate tasks.

* using command 'man man' to open manual in vim
* using command 'help' to open command menu
* you can use 'man' and 'help' to do combo like you open 'help' to find what \command you want to use and use 'man [command]' to see what that command can do and how to use that command

Note: 'less' is the better version of 'more' command

**VIM note 10/07/2025**
* save file by *sav filename* in command mode (this is just save it not quit automatically)
* you can use *wq* to save and quit too
* use *esc* to switch to normal mode 
* you can enter command mode by using *:* in normal
* use *i* to switch to insert mode to type text

Note: when you accidentally get stuck in GNU Nano use Ctrl+x to exit

* you can use *pwd* to check directory address
* you can use *ls* to check what file is in directory
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
* use *Ctrl + v* to enter block mode
* in block mode you can use highlight specific word to copy paste or delete (like cursor mouse but\ 
instead of using mouse to highlight you use keyboard instead)
* in block mode use *y* to copy the highlight
* in block mode use *p* to paste the highlight
* in block mode use *d* to delete the highlight
* in block mode use *c* to replace the highlight
* in block mode use *I* to insert before the highlight
* in block mode use *A* to append after the highlight

Note: .vimrc use to set default by yourself for all vim files when you don't want to use some setting that you set before you just add " in front of that setting like this "set expandtab or when you want to delete all you can do that by rm .vimrc it will delete the file

* in .vimrc *set number* is use to show line numbers
* in .vimrc *set tabstop=4* is use to tab width = 4 spaces
* in .vimrc *set expandtab * is use tabs are spaces
* in .vimrc *set autoindent* is use to auto indent new lines
* in .vimrc *set ignorecase* is use to case-insensitive search
* in .vimrc *set hls* is use to highlight search matches
* in .vimrc *set number* is use to show line numbers

Note: you can paste words from outside by enter insert mode and left click to paste it

**PIPES and SHELL commands/utilities note 15/07/2025**

* you can use *cat [file name]* you can see content inside that file
* you can sent output of command in to other file by do this *[command] > [file name]*\
example: date > currenTime.txt
* to prevent the old file getting overwrite from new file you can use *set -o noclobber* it will\
 cancel the command that will overwrite old file but if you want to bypass it you can use *[command] >| [file name]*\
  this will make you bypass noclobber and when you want to cancel noclobber use this *set +o noclobber*

Note: Redirecting Error use to hide store adjust log for error

* redirect only error using *ls -l file1 noFile 2>error.txt* this will redirect error message to error.txt
* redirect to different files using *ls -l file1 noFile 1>out.txt 2>error.txt* this will redirect output to out.txt and error to error.txt
* redirect to just one file using *ls -l file1 noFile 1>out.txt 2>&1* this will redirect output and error to the same file
* you can use *wc* to count line word byte in file *wc <file.txt*

Note: PIPES is like a chain commands that will start to execute first output from first command then use that output to do next command and then
use second output to do\
next command think like first output is turn into stdin for second input\
example: command1 | command2 | command3

*who the fuck is bathing*

**PIPES & SHELL commands/utilities note 17/07/2025**

*JOB CONTROL*
* *Jobs* running user task and run command or set of cmds entered on one command line

*Foreground Jobs*
* job that run by controller on user no other job can start while Foreground Jobs is running
* you can cancel the job by *ctrl + c*
* you can pause the job by *ctrl + z*
* to resume use *fg* or put into Background Job *bg*

*Background Job*
* is a job that run without display
* is a job that run while other job is running use when there is a job that have to run for a long time 
* usually do the job that doesn't require input

*Job Cycle*
* start as a background job *bg %1*
* start as a foreground job *fg %1*
* terminating a background job *kill %1*

**UNIX File System & Permissions note 17/07/2025**

*Filenames*
* start with alphabet and use (_ , . , -) to separate part of the name
* don't need file surname when create file you put file surname just to make human understand
* don't start with . in front of file name or file will be hidden and won't show up when you use ls
* don't use slash in filename

Note: tty is using to locate the filename that terminal is connect to 

**Unix N Linux note 21/07/2025**
* *touch* is use to change timestamp of file to update and access time in file to modifier the time to current
* *cal* and *ncal* is use to show the calendar *ncal* will have a highlight on current date

Fun Fact: *echo* can do more than you think it can adapt to use with many other command that need to be output so when\
you think of something like output from many command in one line think about *echo* first

* *rm* is use to delete file *rm [filename]*
* *uname* use to output system information 

**Unix Filesystems note 24/07/2025**

* Unix filesystems is like a tree root of directories that each root has their own root of directories that chained together in each root can store specific file or folder that relate to it name

/
├── bin/\
│&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── ls\
├── home/\
│    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── user/\
│       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;├── file.txt\
│       &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── documents/\
│           &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── report.doc\
└── etc/\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;└── password

* *inode* is like id for a file that system use it to locate actual data blocks on disk (system will start to look at inode when you enter that directory)

* drwx------\
  | &nbsp; | &nbsp;&nbsp;&nbsp; |&nbsp;&nbsp;&nbsp; | \
  | &nbsp; | &nbsp;&nbsp;&nbsp; |&nbsp;&nbsp;&nbsp; |-- *---* mean other permission if it get three dats like this it mean you have no permission\
  | &nbsp; | &nbsp;&nbsp;&nbsp; |---- *---* mean group permission if it get three dats like this it mean you have no permission\
  | &nbsp; |\
  | &nbsp; |----*rwx* mean owner's permissions   read, write, execute\
  |\
  |-------*d* mean directory

  &nbsp; ^\
  &nbsp;&nbsp;  |\
  Note: first dat is file type indicators next three dats are permission of owner next three dats are permission of group last three dats are permission of other

  * *owner* is the user who own the file (or creator)
  * *group* users who associate or part of the group assigned to the file
  * *others* everyone else on the system who is not the owner or in the group

  **Note Advance bash commands 31/07/2025**

  * *uniq* use to sort or filter duplicate lines in file *uniq [option] [file] [outfile]
  * *vim -d* use to check different between file can use to check different between old and new version of file or program
  * *dif* can use to check different between file too
  * *tar* use to pack file like zip file