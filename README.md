# GambasShell
Gambas shell gsh for linux required Gambas3 3.14.90 or higher

Only the Ubuntu version/linux mint have been well tested so far.
So be careful with the other. Please report any issues thanks.

With update 1.2.65 the structure of the shell commands has changed.
So if your updating from a revision before 1.2.65 then please run clearsubs on the
first start, exit gsh and restart it. This ensures the use of the new structure.

If your want to use gsh as your login script then add an entry to the /etc/shells
/usr/bin/gsh

Change the defult shell in your user account. Or the /etc/passwd file
depending on your linux release.

See the Wiki for more details: https://github.com/justlostintime/GambasShell/wiki

Or 

See the detailed documentation at:https://github.com/justlostintime/GambasShell/wiki/Documentation
