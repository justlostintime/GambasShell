# GambasShell
### I would really appreciate Some feed Back
If you are cloning or forking this project, I would really appreciate some feedback and suggestions
from everyone who is using or trying to use this shell.

### The latest release 1.3 has a large number of fixes and enhancement, with simplifications of much of the shell
the install packages may be downloaded using the following command examples, substitute your package version as needed.
Adding the plugin commands : 
browse - open the current directory in the default filebrowser
google - open the fierfox browser with the provided search results
toclipboard - copy the content of a file to the clipboard.  alias tcb , requires xclip to be installed
fromclipboard - print the content of the clipboard. alias fcb, example !fcb | less , or !fcb > "myfile"...
```
wget https://raw.githubusercontent.com/justlostintime/GambasShell/master/gambas3-westwood-sharedmem_3.15.3-38_all.deb
wget https://raw.githubusercontent.com/justlostintime/GambasShell/master/gsh_1.3.3-0ubuntu18_all.deb
```
See the detailed documentation at: https://github.com/justlostintime/GambasShell/wiki/Documentation

Source Code can be found here : https://github.com/justlostintime/gsh

And Here : https://github.com/justlostintime/sharedmem

### Note: The release 12-27-2020 was a complete mess as far as input output redirection went. Please update to the latest version as soon as possible.

Documentation  for gsh at https://github.com/justlostintime/GambasShell/wiki

Gambas shell gsh for linux required Gambas3 3.15.3 or higher.
This can be used as a complete bash shell replacement. Very useful for education and general scripting of tasks in your system. GSH integrates many of the features of posix shells with the more regular language structure provided by 'GAMBAS almost means BASIC.'

### Tip
If the shell acts strange, delete the ~/var/gsh.image and any /dev/shm/<username>gsh and /dev/shm/<username>col you find there then restart gsh, 
for a clean restart. Use savesubs and saveclass commands often to save your work.
  
#### See more tips here:https://github.com/justlostintime/GambasShell/wiki/Tips-and-Tricks
  
### Whats New
Because of some required features it is now required to have latest gambas3. Sorry but it makes things a little easier. the official release of gambas3 15.3 I believe to be April this year(maybe).
```
Use the ppa 
  sudo add-apt-repository ppa:gambas-team/gambas-daily
  sudo apt-get update
  
  or clone from 
  
  https://gitlab.com/gambas/gambas
  And follow the detailed description to build for your version of linux
```
#### See List of New/Updated Features here: https://github.com/justlostintime/GambasShell/wiki/What's-New

Only the Ubuntu and Mint Versions of linux have been well tested so far.
So be careful with the other. Please report any issues thanks.

With update 1.2.65 the structure of the shell commands has changed.
So if you are updating from a revision before 1.2.65 then please run clearsubs on the
first start, exit gsh and restart it.
Remember to save all your personal subs/functions/procedures before clearing the in memory subs.
This ensures the use of the new structure.

Clearing the subs is a good idea after each release if you can.

Clear subs using : clearsubs ' Subroutines are loaded into the gsh.image on first use 

Save your personal subs using : savesubs "sub1" "sub2" ....

If you want to use gsh as your login script then you must add an entry to the 
    /etc/shells
add this line at the end:
    /usr/bin/gsh

Change the defult shell in your user account. Or the /etc/passwd file
depending on your linux release. 

Better still use 'chsh -e /usr/bin/gsh' command to change your shell. 
Be sure to log out and back in for it to take effect.


See the Wiki for more details: https://github.com/justlostintime/GambasShell/wiki

Or 

See the detailed documentation at:https://github.com/justlostintime/GambasShell/wiki/Documentation

Source Code can be found here : https://github.com/justlostintime/gsh

And Here : https://github.com/justlostintime/sharedmem
