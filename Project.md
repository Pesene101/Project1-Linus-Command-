# Documentation For LINUS COMMAND IMPLEMENTATION

## This Project shows how to implement linus Commands

## 1. **sudo command**
Sudo is a command-line utility for Unix and Unix-based operating systems such as Linux and macOS. The utility provides an efficient way to temporarily grant users or user groups privileged access to system resources so that they can run commands that they cannot run under their regular accounts.

Here is the general syntax;


`sudo (command e.g apt upgrade)`


so it becomes 


`sudo apt upgrade`



![Sudo](./Images/sudo.png)



## 2. **pwd command**
The "pwd" command prints the full name (the full path) of current/working directory. By default, right after ssh-ing to a Linux machine you would find yourself in your home directory, usually /home/<username>. ssh to a cluster, type “pwd” and see if it returns '/home/<ISUNetID>', where <ISUNetID> is your ISU NetID.

The pwd command uses the following syntax;

`pwd [option]`

it has the following options;

-L (logical)	Use PWD from environment, even if it contains symbolic links

-P (physical)	Avoid all symbolic links

–help	Display this help and exit

–version	Output version information and exit

`pwd`

![pwd](./Images/pwd.png)

## 3. ** command**
cd: The cd command will allow you to change directories. When you open a terminal you will be in your home directory. To move around the file system you will use cd. Examples:

    To navigate into the root directory, use "cd /"

    To navigate to your home directory, use "cd" or "cd ~"

    To navigate up one directory level, use "cd .."

    To navigate to the previous directory (or back), use "cd -"

    To navigate through multiple levels of directory at once, specify the full directory path that you want to go to. For example, use, "cd /var/www" to go directly to the /www subdirectory of /var/. As another example, "cd ~/Desktop" will move you to the Desktop subdirectory inside your home directory. 

![cd](./Images/cd.png)

## 4. **LS command**
ls: The ls command will show you ('list') the files in your current directory. Used with certain options, you can see sizes of files, when files were made, and permissions of files. Example: "ls ~" will show you the files that are in your home directory. 

ls has the following options;

ls -r	It is used to print the list in reverse order.

ls -R	It will display the content of the sub-directories also.

ls -lX	It will group the files with same extensions together in the list.

ls -lt	It will sort the list by displaying recently modified filed at top.

![LS](./Images/Ls.png)

## 5. **CAT command**

The cat command on Linux concatenates files together. It's often used to concatenate one file to nothing to print the single file's contents to the terminal. This is a quick way to preview the contents of a text file without having to open the file in a large application.

Here is the general syntax;

`cat Project.md`

![cat](./Images/cat.png)

## 6. **cp command**

cp: The cp command will make a copy of a file for you. Example: "cp file foo" will make an exact copy of "file" and name it "foo", but the file "file" will still be there. If you are copying a directory, you must use "cp -r directory foo" (copy recursively). (To understand what "recursively" means, think of it this way: to copy the directory and all its files and subdirectories and all their files and subdirectories of the subdirectories and all their files, and on and on, "recursively") 

for example; `cp -r Images NewImages`

![CP](./Images/cp.png)

## 7. **mv command**

mv: The mv command will move a file to a different location or will rename a file. Examples are as follows: "mv file foo" will rename the file "file" to "foo". "mv foo ~/Desktop" will move the file "foo" to your Desktop directory, but it will not rename it. You must specify a new file name to rename a file.

    To save on typing, you can substitute '~' in place of the home directory.

    Note that if you are using mv with sudo you can use the ~ shortcut, because the terminal expands the ~ to your home directory. However, when you open a root shell with sudo -i or sudo -s, ~ will refer to the root account's home directory, not your own. 

for example; `mv Project.md Images`

![mv](./Images/mv.png)

## 8. **mkdir command**

The mkdir command in Linux/Unix is a command-line utility that allows users to create new directories. mkdir stands for "make directory." With mkdir , you can also set permissions, create multiple directories at once, and much more.

Here's the basic syntax

`mkdir [option] directory_name`

![mkdir](./Images/mkdir.png)

## 9. **rmdir command**

The rmdir command removes the directory, specified by the Directory parameter, from the system. The directory must be empty before you can remove it, and you must have write permission in its parent directory. Use the ls -al command to check whether the directory is empty.

![rmdir](./Images/rmdir.png)

## 10. **rm command**

The rm command removes the entries for a specified file, group of files, or certain select files from a list within a directory. User confirmation, read permission, and write permission are not required before a file is removed when you use the rm command.

Here's the general syntax;

`rm filename`

![rm](./Images/rm.png)

## 11. **touch command**

The touch command is used in Linux to change timestamps and access stamps in individual files or directories. Since this recreates a file if it doesn't already exist, the command is also often used to create new, empty files. For most users, this secondary use is far more important in their daily work.

![touch](./Images/touch.png)

## 12. **locate command**

The 'locate' command in Linux is a powerful tool used to find files by their name. You can use it like this: locate [options] filename. txt . In this example, we use the 'locate' command to search for 'example.

![locate](./Images/locate.png)

## 13. **find command**

To find a file in Linux, you can use the Linux find command. This starts a recursive search, where a directory hierarchy is searched following certain criteria. The Linux find command is a precise tool for finding files and directories and is supported across pretty much all Linux distributions.

Here's the general syntax;

`find [option] [path][expression]`

You can edit to suit your case.
For example; you want to look for a file called Project.md in the home directory.

![find](./Images/find.png)

## 14. **grep command**

Grep is a useful command to search for matching patterns in a file. grep is short for "global regular expression print". If you are a system admin who needs to scrape through log files or a developer trying to find certain occurrences in the code file, then grep is a powerful command to use.

![grep](./Images/grep.png)

## 15. **df command**
The df command displays information about total space and available space on a file system. The FileSystem parameter specifies the name of the device on which the file system resides, the directory on which the file system is mounted, or the relative path name of a file system.

![df](./Images/df.png)

these are of the command options for df command;
-t type	Limit listing to file systems of type TYPE
-a	Show all filesystems
-i	Get info about Inodes
-B SIZE	Set blocksize. You can also use the BLOCKSIZE environment variables. For example, BLOCKSIZE=512 df

## 16. **du command**

The du (disk usage) command measures the disk space occupied by files or directories. By default, it measures the current directory and all its subdirectories, printing totals in blocks for each, with a grand total at the bottom.

![du](./Images/du.PNG)
Adding a flat to the du command will modify the operation, such as;

-b -k -m	Measure usage in bytes ( -b ), kilobytes ( -k ), or megabytes ( -m ).
-c	Print a total in the last line. This is the default behavior when measuring a directory, but for measuring individual files, provide -c if you want a total.
-L	Following symbolic links and measure the files they point to.

## 17. **head command**

The Linux head command prints the first lines of one or more files (or piped data) to standard output. By default, it shows the first 10 lines. However, head provides several arguments you can use to modify the output. Read on to learn how to use the head command, its syntax, and options with easy-to-follow examples.

![head](./Images/head.PNG)

## 18. **tail command**

The Linux tail command is a command-line utility that prints data from the end of a specified file or files to standard output. The utility provides an easy way to quickly see file updates in real time, as new data is usually added to the end of a file.

## 19. **diff command**

diff is a command-line utility that allows you to compare two files line by line. It can also compare the contents of directories. The diff command is most commonly used to create a patch containing the differences between one or more files that can be applied using the patch command.

Here's the general format;

`dif [option] file1 file2`

![diff](./Images/diff.PNG)

## 20. **tar command**

The Linux tar command is used for saving several files into an archive file. We can later extract all of the files or just the desired ones in the archive file. tar stands for “tape archive”. tar, by default, keeps the directory structure of archived files.

Here is the basic syntax;

`tar [options][archive_file][file or directory to be archived]`

For instance, you want to create a new TAR arrchive named newimage.tar in the home directory: you can edit the code to suit your purpose.

