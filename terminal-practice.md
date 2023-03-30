# The Command Line
* A command line *( aka terminal )* is a text based interface to the system. 
* The computer then presents us with a prompt *( user@bash )*
* ![bash](https://user-images.githubusercontent.com/123340286/228934731-8d465990-f34b-4f8c-8dcc-756b40672bb2.jpg)

* Within a terminal you have what is known as a shell. 
* This is a part of the operating system that defines how the terminal will behave and looks after running (or executing) commands for you. 
* There are various shells available, but the most common one is called bash *( Bourne again shell )* 
* ![no shell?](https://user-images.githubusercontent.com/123340286/228935751-a10218d4-34f8-4b39-8973-aa09cff54c83.png)
* *Why am I not in a shell?*

# Basic Navigation
* You can enter commands by typing them on the keyboard and recieve feedback from yout computer as text.
* When you enter commands, they are stored in a history. 
* You can traverse this history using the up and down arrow keys.

## Where Am I?
* pwd stands for Print Working Directory
* It tells you what your current or present working directory is.
* ![pwd](https://user-images.githubusercontent.com/123340286/228937099-f663303d-1aef-4bf6-b089-af6b24f93dca.jpg)

### What's Here?
* ls (short for list)
* ![ls](https://user-images.githubusercontent.com/123340286/228937556-cf1a6ccf-0106-4092-88db-e65e7cc8b76c.jpg)

* optional commands to use with ls:
  * [options]
    * single command line option *-l* indicates we are going to do a long listing
  * [arguments]
    * command line argument */etc* tells ls not to list our current directory but instead to list that directories contents.
  * ![ls-options-arguments](https://user-images.githubusercontent.com/123340286/228939014-cdf9c147-8cb7-406d-9320-2560df4835f7.jpg)
  * In he long list:
    * First character indicates whether it is a normal file ( - ) or directory ( d )
    * Next 9 characters are permissions for the file or directory
    * The next field is the number of blocks *?*
    * The next field is the owner of the file or directory
    * The next field is the group the file or directory belongs to
    * Next is the file size
    * Then is the file modification time
    * Finally, the actual name of the file or directory

## Paths
* A path is a means to get to a particular file or directory on the system.
* The file system under linux is a hierarchical structure: At the very top of the structure is what's called the root directory. 
   * Root is denoted by a single slash ( / ). 
   * It has subdirectories, and they have subdirectories, and so on. 
   * Files may reside in any of these directories.
* *Absolute paths* specify a location (file or directory) in relation to the root directory. 
  * You can identify them easily as they always begin with a forward slash ( / )
* *Relative paths* specify a location (file or directory) in relation to where we currently are in the system. 
  * They will *not* begin with a slash.
  
* ![ls-absolute-relative](https://user-images.githubusercontent.com/123340286/228940699-24af7f3e-e075-4a30-a7fe-ac6eac3890d2.jpg)
  * first command: pwd to find current location
  * second command: relative path
  * third command: absolute path

* ~ (tilde) - This is a shortcut for your home directory. 
  * Home directory is */home/laurel*  
  * You could refer to the directory *projects* with the path */home/laurel/projects* or ***~/projects***
* . (dot) - This is a reference to your current directory. 
  * ex: ***./projectss*** 
  * Normally this extra bit is not required but s0ometimes it comes in handy
* .. (dotdot)- This is a reference to the parent directory. 
  * You can use this several times in a path to keep going up the hierarchy. 
  * If you were in the path /home/laurel you could run the command ls ../../ and this would do a listing of the root directory.

* cd *( change directory )*
  * Usually run with a location argument *( cd [location] )*
  * If you run the command cd without any argument, it will always take you back to your home directory.
  * Tab completion:
    * When you start typing a path, you may hit the Tab key on your keyboard at any time which will invoke an auto complete action. 
    * If nothing happens, that means there are several possibilities. 
    * If you hit Tab again, it will show you those possibilities. 
    * You may then continue typing and hit Tab again and it will again try to auto complete for you.
* ![cd](https://user-images.githubusercontent.com/123340286/228943792-8e646fc0-943c-4369-8f95-ea8f0c914750.jpg)
* ![cd-dot-dot](https://user-images.githubusercontent.com/123340286/228943819-121c8dba-aa75-40ec-a8cf-98d19566eb14.jpg)

# Files
* Everything is a file
  * a text file is a file, 
  * a directory is a file, 
  * your keyboard is a file (one that the system reads from only), 
  * your monitor is a file (one that the system writes to only), 
  * etc.

## Linux
* Linux is an extentionless system
* A file extension is normally a set of 2 - 4 characters after a full stop at the end of a file, which denotes what type of file it is.
  * file.exe *( an executable file or program )*
  * file.txt
  * file.png
  * etc.
  
* Under Linux, the system actually ignores the extension and looks inside the file to determine what type of file it is.
  * An image saved as a .txt file will still be seen as an image by Linux
  * This can sometimes make it more difficult to know for certain what type of file a particular file is. 
  * ***file [path]*** can help us find this out

* ![linux-is-case-sensitive](https://user-images.githubusercontent.com/123340286/228946425-d7e73978-ab3c-486f-bb81-84aa0be3eb15.png)
* Remember that *Linux is case sensitive!*

* ![spaces-in-names](https://user-images.githubusercontent.com/123340286/228947424-f83d638c-af3e-486e-b77e-18c7b280e652.png)
* cd moves into whichever directory is specified by the *first command line argument only.*
* ![spaces-in-names-with-quotes](https://user-images.githubusercontent.com/123340286/228947607-e5a19408-947b-4b3f-be35-3b678e699cc8.png)
* Use quotes around the entire item.
  * You may use either single or double quotes
  * Anything inside quotes is considered a single item.
  * or...
* ![spaces-in-names-with-excape-character](https://user-images.githubusercontent.com/123340286/228947886-68c6bf25-b667-464d-81ed-fdf71d0d2004.png)
* Another method is to use what is called an *escape character ( \ )*
  * What the backslash does is escape (or nullify) the special meaning of the next character.
  * If you use *tab completion* before encountering the space in the directory name then the terminal will automatically escape any spaces in the name for you.

## Hidden Files and Directories
* If the file or directory's name begins with a . (full stop) then it is considered to be hidden.
  * user-specific config files
  * .env
* To hide a file, name or rename it beginning with a .
* To un-hide a file, rename the file to remove the . from the beginning

* ![ls-dash-a](https://user-images.githubusercontent.com/123340286/228948777-d44dc909-a0e8-4691-b974-5825eb854614.png)
* The command ls *will not list hidden files and directories* by default. 
* We may modify this by including the command line option -a
  * This will ensure that it does show hidden files and directories.

# Manual Pages
* The manual pages are a set of pages that ***explain every command available on your system*** including:
  * what they do, 
  * the specifics of how you run them,
  * and which command line arguments they accept
* man <command to look up>
* ![manual](https://user-images.githubusercontent.com/123340286/228950315-bfa492b9-55e1-4a55-9d09-e235d3f52d97.png)

* man -k <search term>
  * This command will do a keyword search on the manual pages
  * Note that the keyowrd may appear on many pages, making this search option tricky at times
* To seqarch within a manual page, press forward slash '/' followed by the term you would like to search for and hit 'enter' 
  * If the term appears multiple times, cycle through them by pressing the 'n' button for next
  
# File Manipulation

## Making a Directory
* It's important that we create a directory structure that will help us organise that data in a manageable way.
* mkdir [options] <directory-name>
  * other ways to we can supply a directory to be created:
    * mkdir /home/ryan/foo
    * mkdir ./blah
    * mkdir ../dir1
    * mkdir ~/linuxtutorialwork/dir2
* ![mkdir-dash-p](https://user-images.githubusercontent.com/123340286/228953107-7904ecf9-b701-45df-99ea-29c5b4aa1d7b.png)
  * The option -p tells mkdir to make parent directories as needed
* ![mkdir-dash-pv](https://user-images.githubusercontent.com/123340286/228953135-b1080918-1016-4cc3-b698-b58ac7dbfff9.png)
  * -v makes mkdir tell us what it is doing (normally it does not show its work)

## Deleting a Directory
* rmdir [options] <directory-name>
* **Remember that that there is no undo when it comes to the command line on Linux**, so be sure before you delete
  
* Things to note:
  * rmdir supports the -v and -p options similar to mkdir.
  * a directory must be empty before it may be removed

## Creating a File
* touch [options] <filename>
  * touch is actually a command we may use to modify the access and modification times on a file
  * however, if we touch a file and it does not exist, the command will automatically create it for us, thus the use of touch to create blank files

## Copying a File or Directory
* cp [options] <source> <destination>
  * Before making major changes to a file, we may wish to create a duplicate 
  * This way, if something goes wrong, we can easily revert back to the original
* ![copy-file-directory](https://user-images.githubusercontent.com/123340286/228955454-6ae61eef-f78e-4639-8bf0-85eccc0da1c9.png)

* The -r option *( recursive )* allows us to copy directories. 
  * Recursive means that we want to look at a directory, all files and directories within it, and for it's subdirectories
  * We want to go into these and do the same things to them that we did to the parent directory
* ![cp-dash-r](https://user-images.githubusercontent.com/123340286/228956575-3764826d-0d9f-4b2a-b599-01c27c7ad865.png)
  * In this example, any files and directories within the directory *foo* will also be copied to foo2.
  
## Moving a File or Directory
* mv [options] <source> <destination>
* One slight advantage over cp is that we can move directories without having to provide the -r option.
  
* ![mv](https://user-images.githubusercontent.com/123340286/228957162-fec02138-6c37-41b1-a5ab-63f0f8403043.png)
  * the directory foo2 was moved into the directory backups and renamed it as foo3
  * the file barney was moved into backups. As no destination name was provided, it kept the same name.

* ***mv may be used to rename a file or directory.***
  * Normally, mv will be used to move a file or directory into a new directory 
  * As shown in the example above, we may provide a new name for the file or directory and, as part of the move, it will also rename it. 
  * If we specify the destination to be the same directory as the source, but with a different name, then we have effectively used mv to rename a file or directory.

## Removing a File or a Non-Empty Directory
* rm [options] <file>
* As with rmdir, removing a file is an action **that may not be undone**
  
* **rm can be used to remove non-empty directories**
  * When rm is run with the -r *( recursive )* option, it allows us to remove directories and all files and directories contained within
* ![rm-dash-r](https://user-images.githubusercontent.com/123340286/228958808-3f3d243f-5adc-469d-bdc7-fec620b0649e.png)

* A good option to use in combination with *r* is *i ( interactive )* 
* This option will prompt you ***before removing each file and directory*** and give you *the option to cancel the command.*
  
# References:
* <https://ryanstutorials.net/linuxtutorial/commandline.php>
  * Tutorial sections 1 - 5 complete
  
* Cheat sheet:
  * <https://ryanstutorials.net/linuxtutorial/cheatsheet.php>
