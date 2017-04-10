

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. 

*/home/cabox/workspace                                                                                                                                                
cabox@box-codeanywhere:~/workspace$*

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  super_scavengers.md*                                                     

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory.*

*total 40K                                                                                                                                                         
drwxrwxr-x 4 cabox cabox 4.0K Apr  9 23:18 .                                                                                                                         
drwxr-xr-x 9 cabox cabox 4.0K Apr  9 23:18 ..                                                                                                                        
drwxrwxr-x 8 cabox cabox 4.0K Apr  9 23:18 .git                                                                                                                      
-rw-rw-r-- 1 cabox cabox 1.1K Apr  9 23:18 LICENSE                                                                                                                   
-rw-rw-r-- 1 cabox cabox 2.7K Apr  9 23:18 README.md                                                                                                                 
drwxrwxr-x 7 cabox cabox 4.0K Apr  9 23:18 challenge_files                                                                                                           
-rw-rw-r-- 1 cabox cabox 5.5K Apr  9 23:18 nix_scavenger_hunt.md                                                                                                     
-rw-rw-r-- 1 cabox cabox  317 Apr  9 23:18 nix_scavenger_hunt_stretch.md                                                                                             
-rw-rw-r-- 1 cabox cabox  191 Apr  9 23:18 super_scavengers.md*

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. 

* -a, --all
      do not hide entries starting with .
 -l   use a long listing format
 -h,  --human-readable
      print sizes in human readable format (e.g., 1K 234M
      2G)*
              
* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. 

*bin  boot  dev  etc  fastboot  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var                                                     
*

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) 

*/*

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. 

*/home/cabox                                                                                                                                                          
*

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. 

*3: 2015_special_stuff.demo  cloaked-wookie.demo  scooter-double-mamba.demo                                                                                              
*

* Use the `cd` command to move "up" one directory. 

*/home/cabox                                                                                                                                                          
*

* Press the up arrow on your keyboard. 

*I got the pwd command.*

* Press the up arrow a few more times. 

*I got ls and cd commands.*

* Run the `history` command. 

*    8  cd /                                                                                                                                                          
    9  pwd                                                                                                                                                           
   10  cd /                                                                                                                                                          
   11  pwd                                                                                                                                                           
   12  cd                                                                                                                                                            
   13  cd /                                                                                                                                                          
   14  cd/                                                                                                                                                           
   15  cd ~                                                                                                                                                          
   16  pwd                                                                                                                                                           
   17  cd challenge_files                                                                                                                                            
   18  cd /                                                                                                                                                          
   19  cd challenge_files                                                                                                                                            
   20  clear                                                                                                                                                         
   21  cd challenge_files                                                                                                                                            
   22  pwd                                                                                                                                                           
   23  ls                                                                                                                                                            
   24  cd home                                                                                                                                                       
   25  cd challenge_files                                                                                                                                            
   26  cd home ls                                                                                                                                                    
   27  cd home                                                                                                                                                       
   28  ls                                                                                                                                                            
   29  cd cabox                                                                                                                                                      
   30  ls                                                                                                                                                            
   31  cd workspace                                                                                                                                                  
   32  ls                                                                                                                                                            
   33  cd challenge_files                                                                                                                                            
   34  ls                                                                                                                                                            
   35  grep <.demo><file>                                                                                                                                            
   36  grep <.demo>                                                                                                                                                  
   37  grep <demo>                                                                                                                                                   
   38  ls *.{demo}                                                                                                                                                   
   39  cd workspace                                                                                                                                                  
   40  cd cabox                                                                                                                                                      
   41  pwd                                                                                                                                                           
   42  cd challenge_files                                                                                                                                            
   43  ls *.{demo}                                                                                                                                                   
   44  ls *.demo                                                                                                                                                     
   45  pwd                                                                                                                                                           
   46  cd                                                                                                                                                            
   47  ls                                                                                                                                                            
   48  pwd                                                                                                                                                           
   49  cd                                                                                                                                                            
   50  ls                                                                                                                                                            
   51  history *

### Observing the System

* Discover what account you are logged into using the `whoami` command. 

*cabox*

* Discover who else is on your system with the `who` command. 

*No, just me.*

* How long has your system been running? Use `uptime` to see, and 

*cabox    pts/0        Apr  9 23:20 (54.69.152.243)                                                                                                                   
*

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) 

*USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND                                                                                             
root         1  0.0  0.4  33196  2584 ?        Ss   23:17   0:00 init                                                                                                
root         2  0.0  0.0      0     0 ?        S    23:17   0:00 [kthreadd/109251]                                                                                   
root         3  0.0  0.0      0     0 ?        S    23:17   0:00 [khelper/1092516]                                                                                   
root       151  0.0  0.1  19428   832 ?        S    23:17   0:00 upstart-udev-bridge --daemon                                                                        
root       166  0.0  0.2  49216  1416 ?        Ss   23:17   0:00 /lib/systemd/systemd-udevd --daemon                                                                 
syslog     327  0.0  0.2 184188  1436 ?        Ssl  23:17   0:00 rsyslogd                                                                                            
root       396  0.0  0.1  15472   952 ?        S    23:17   0:00 upstart-socket-bridge --daemon                                                                      
root       409  0.0  0.5  61316  3052 ?        Ss   23:17   0:00 /usr/sbin/sshd -D                                                                                   
root       425  0.0  0.1  15492   848 ?        S    23:17   0:00 upstart-file-bridge --daemon                                                                        
root       445  0.0  0.1  12740   832 tty1     Ss+  23:17   0:00 /sbin/getty 38400 console                                                                           
root       447  0.0  0.1  12740   848 tty2     Ss+  23:17   0:00 /sbin/getty 38400 tty2                                                                              
root       481  0.0  0.6  63876  3460 ?        Ss   23:19   0:00 sshd: cabox [priv]                                                                                  
cabox      483  0.0  0.2  63876  1472 ?        S    23:19   0:00 sshd: cabox@pts/0                                                                                   
cabox      484  0.0  1.0  21480  5412 pts/0    Ss   23:19   0:00 -bash                                                                                               
cabox      698  0.0  0.2  15520  1148 pts/0    R+   23:59   0:00 ps aux

Looks like it's giving me a run down of all the processes run in the dev box.*

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) 

*Looks like it's giving me a run down of my use of the system.*

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. 

*2: credit_cards.txt  credit_cards2.txt                                                                                                                                  
*

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) 

*01-15-2015 *

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. 

*./challenge_files/tmp/modi_laboriosam.txt                                                                                                                            
*

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). 

*2: Britt-Erdman.user
Lissie-Strosin.user*

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. 

*./challenge_files/serial-numbers/eaque_molestiae.txt:4:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt cons
*

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. 

*LICENSE                                                                                                                                                              
README.md                                                                                                                                                            
challenge_files                                                                                                                                                      
files.txt                                                                                                                                                            
nix_scavenger_hunt.md                                                                                                                                                
nix_scavenger_hunt_stretch.md                                                                                                                                        
super_scavengers.md              *

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. 

*
-rw-rw-r-- 1 cabox cabox   91 Apr  9 23:18 Kirstin-Hoppe.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   93 Apr  9 23:18 Kwame-Schmitt.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   78 Apr  9 23:18 Ladonna-Lueilwitz.user                                                                                                    
-rw-rw-r-- 1 cabox cabox   64 Apr  9 23:18 Lala-Will.user                                                                                                            
-rw-rw-r-- 1 cabox cabox   71 Apr  9 23:18 Leia-Hudson.user                                                                                                          

-rw-rw-r-- 1 cabox cabox   76 Apr  9 23:18 Leia-Ziemann.user                                                                                                         
-rw-rw-r-- 1 cabox cabox   87 Apr  9 23:18 Lillard-Purdy.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   67 Apr  9 23:18 Lilly-Kohler.user                                                                                                         
-rw-rw-r-- 1 cabox cabox   70 Apr  9 23:18 Lissie-Strosin.user                                                                                                       
-rw-rw-r-- 1 cabox cabox   73 Apr  9 23:18 Mannie-Ritchie.user                                                                                                       
-rw-rw-r-- 1 cabox cabox  104 Apr  9 23:18 Masako-Lind.user                                                                                                          
-rw-rw-r-- 1 cabox cabox   89 Apr  9 23:18 Melisa-Yundt.user                                                                                                         
-rw-rw-r-- 1 cabox cabox   90 Apr  9 23:18 Michelina-Kuphal.user                                                                                                     
-rw-rw-r-- 1 cabox cabox   93 Apr  9 23:18 Minnie-Jacobi.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   80 Apr  9 23:18 Murdock-Leffler.user                                                                                                      
-rw-rw-r-- 1 cabox cabox   77 Apr  9 23:18 Mychal-Corkery.user                                                                                                       
-rw-rw-r-- 1 cabox cabox   74 Apr  9 23:18 Nakita-Nader.user                                                                                                         
-rw-rw-r-- 1 cabox cabox   68 Apr  9 23:18 Nayely-Dare.user                                                                                                          
-rw-rw-r-- 1 cabox cabox   76 Apr  9 23:18 Nicholas-Strosin.user                                                                                                     
-rw-rw-r-- 1 cabox cabox   88 Apr  9 23:18 Niles-Runte.user                                                                                                          
-rw-rw-r-- 1 cabox cabox   81 Apr  9 23:18 Nina-Sporer.user                                                                                                          
-rw-rw-r-- 1 cabox cabox   70 Apr  9 23:18 Noreta-Steuber.user                                                                                                       
-rw-rw-r-- 1 cabox cabox   79 Apr  9 23:18 Ovid-Bogan.user                                                                                                           
-rw-rw-r-- 1 cabox cabox   78 Apr  9 23:18 Randell-Sauer.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   78 Apr  9 23:18 Remy-Renner.user                                                                                                          
-rw-rw-r-- 1 cabox cabox  103 Apr  9 23:18 Ronna-Hermann.user                                                                                                        
-rw-rw-r-- 1 cabox cabox  100 Apr  9 23:18 Rosalind-Wisozk.user                                                                                                      
-rw-rw-r-- 1 cabox cabox  102 Apr  9 23:18 Rosena-Simonis.user                                                                                                       
-rw-rw-r-- 1 cabox cabox   96 Apr  9 23:18 Sandie-Balistreri.user                                                                                                    
-rw-rw-r-- 1 cabox cabox   93 Apr  9 23:18 Sharen-Hansen.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   97 Apr  9 23:18 Sherrill-Russel.user                                                                                                      
-rw-rw-r-- 1 cabox cabox   84 Apr  9 23:18 Sherwin-Kovacek.user                                                                                                      
-rw-rw-r-- 1 cabox cabox   96 Apr  9 23:18 Sherwood-Rath.user                                                                                                        
-rw-rw-r-- 1 cabox cabox   77 Apr  9 23:18 Shyheim-Murazik.user                                                                                                      
-rw-rw-r-- 1 cabox cabox   96 Apr  9 23:18 Siobhan-Kirlin.user                                                                                                       
-rw-rw-r-- 1 cabox cabox   75 Apr  9 23:18 Tomas-Kutch.user                                                                                                          
-rw-rw-r-- 1 cabox cabox    0 Apr  9 23:18 cloaked-wookie.demo                                                                                                       
-rw-rw-r-- 1 cabox cabox  16K Apr  9 23:18 credit_cards.txt                                                                                                          
-rw-rw-r-- 1 cabox cabox  16K Apr  9 23:18 credit_cards2.txt                                                                                                         
-rw-rw-r-- 1 cabox cabox    0 Apr  9 23:18 scooter-double-mamba.demo                                                                                                 
drwxrwxr-x 2 cabox cabox 4.0K Apr  9 23:18 serial-numbers                                                                                                            
drwxrwxr-x 2 cabox cabox 4.0K Apr  9 23:18 test2                                                                                                                     
drwxrwxr-x 2 cabox cabox 4.0K Apr  9 23:18 tmp                                                                                                                       
drwxrwxr-x 2 cabox cabox 4.0K Apr  9 23:18 wow     *

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. 

*cabox@box-codeanywhere:~/workspace/challenge_files$  ps aux | grep cabox                                                                                             
root      1355  0.0  0.6  63876  3456 ?        Ss   00:36   0:00 sshd: cabox [priv]                                                                                  
cabox     1357  0.0  0.2  63876  1468 ?        S    00:36   0:00 sshd: cabox@pts/0                                                                                   
cabox     1358  0.0  1.0  21544  5484 pts/0    Ss   00:36   0:00 -bash                                                                                               
cabox     1571  0.0  0.2  15520  1144 pts/0    R+   00:56   0:00 ps aux                                                                                              
cabox     1572  0.0  0.1   8816   752 pts/0    S+   00:56   0:00 grep --color=auto cabox   *
