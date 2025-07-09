# linux-practice-link

https://www.geeksforgeeks.org/difference-between-linux-and-windows/

https://www.geeksforgeeks.org/architecture-of-linux-operating-system/

https://www.geeksforgeeks.org/difference-between-hard-link-and-soft-link/

https://github.com/PrashantDongarwar/Linux-Interview-Questions

https://www.geeksforgeeks.org/open-systems-interconnection-model-osi/

https://www.geeksforgeeks.org/differences-between-tcp-and-udp/

https://www.cyberciti.biz/faq/understanding-etcshadow-file/

## linux_basic_commands :-

| Command            | Use (Short Description)                               |
| ---------------------- | ---------------------------------------------------------- |
| `hostname`             | Shows the name of your system.                             |
| `pwd`                  | Shows the current directory path.                          |
| `cd /`                 | Changes directory to root (`/`).                           |
| `ls`                   | Lists files and folders in current directory.              |
| `cd /root`             | Goes to root user's home directory (needs sudo).           |
| `cd /mnt`, `cd /media` | Access mounted storage devices or drives.                  |
| `cd home`, `cd /home`  | Moves to home directory.                                   |
| `cd ubuntu`            | Enters the "ubuntu" user's folder (inside /home).          |
| `touch file1`          | Creates an empty file named `file1`.                       |
| `mkdir demo`           | Creates a new directory called `demo`.                     |
| `ls -l`                | Lists files with detailed info (permissions, owner, size). |
| `clear`                | Clears the terminal screen.                                |
| `ls /home/`            | Lists contents of `/home` from any location.               |
| `cal`                  | Shows the current month's calendar.                        |
| `apt install ncal`     | Installs `ncal` (an improved calendar tool).               |
| `apt update`           | Updates the list of available packages.                    |
| `cal -3`               | Shows calendar for previous, current, and next month.      |
| `uname -a`             | Shows all system information.                              |
| `uname -s`             | Shows operating system name only.                          |
| `uname`                | Default – shows OS name (same as `uname -s`).              |

touch file.txt --------- create file at current location
touch /home/data.txt ----- create file inside home directory   
touch project.txt project1.txt -------- create multiple files at present working directory  
touch /mnt/imp.txt /root/abc.txt /home/xyz  ------ create multiple files in different_different locations
touch /root/{data.txt,file1.txt,projectfile.txt} ------- create multiple file at different location
touch file{1..20}.txt  -------- create 20 files with same name in single command
touch .imp.txt  -------- to create hidden file
ls -a -------- to list hidden files.


## Hierarchy Of Linux file system :
1) /root ------- root directory is a home directory of root user *
2) /home ------ it is a home directory of local users*
3) /etc ------- it stores all configurations files of system and services *
4) /bin ------- it stores binary files, binary file means nothing but our commands (local user commands)
5) /sbin ------ it stores system binary executable files, commands----- (root user command)
6) /var ------ it stores variable data such as, mail, logs, messages etc.... *
7) /lib32 ------ library file information, support 32 bit commands
8) /lib64 ------ library file information, 64 bit supporting files 
9) /boot ------- it store boot loader and other booting files that helps to start our system
10) /dev ------- it stores device related information, usb drives, printer, 
11) /media ----- information of removable devices, card reader, pen drives, floppy disk
12) /sys ------- system related information
13) /run ------ store the information of all running devices
14) /proc ----- it stores the process related information, it store information related RAM and CPU
15) /tmp ------ it stores temporary file for 10 days
16) /usr ------ it store user related information, man pages
17) /srv ------ it stores service related information
18) /mnt ------ it store mount point for our storage devices ex : hard disk*
19) /opt ----- optional directory, addon services information

## File operation :

READ :-
 1) cat  ----------- use to read the file which have small amount of data
 2) more ----------- you can scroll the data downward using enter command, but you cant scroll upward
 3) less ----------- you can scroll upward and downward using upper arrow key and lower arrow key. 
                     Press Q (quite) to return on terminal  
 4) head ----------- by default it will show top 10 lines
    head -n <no> <file name>
    ex : head -n 5 /etc/passwd --------- it will show top 5 lines
5) tail ------------ by default it will show bottom 10 lines
    tail -n 15 /etc/passwd ------- it will show bottom 5 lines

  ## **vim editor 
    1) command mode
    2) Insert mode
    3) Execution mode
    4) Visual mode

    #1) Command mode :
       1. G -------- move cursor at end of file, bottom of the file
       2. gg ------- move cursor at top of the file
       3. yy ------- for copy the line where your cursor is present
       4. <number>yy -- copu no of lines 
       5. yw ------- copy the single world
       6. <number>yw copy no of words
       7. p ------- for paste the line to below the cursor
       8. P ------- paste the line at top of cursor
       9. dd ------ for delete the line
       10. <n>dd ----- delete nimbers of line
       11. dw -------- delete the word 
       12. <n>dw ----- delete the numbers of words
       13. cc ------ for cut the line
       14. <n>cc ------ cut number of lines
       15. cw ------- for cut the single word
       16. <n>cw ------ for cut the multiple words
       17. /<word> ----- search the perticular word
               n ---- move forward 
               N ---- move backward
       18. u -------- undo the changes
       19. ctrl+r ------- redo the changes

    #2) Insert mode : 
       - Edit the data manually
      1) i -insert text at current cursor position 
      2) I -insert text at start of the current line 
      3) a -insert text just right of the current character 
      4) A -insert text at end of the current line 
      5) o -insert new line below the current line 
      6) O -insert new line above the current line 
      7) r -it replaces single character 
      8) R -replace multiple characters 


    #3) Execution mode : 
       - Type ":" to insert into execution mode
       1. :q ------ quit without saving the file
       2. :q! ------ quit forcefully without saving the file 
       3. :w ------- save the changes and stay in file
       4. :wq or :x or :exit ------ save the changes and quit the file
       5. :wq! or :x! ------ save the change and quit the file forcefully
       6. :set nu ------- set line numbers
       7. :set nonu ------ remove the line numbers
       8. :/<word> ------ search the word
       9. :set hlsearch ---- highlight the search word
       10 :nohl -------- remove the highlighting
       11. :%s/<oldword>/<newword>/g ------ find the word and replace it with new word
       12. :!touch /home/file.txt -------- execute any command on terminal without leaving the editor

    #4) Visual mode :
       - V --------- select line by line
       - v --------- select character by character

         y,d,c -------- for copy, delete, cut

## Managing Users and Permissions in Linux :-

       A user is a person who utilizes a computer or network service. Linux is said to be secure 
       because one user cannot access files of other user without its permission. There are three types of user, 

       1. Super user/root user: Super users are those users who has all privileges of Linux system. On all 
          Linux systems, by default there is the user root, also known as the super user. This account is used for 
          managing Linux. Root, for instance, can create other user accounts on the system. For some tasks, 
          root privileges are required. Some examples are installing software, managing users, and creating 
          partitions on disk devices.  

       2. System user: System accounts are used by the services in Linux system. These 
          accounts or users generally created when services are installed in system. 

       3. Standard user(Local user): local user accounts or standard user accounts are for the people who 
          need to work on a system and who need limited access to the resources on that system. These user 
          accounts typically have a password that is used for authenticating the user to the system.






sakshi:   x:  1001:   1001:   sakshi wadkar,,12345678,0987654:  /home/sakshi:   /bin/bash

username pw   UID    GID     additional info of user        home dir    user_login_shell



sakshi:         x:                        1001:     

group_name  password from gshadow file    GID    group members




sakshi        :!          :             :

group name  password    group admin    group members


## commands managing user and permission :

    1  whoami
    2  exit
    3  adduser chanchal
    4  cd /home
    5  ls
    6  su - chanchal
    7  su chanchal
    8  exit
    9  useradd ninad
   10  su ninad
   11  cd /home
   12  ls
   13  userdel ninad
   14  cd /var/spool/mail
   15  ls
   16  cd ../../
   17  cd ../
   18  cat /etc/passwd
   19  cat /etc/shadow
   20  cat /etc/group
   21  cat /etc/gshadow
   22  cat /etc/passwd
   23  userdel chanchal
   24  tail -5 /etc/passwd
   25  cd /home
   26  ls
   27  adduser shweta
   28  tail -5 /etc/passwd
   29  ls /home
   30  userdel -r shweta
   31  ls
   32  tail -5 /etc/passwd
   33  adduser pawan
   34  tail -2 /etc/passwd
   35  tail -3 /etc/group
   36  cat /etc/shells
   37  echo $SHELL
   38  tail /etc/shadow
   39  tail -3 /etc/passwd
   40  cat /etc/passwd
   41  cat /etc/group
   42  cat /etc/gshadow
   43  tail -3 /etc/passwd
   44  man usermod
   45  ls
   46  cd ubuntu/
   47  ls
   48  ls -a
   49  cd /etc/skel/
   50  ls
   51  ls -a
   52  cd /
   53  cd home
   54  ls
   55  cd chanchal/
   56  ls -a
   57  cd ..
   58  ls
   59  cd pawan/
   60  ls -a
   61  cd ..
   62  ls'
   63  cd chanchal/
   64  ls -a
   65  cat .bash_history
   66  alias t=touch
   67  ls
   68  t file.txt
   69  ls
   70  cd /root
   71  ls -a
   72  vim .bashrc
   73  m demo
   74  source .bashrc
   75  m demo
   76  ls
   77  history
    1  tail -3 /etc/passwd
    2  tail -3 /etc/group
    3  passwd ninad
    4  passwd shweta
    5  tail -3 /etc/passwd
    6  usermod -u 5001 shweta
    7  tail -3 /etc/passwd
    8  tail -3 /etc/group
    9  usermod -c "Cloud engineer" shweta
   10  tail -3 /etc/shadow
   11  tail -3 /etc/passwd
   12  su - shweta
   13  usermod --info
   14  usermod -d /mnt shweta
   15  tail -3 /etc/passwd
   16  su - shweta
   17  tail -3 /etc/passwd
   18  su - shweta
   19  cat /etc/shells
   20  usermod -s /bin/sh shweta
   21  tail -3 /etc/passwd
   22  su - shweta
   23  tail -3 /etc/passwd
   24  usermod -s /bin/bash shweta
   25  tail -3 /etc/passwd
   26  history
   27  tail -3 /etc/passwd
   28  adduser pawan
   29  tail -3 /etc/passwd
   30  tail -3 /etc/shadow
   31  chage -l
   32  chage -l shweta
   33  chage -m 10 shweta
   34  chage -l shweta
   35  su - shweta
   36  chage -l shweta
   37  chage -M 90 shweta
   38  chage -l shweta
   39  date
   40  date -s "7 may 2025"
   41  date
   42  su - shweta
   43  chage -l shweta
   44  chage -W 10 shweta
   45  chage -l shweta
   46  chage -I 30 shweta
   47  chage -l shweta
   48  chage -E "jul 06 2025" shweta
   49  chage -l shweta
   50  tail -3 /etc/shadow
   51  usermod -L shweta
   52  su - shweta
   53  su - ubuntu
   54  cat /etc/group
   55  history

   4. /etc/passwd --- user information

           ashwini:       x:                 1000:   1000:  ,,123456789,,DevOps engineer:  /home/ashwini:     /bin/bash      
         (user name) (encrypted password)   (UID)   (GID)         (comment)               (home directory)   (user login shell) 
         
         root user ------UID------ 0
         system user ----UID range ---- 1-999
         local user -----UID range ---- 1000-

         passwd <username> ------ provide password to user
         
      commands for user modifications: 
         usermod <option> <parameter> <username>

        1) usermod -l <new_name> <old_name>  
        2) usermod -u 2000 nikita     -------- for change the userid UID
        3) usermod -c "devops engineer" nikita ------- change the comment
        4) usermod -d /mnt <user_name> -------- chnage home dir of user to mnt
        5) usermod -s /bin/sh <user_name> ----- change user login shell
        6) usermod -L <user_name> ------ Lock user account
        7) usermod -U <user_name> ------ unlock user account


   5. /etc/shadow 
       ----- user passowrd informaton

      ubuntu:$y$j9T$KBrdN4tKMbqQGaWziO0f50$s2fELyTr6Vl8gaRR42Woq3uHGIQwE4Y9U.5B/gmU6C3:20182:10:90:10:30:20333:
            
      1. Username: This is a unique name for the user. User names are important to match a 
         user to his password. On Linux, there can be no spaces in the user name. 
      2. Encrypted password: This field contains all that is needed to store the password in a secure way. 
      3. Days since Jan 1, 1970, that the password was last changed: Many things on Linux 
         refer to this date, which on Linux is considered the beginning of days. 
      4. Days before password may be changed: This is minimum age of password. That means user cannot change password,
         before the mentioned days, after immediately changing the password. Typically this field is set to the value 0. 
      5. Days after which password must be changed: This field contains the maximal validity 
         period of passwords or maximum age of password. User must have to change their password after mentioned days. 
         By default it is set to 99999 days. 
      6. Days before password is to expire that user is warned: This field is used to warn a 
         user when a forced password change is upcoming. By default it is set to 7 days. 
      7. Days after password expires that account is disabled: Use this field to enforce a 
         password change. After password expiry, users can no longer log in. 
      8. Days since Jan 1, 1970, that account is disabled: An administrator can set this field to 
         disable an account. This is typically a better approach than removing an account, as 
         all associated properties and files of the account will be kept, but it can be used no 
         longer to authenticate on your server. 
      9. For future use: This is reserved field for future use. 
## commands :
   syntax; 
   chage <option> <parameter> <username>

   chage -l <username> ------- list the password onformation
   chage -m <username> ------- change minimum days between password change
   chage -M <username> ------- maximum password age
   chage -W <username> ------- warning days
   chage -I <username> ------- password inactive days
   chage -E <username> ------- account expired

   







































































