
# Handy commands for Linux


<details>
Specially for noobs :)
</details>
<br />


## Quick links
1. [Hotkeys](#hotkeys)
1. [run a sh file](#run-sh-file)
1. [copy a file](#copy-a-file)
1. [duplicate a file](#duplicate-a-file)
1. [copy a directory](#copy-a-directory)
1. [duplicate a directory](#duplicate-a-directory)
1. [move a file](#move-a-file)
1. [rename a file](#rename-a-file)
1. [move a directory](#move-a-directory)
1. [rename a directory](#rename-a-directory)
1. [merge directories](#merge-directories)
1. [create a new file](#create-a-new-file)
1. [create a new directory](#create-a-new-directory)
1. [show file/directory size](#show-filedirectory-size)
1. [show file/directory info](#show-filedirectory-info)
1. [open a file with the default program](#open-a-file-with-the-default-program)
1. [zip a directory](#zip-a-directory)
1. [unzip a directory](#unzip-a-directory)
1. [peek files in a zip file](#peek-files-in-a-zip-file)
1. [remove a file](#remove-a-file)
1. [remove a directory](#remove-a-directory)
1. [list directory contents](#list-directory-contents)
1. [find a stale file](#find-a-stale-file)
1. [show a calendar](#show-a-calendar)
1. [find a future date](#find-a-future-date)
1. [use a calculator](#use-a-calculator)
1. [force quit a program](#force-quit-a-program)
1. [check server response](#check-server-response)
1. [view content of a file](#view-content-of-a-file)
1. [search for a text](#search-for-a-text)
1. [show disk size](#show-disk-size)
1. [check performance of your computer](#check-performance-of-your-computer)
1. [I can't remember these cryptic commands](#i-cant-remember-these-cryptic-commands)


## Hotkeys

```
Ctrl + Shift + X  To cut from terminal
Ctrl + Shift + C  To copy from terminal
Ctrl + Shift + V  To paste in terminal

Ctrl + A  Go to the beginning of the line you are currently typing on
Ctrl + E  Go to the end of the line you are currently typing on
Ctrl + L  Clears the Screen, similar to the clear command
Ctrl + U  Clears the line before the cursor position. If you are at the end of the line, clears the entire line.
Ctrl + H  Same as backspace
Ctrl + R  Let’s you search through previously used commands
Ctrl + C  Kill whatever you are running
Ctrl + D  Exit the current shell
Ctrl + Z  Puts whatever you are running into a suspended background process. fg restores it.
Ctrl + W  Delete the word before the cursor
Ctrl + K  Clear the line after the cursor
Ctrl + T  Swap the last two characters before the cursor
Esc + T   Swap the last two words before the cursor
Alt + F   Move cursor forward one word on the current line
Alt + B   Move cursor backward one word on the current line

cd        change directory
Tab       Auto-complete files and directory names
```

### run a sh file
```shell
$ chmod +x script-name-here.sh   # Set execute permission on your script
$ ./script-name-here.sh          # To run your script
```

### copy a file

Copy `readme.txt` to the `documents` directory

```shell
$ cp readme.txt documents/
```

### duplicate a file


```shell
$ cp readme.txt readme.bak.txt
```


### copy a directory


Copy `myMusic` directory to the `myMedia` directory

```shell
$ cp -a myMusic myMedia/
# or
$ cp -a myMusic/ myMedia/myMusic/
```

### duplicate a directory


```shell
$ cp -a myMusic/ myMedia/
# or if `myMedia` folder doesn't exist
$ cp -a myMusic myMedia/
```

### move a file


```shell
$ mv readme.txt documents/
```

**Always** use a trailing slash when moving files, [for this reason](http://unix.stackexchange.com/a/50533).

### rename a file


```shell
$ mv readme.txt README.md
```

### move a directory


```shell
$ mv myMedia myMusic/
# or
$ mv myMedia/ myMusic/myMedia
```

### rename a directory



```shell
$ mv myMedia/ myMusic/
```

### merge directories



```shell
$ rsync -a /images/ /images2/	# note: may over-write files with the same name, so be careful!
```

### create a new file


```shell
$ touch 'new file'    # updates the file's access and modification timestamp if it already exists
# or
$ > 'new file'        # note: erases the content if it already exists
```

### create a new directory


```shell
$ mkdir 'untitled folder'
# or
$ mkdir -p 'path/may/not/exist/untitled\ folder'
```

### show file/directory size


```shell
$ du -sh node_modules/
```

### show file/directory info


```shell
$ stat readme.md      # on Linux
```

### open a file with the default program


```shell
$ xdg-open file   # on Linux
```

### zip a directory


```shell
$ zip -r archive_name.zip folder_to_compress
```

### unzip a directory


```shell
$ unzip archive_name.zip
```

### peek files in a zip file


```shell
$ zipinfo archive_name.zip
# or
$ unzip -l archive_name.zip
```

### remove a file


```shell
$ rm my_useless_file
```

IMPORTANT: The rm command deletes my_useless_file permanently, which is equivalent to move my_useless_file to Recycle Bin and hit Empty Recycle Bin.

### remove a directory


```shell
$ rmdir my_useless_folder   # Deletes the specified empty directories and folders
$ rm -rf my_useless_folder  # Delete the directories including sub-directories.
```

### list directory contents


```shell
$ ls my_folder        # Simple
$ ls -la my_folder    # -l: show in list format. -a: show all files, including hidden. -la combines those options.
$ ls -alrth my_folder # -r: reverse output. -t: sort by time (modified). -h: output human-readable sizes.
```



### find a stale file


Find all files modified more than 5 days ago

```shell
$ find my_folder -mtime +5
```

### show a calendar


Display a text calendar

```shell
$ cal
```
Display selected month and year calendar

```shell
$ cal 11 2018
```

### find a future date


What is todays date?

```shell
$ date +%m/%d/%Y
```

What about a week from now?

```shell
$ date -d "+7 days"                                           # on Linux
```

### use a calculator


```shell
$ bc
```

### force quit a program


```shell
$ killall program_name
```

### check server response


```shell
curl -i umair.surge.sh
# curl's -i (--include) option includes HTTP response headers in its output.
```

### view content of a file


```shell
$ cat apps/settings.py
# if the file is too big to fit on one page, you can send it to a 'pager' (less) which shows you one page at a time.
$ cat apps/settings.py | less
```

### search for a text


```shell
$ grep -i "Query" file.txt
```



### show disk size


```shell
$ df -h
```

### check performance and hardware of your computer


```shell
$ top
$ htop        # sudo apt-get install htop
$ neofetch    # sudo apt-get install neofetch
```



## I can't remember these commands

You can always `man` the commands you are not familiar with.