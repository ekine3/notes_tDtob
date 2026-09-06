# Emacs notes  
ediaz  

## What is Emacs?  
Originally named *EMACS* as an acronym for "Editor Macros", is a family of text editor characterized by their extensibility. 
Emacs has over ten thousand built int commands and its interface allows users to combine theses commands into macros to automate work, some implementations typically feature a dialect of the *Lisp* programming language allowing users to write new commands and applications for the editor..  

The most popular and most ported version is GNU Emacs, created for the GNU project. GNU Emacs and Vi are the two main contenders in the traditional editor wars of Unix culture.  

## How to get the application  
We can install the application in Windows 11 using their native package manager:  
```EmacsId
winget search emacs  
winget show GNU.Emacs
winget install GNU.Emacs    
```
![GNU Emacs 31.1 available in Windows Package Manager (winget).  Version, publisher, description license, tags and installer information using "show" command.](https://files.mastodon.social/media_attachments/files/117/225/813/474/064/628/original/4b93805eb110e81c.png)

We can get this application in Debian based distros using *apt*:  
```Installing Emacs in debian
apt-get -y update  
apt-cache search --names-only emacs  
apt-get install emacs  
emacs --version   
```
![GNU Emacs 27,1 cairo version, running in Debian 11, WSL2. Installation through apt, version check and GTK emulation.](https://files.mastodon.social/media_attachments/files/117/226/095/014/532/222/original/efdd9ed37322c77f.png)

GNU Emacs 30.2 package in Arch based distros. Installation in Manjaro, xfce4 terminal using pacman  
```Emacs using pacman
pacman -Syu emacs
pacman -Ss emacs
emacs --version
```
![Gnu emacs in Manjaro](https://files.mastodon.social/media_attachments/files/117/226/278/893/743/743/original/58c5c26f41b37605.png)

## Navigation  
Commands usually involve the *control* key labeled as *CTRL* and the *Meta* key, *ALT*, and tehir abreviations *C-chr* and *M-chr*.  
To view the next screen *C-v*, to vie the previous screen *M-v*,there is a two line overlap between screens for continuity porpuses.  

Clear screeen and redisplay all text *C-l*, first instance of this command center the paragraph in the screen, second try move it to the top and a third one moves it to the bottom. The location of the cursor in a text is called **point**, shows where you are located in the text.  

The movement of the arrows is also possible with *C-p* up, *C-n* down, *C-b* left and *C-f* right (Command previous, next, backwards and forward). 
This movement set up can be speed up using M, moving by words instead of characters (just available for backwads and forward, *M-b* and *M-f*).  

To move to the beginning of a line use *C-a* and *C-e* to get to the end of a line. To move to the beginning of a sentence use *M-a* and *M-e* to the end of a sentence. 
And use *M-<* to move to the beginning of the whole document and *M->* to the end of the whole document.  

## Numeric arguments, prefix arguments
Most commands accept numeric arguments, this serves as a repeat count; these are also called *prefix arguments*, because you type the argument before the command it applies to.  

## Cancel commands  
You can stop commands frozen or that are taking too long to execute using *C-g*, this also works to scape incomplete commands or cancel *ESC* key.  

## Cheat page  

|Action|Command|Key|Notes|  
| --- | --- | --- | --- | 
|Cancel command|C|g||  
|Go the beginning of the document|M|<||  
|Go the end of the document|M|>||  
|Move to the beginning of a line|C|a||
|Move to the end of a line|C|e||
|Quit a partially entered command|C|g||
|End emacs session|C|xc||

# Session  
To end the emacs session type *C-x C-c*, two characters.  
To quit a partially entered command *C-g*.  
To stop the tutorial *C-x k* then *Return*.

## References  
* Wikipedia (2026). *Emacs*.   
    * <https://en.wikipedia.org/wiki/Emacs>   
