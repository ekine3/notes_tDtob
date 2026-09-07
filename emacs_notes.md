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

## Deleting  
To delete text we can use *d* and the *del* key to delete the text next and before the cursor; we can combine this two keys with *C* for characters, *M* for words and *C-k* for the end of the line and *M-k* for the end of the sentence. To delete selected text use *C-space* and after that *C-w*.  

## Visual mode  
You can select text using *C-space* to select text and using navigation commands.

## Undo changes
To undo changes we can use *C-/* (command plus slash), command that do not change the text can't be undone. *C-_* works the same and works as an alternative in some text terminals. 

## Search  
Emacs can do searches for strings either forward or backwards through the text. *C-s* does forward search and *C-r* does reverse search. The name of the command is "incremental", when you start *C-s* "I-search" appears as prompt in the echo area, then you can enter the search character by character; new instances of *C-s* shows the next coincidence of the search and *Return* terminates the command. 

## Copy and yank
In some instances of Emacs the command to yank text is *M-w* and *C-y* to paste. I did noticed that in GNU Emacs built in tutorial the commands are inverted, maybe it's an error in the version of GUI I have or something else.

## File management  
To Open a file use *C-x* and *C-f*. To Save a file use *C-x* and *C-w*.


# Session  
To end the emacs session type *C-x C-c*, two characters.  
To quit a partially entered command *C-g*.  
To stop the tutorial *C-x k* then *Return*.


## Cheat page  
|Action|Command|Key|Notes|  
| --- | --- | --- | --- | 
|Cancel command|C|g||  
|Go the beginning of the document|M|<||  
|Go the end of the document|M|>||  
|Move to the beginning of a line|C|a||
|Move to the end of a line|C|e||
|Quit a partially entered command|C|g||
|End emacs session|C|xc|two commands|
|Delete the next character|C|d||
|Kill the word before the cursor|M|del||
|Kill the word next the cursor|M|d||
|Kill from the point to the end of line|C|k||
|Kill from the point to the end of sentence|M|k||
|Delete selected text|C|w||
|Select text|C|space||
|Search|C|s|Return key terminates the search|
|Undo changes|C|/||
|Yank or copy text|M|w||
|Paste text|C|y||
|Save file|C|xw|two commands|
|Open file|C|xf|two commands|
|Exit emacs|C|xc|two commands|


## References  
* Wikipedia (2026). *Emacs*.   
    * <https://en.wikipedia.org/wiki/Emacs>

* Sung Phil and Free Software Foundation (2026). *A guided tour of Emacs*.
   * <https://www.gnu.org/software/emacs/tour/>
