# Udemy course: Learn the Linux Command Line 

Course September 6th 2026. Ediaz, notes made in Vim using markdown format.  

Even the course is really simple and short, is useful to set known information about bash and cli application, to understand how Udemy works and to make observations about the course information, the tools and the interface.
## 1. Introduction 

This course is to learn basic commands and properties, we will make our own command to run in unix like terminals aka linux bash.

## 2. What is the Command Line

* A way to directly access your computer 
* other names
    * terminal
    * Bash shell / shell
    * CLI (command line interface)
    * Command prompt / cmd (windows)

Allows direct access: often easier than GUI, has specific command is a good habit.  

**Why is this important?**, is extremely useful in programming, get things done quicker and is a great skill.

## 3. Opening the Command line
In several linux distributions we have an easy access to terminal emulators, often using *ctrl-alt-t*.
The instructor recommends to use "Ask Ubuntu" to get norths on how to use linux terminals.  

## 4. Copy and pasting
To paste from a GUI yank text to a terminal, we have to use the secure paste. *C-v* does not work, so we have to use *C-shift-v*.  

## 5. Using applications: calendar  
To use a calendar in Linux terminal we can use *calendar*. In my case I did not have *calendar* installed in my Debian WSL2, so I first looked up for the application, installed it and use it:

```calendar
apt-cache search --names-only calendar
apt-get install -y calendar
calendar
#we'll get Sep 06  Defense of Pakistan Day in Pakistan
```
## 6. The pwd command  
Using *pwd*  (print working directory) is useful to locate the current directory we are working on. By default we start terminals in the *Home* directory.

```pwd
#if we are in the default directory "~" we would see it through pwd
pwd
#we'll see something like /home/user/
```

## 7.1 Changing Directories
While working in terminals we'll have to change directories.

|Action|Command|
|---|---|
|Go to home directory|cd|
|Go to Videos folder in Home folder|cd ~/Videos|
|Going back one folder|cd ..|

## A survey in the half off the course
I got a survey asking for a star rating (up to five stars) with a opinion box and a "tell us more" form about: the value of information, explanation of concepts, instructors eengaging, opportunities to apply the knowledge, expectations delivery and instructor's knowledge. After filling the review we can see a preview of the rating, that will be public.  
 
## 7.2 Changing Directories
We have can use *autocompletion* in commands so we can speed up changes and use of the files and directories.

|Action|Command|
|---|---|
|To change to a neigboor of a current directory, from ~/Videos to ~/Images|cd ../Images|

To clear a screen we can use *clear* and have more clear view of our working space.

# 8. (In the course sections this is part 9) The ls command  
The *ls* allow us to list the contents of a directory.
Hidden files start with a dot "." by default, we can use *ctrl-h* in some file managers or user *-a* argument in some cli applications.


|Action|Command|
|---|---|
|Print current directory contents|ls|
|View contents of a specific folder|ls ~/Documents/notes|
|View recently changed|ls -t|
|List by size folder|ls --size|
|List more information|ls -l|
|Flip order (from -t argument)|ls -t -r|
|We can see information about the *list* command|ls --help|
|List hidden files|ls -a|
|get into a hidden directory|cd .hidden/|
|print all the files in a folder and sub folders, recursive argument|ls -R ~/Documents/|
|list all the files in home|ls -R|

## 10. Making and deleting directories

|Action|Command|
|---|---|
|create a new directory|mkdir ./test|
|remove a directorry (works if it's emty)|rmdir|
|to remove directories and their contents|rm -r ./test/|

## 11. Copying files  
Change position command *cp*. If you type the name of a program in terminal the program opens, this is possible because their aliases are recorder in applications shortcuts at their installation, also depends on the configuration and Desktop environments. To close an open program running in our terminal window wwwe can use *ctrl-c*.

|Action|Command|
|---|---|
|to create a test file|touch test.txt|
|copy a file to desktop|cp ./test.txt ~/Desktop/|

## Feed back after chapter 11
After chapter 11 a small box asked for positive or negative feedback, after that a comments section appeared; this time the feedback is supossed to be anonymous and will be sent to the instructor.  

## 12. Making custom commands  
Creating new custom commands using a text editor, the instructor uses *gedit*.
Sudo, super user do.

```bash
echo "hello world"
#saved, after that the instructor add execute privileges in a file editor i'll use bash
chmod +x ./helloworld
sh helloworld
./helloworld
#he moves his file to /usr/bin using sudo privileges
cp ./helloworld /usr/bin/
cd ~
helloworld
```

## 13. Evaluation
We have two options Practice mode (in beta) and Final test.
In practice mode we have time breaks, skip questions, focus on certain themes, reseume later and a progress bar.  

## I got a broken evaluation
The system asked me to to restart the test, the answer wasn't saved. An gott a 90% correcct answers ven all were marked as correct.
It considered the last question as skipped and did not allow to take the actual test.

There we some issues with the services. Overall was a easy to understand course environment, but it was really important tha the part that failed was the evaluation, this might dis engage future students.

## References
* Udemy (2026). *Learn the Linux Command Line*.  
        * <https://www.udemy.com/share/101rxc3@piI-7opfYL3wmOWTWx0nM5lRh_E7rxJtnVxkF7XxbqrrWYO-zikI9R9BTnNvZwEyOA==/>  
