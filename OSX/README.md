The key to understanding what all this means it is important first understand the difference between a login shell and a non-login shell.

Types of Shells
A login shell is when you are logging in remotely to another machine via ssh. You generally need to login.

A non-login shell is when you are already logged into your desktop and you open up the terminal app. You will have noticed that when you open up terminal in OSX, you don’t have to login so it is a non-login shell.

The reason why this is important is because the startup file that is used depends on which shell you are using (bash or tsch etc) and whether it is a login shell or non-login shell.

Order of Execution
When a login shell starts up, it reads the files in the following order:

/etc/profile
~/.bash_profile or
~/.bash_login or
~/.profile
It only reads one of these files and reads the first one it encounters.

When a non-login shell starts up, it reads

/etc/bashrc” and then
~/.bashrc
OSX Quirk
For OSX, all terminal apps counter intuitively open up as login shells. Go figure. You can test this out by adding echo “*** now executing .bash_profile” as the first line of .bash_profile and the same for .bashrc and .profile. Then open up terminal and see what gets echoed out in what order. (In my home directory I only have .bashrc and .bash_profile so I’d have to create a .profile)

Sources:

http://michael-rushanan.blogspot.co.nz/2013/01/os-x-bashrc-vs-profile-vs-bashprofile.html
http://hayne.net/MacDev/Notes/unixFAQ.html#shellStartup
