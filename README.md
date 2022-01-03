# Gambas Shell
### I would really appreciate some feedback!
If you are cloning or forking this project, I would really appreciate some feedback and suggestions
from everyone who is using or trying to use this shell.

### Also if you would like to contribute to this project please drop me an email!

## New Install process
To install the latest version of gsh and its dependencies, download and install the gshinstall for your distribution\
Listed are the keys to each distribution version:\
```
fedora/red hat/centos   - gshinstall-......fdr.noarch.rpm
opensuse/suse           - gshinstall-.....suse.noarch.rpm
Ubuntu/kbuntu/mint...   - gshinstall_....._0ubuntu._all.deb
debian and derivitives  - gshinstall_...._all.deb
```
Then run the command:\
```
   sudo gshinstall
```   
from the command line after the installation completes.

This supports ubuntu/kubuntu/mint.., fedora/redhat/centos, debian
or derivatives of these root distros.

[What's new](https://github.com/justlostintime/GambasShell/wiki/What's-New)

See the detailed documentation at: https://github.com/justlostintime/GambasShell/wiki

Source Code can be found here : https://github.com/justlostintime/gsh

And Here : https://github.com/justlostintime/sharedmem

## Requires gambas
Requires the latest version of gambas. [See the documentation on the wiki](https://github.com/justlostintime/GambasShell/wiki)
The latest stable release for openSUSE can be installed with one click [here](https://software.opensuse.org/package/gambas3)

### Last update error cd and other builtin subroutines required quote around path names
This has been resolved with this fix

### Update asap to the latest version
The commit 1.3.34-36  had an error I induced that causes redirection to fail and exported environment variables to fail on the cli.\ 
New: The latest Version now supports embedded cli into a gambase statement. For example:
```
if `ls | tr [a-z] [A-Z] > $a` = 0 then 
  print $a
else
  echo the cli failed
endif
```
Any cli command line may be enclosed in back ticks \` and may be used anywhere in a gsh script that 
a gambas function can be used. Note that this differs from thier use in BASH/CSH.

### Something to note when using gsh
In gsh subroutines/Functions/Procedures are not gsh script they are gambas plugins to the gsh shell
they support the Alias process and cli interface but you can not use the Edit/listing etc internal commands.
To do that you need to author a gsh script file.
Example:
```
vim MyScript
   add Content Like:
#!/usr/bin/gsh
ls /
{
 dim a as integer = 1
 print a
 list
}
$b = [1,2,3,4,5]
edit $b
?? $b
 
   Then save the file and do: 
 chmod 766 MyScript
 ./MyScript
```
### Updated Wiki with getting started - intro to gsh
First pass at an into guide.. Will be adding more in the future.

### The latest release 1.3 has a large number of fixes and enhancement, with simplifications of much of the shell
the install packages may be downloaded using the following command examples, substitute your package version as needed.
Adding the plugin commands : 
```
    browse       - open the current directory in the default filebrowser
    google       - open the fierfox or chrome browser with the provided search results
    
Two new clipboard functions have been added, they both require that xclip be installed

    toclipboard   - copy the content of a file to the clipboard. With an alias of tcb
    fromclipboard - print the content of the clipboard to std out.with an alias of fcb
    
    Examples:
       open the default file browser   - browse "/"
       do a internet lookup            - google "fast cars"
       Write to clipboard              - tcb "myfile.txt"
       view content of clipboard       - !fcb | less 
       Capture clipboard to a file     - !fcb > "myfile"...
       Capture clipboard to a variable - !fcb > $a
```
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
