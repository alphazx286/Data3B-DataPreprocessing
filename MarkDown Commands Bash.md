# DESCRIPTION OF COMMANDS BASH

### **mkdir**
> Create new folder(s), if they do not already exist. 

-     mkdir [Options] folder...

-     mkdir "Name with spaces"

### **cd**

> Change Directory - change the current working directory to a specific Folder.

-     Syntax: cd [Options] [Directory]

> Change to the directory fred inside the current directory: $ cd ./fred

- $ cd /usr/local/sybase
- $ pwd
- /usr/local/sybase

> Quickly get back:
- $ cd -
- $ pwd
- /usr/local/sybase

> (Back to your home folder)
- $ cd 

### **history**

> Command Line history

- Syntax
-      history 
-      history [n]
-      history -c
-      history -d offset
-      history [-anrw] [filename]
-      history -ps arg

- Key
>   -c   Clear the history list. This can be combined with the other
>        options to replace the history list completely.

>   -d offset 
>        Delete the history entry at position offset. 
>        offset should be specified as it appears when the history is displayed. 

>   -a   Append the new history lines (history lines entered since 
>        the beginning of the current Bash session) to the history file. 

>   -n   Append the history lines not already read from the history file 
>        to the current history list. These are lines appended to the 
>        history file since the beginning of the current Bash session. 

>   -r   Read the current history file and append its contents to the history list. 

>   -w   Write out the current history to the history file. 

>   -p   Perform history substitution on the args and display the result 
>        on the standard output, without storing the results in the history list. 

>   -s   The args are added to the end of the history list as a single entry. 


### **clear**

> command can make the next command easier to read


### **ls (.* , .*.txt , -a , -Al , -h , -lh, ls my?dir*, ls my*dir*)**

> List information about files.

- Syntax
-      ls [Options]... [File]...

- -a, --all                  
> List all entries including those starting with a dot .

- -A, --almost-all           
> List all entries including those starting with a dot .  ; Except for . and .. (implied)

- -h, --human-readable       
> Print sizes in human readable format (e.g., 1K 234M 2G)

- -l                         
> Use a long listing format

- -s, --size                 
> Print size of each file, in blocks

- $ ls ~
> List the contents of your home directory

- $ ls -al
> list everything in a vertical list:


- $ ls -d */
> List the directories in the current directory:

- $ ls *
> List all subdirectories:


## **nano**

> a small and friendly text editor. Besides basic text editing, nano offers many extra features like an interactive search and replace, go to line and column number, auto-indentation, feature toggles, internationalization support, and filename tab completion.

- Syntax
-       nano [Filename] [Fileformat]...


## **cat**
> Concatenate and print (display) the content of files. Concatenate FILE(s), or standard input, to -	standard output.

- Syntax
-       cat [Options] [File]...


-  -A, --show-all           
> equivalent to -vET

-  -b, --number-nonblank    
> number nonblank output lines

-  -e                       
> equivalent to -vE

-  -E, --show-ends          
> display $ at end of each line

-  -n, --number             
> number all output lines

-  -s, --squeeze-blank      
> never more than one single blank line

-  -t                       
> equivalent to -vT

-  -T, --show-tabs          
> display TAB characters as ^I

-  -u                       
> (ignored)

 - -v, --show-nonprinting   
> use ^ and M- notation, except for LFD and TAB


- $ cat myfile.txt
> Display a file:

- $ cat *.txt
> Display all .txt files:

- $ cat File1.txt File2.txt > union.txt
> Concatenate two files:


- $ sort -u File1.txt File2.txt > unique_union.txt
> If you need to combine two files but also eliminate duplicates, this can be done with sort unique:

- $ my_variable='cat File3.txt'
> Put the contents of a file into a variable

## **cp (-i , -R)**

>Copy one or more files to another location.
>Copy SOURCE to DEST, or multiple SOURCE(s) to >DIRECTORY. 

- Syntax
-       cp [options]... Source Dest
-       cp [options]... Source... Directory

- Key

- -a, --archive                
> same as -dpR

-  -b, --backup                 
> Make backup before removal. If the copy will overwrite a file in the destination, then the original file will be backed up as 'filename~' before being overwritten.

-  -d, --no-dereference         
> preserve links

-  -f, --force                  
> remove existing destinations, never prompt

-  -i, --interactive            
> prompt before overwrite

-  -l, --link                   
> link files instead of copying

-  -p, --preserve               
> preserve file attributes if possible

-  -P, --parents                
> append source path to DIRECTORY

-  -r                           
> copy recursively, non-directories as files

-  -R, --recursive              
> copy directories recursively

-  -s, --symbolic-link          
> make symbolic links instead of copying

-  -S, --suffix=SUFFIX          
> override the usual backup suffix

-  -u, --update                 
> copy only when the SOURCE file is newer than the destination file or when the destination file is missing

-  -v, --verbose                
> explain what is being done

-  -x, --one-file-system        
> stay on this file system

-  --help                   
> display this help and exit

-   --version                
> output version information and exit.


- $ cp demofile demofile.bak
- or
- $ cp demofile{,.bak}

> Copy demofile to demofile.bak :


- $ cp "$SOURCE" "$DEST"
> With variables make sure you quote everything:


- $ FILE="demofile.txt"
- $ cp "$FILE" "${FILE%.*}.bak"
> Copy demofile.txt to demofile.bak :


- $ cp -f /mnt/floppy/* ~
> Copy floppy to home directory:

## **pwd**
> Print Working Directory (shell builtin) 

- Syntax
-       pwd [-LP]

### **man**
> is used to display the user manual of any command that we can run on the terminal. It provides a detailed view of the command which includes NAME, SYNOPSIS, DESCRIPTION, OPTIONS, EXIT STATUS, RETURN VALUES, ERRORS, FILES, VERSIONS, EXAMPLES, AUTHORS and SEE ALSO

- Syntax
-       man [command]

### **rm (-R)**
> Remove files (delete/unlink)

- Syntax
-      rm [options]... file...

>To remove a file you must have write permission on the file and the folder where it is stored. The OWNER of a file does not need rw permissions in order to rm it.

>By default, rm does not remove directories. Use the --recursive (-r or -R) option to remove each listed directory, too, along with all of its contents.

>Note that if you use rm to remove a file, it is usually possible to recover the contents of that file. If you want more assurance that the contents are truly unrecoverable, consider using shred. 


-   -f, --force
> ignore nonexistent files, never prompt
 
-   -i
> Prompt before every removal
 
-   -I
> Prompt once before removing more than three files, or when removing recursively. Less intrusive than -i, while still giving protection against most mistakes interactive[=WHEN] Prompt according to WHEN: never, once (-I), or always (-i). Without WHEN, prompt always --one-file-system When removing a hierarchy recursively, skip any directory that is on a file system different from that of the corresponding command line argument --no-preserve-root Do not treat '/' specially --preserve-root Do not remove '/' (default) 

-   -r, -R, --recursive
> Remove directories and their contents recursively 
-   -v, --verbose
> Explain what is being done 

### **mv**
>Move or rename files or directories.
- SYNTAX
-      mv [options]... Source Dest
-      mv [options]... Source... Directory

>If the last argument names an existing directory, 'mv' moves each other given file into a file with the same name in that directory. Otherwise, if only two files are given, it renames the first as the second. It is an error if the last argument is not a directory and more than two files are given.

- -b or -backup
> Make a backup of each file that would otherwise be overwritten or removed.

- -f or -force
> Remove existing destination files and never prompt the user.

- -i or -interactive
> Prompt whether to overwrite each existing destination file, regardless of its permissions.  If the response does not begin with 'y' or 'Y', the file is skipped.

- -u or -update
> Do not move a nondirectory that has an existing destination with the same or newer modification time.

- -v or -verbose
> Print the name of each file before moving it.

### locate
> Find files.

- Syntax
-       locate [options] pattern

> Search database(s) of filenames and print matches. *, ?, [, and ] are treated specially; / and . are not. Matches include all files that contain pattern, unless pattern includes metacharacters, in which case locate requires an exact match.



- sudo find / > database.txt
- grep Alanis database.txt

### **find**
> Search a folder hierarchy for filename(s) that meet a desired criteria: Name, Size, File Type

- Syntax
-      find [-H] [-L] [-P] [path...][expression]

> he -H, -L and -P options control the treatment of symbolic links. Command-line arguments following these are taken to be names of files or directories to be examined, up to the first argument that begins with and of the characters:   - ( ) , ! That argument and any following arguments are taken to be the expression describing what is to be searched for. If no paths are given, the current directory is used. If no expression is given, the expression '-print' is used (but you should probably consider using '-print0' instead, anyway).


-    -P
> Never follow symbolic links. This is the default behaviour. When find examines or prints information a file, and the file is a symbolic link, the information used shall be taken from the properties of the symbolic link itself.

-    -L
> Follow symbolic links. When find examines or prints information about files, the information used shall be taken from the properties of the file to which the link points, not from the link itself (unless it is a broken symbolic link or find is unable to examine the file to which the link points). Use of this option implies -noleaf. If you later use the -P option, -noleaf will still be in effect. If -L is in effect and finddiscovers a symbolic link to a subdirectory during its search, the subdirectory pointed to by the symbolic link will be searched. When the -L option is in effect, the -type predicate will always match against the type of the file that a symbolic link points to rather than the link itself (unless the symbolic link is broken). Using -L causes the -lname and -ilname predicates always to return false.

-    -H

> Do not follow symbolic links, except while processing the command line arguments. When find examines or prints information about files, the information used shall be taken from the properties of the symbolic link itself. The only exception to this behaviour is when a file specified on the command line is a symbolic link, and the link can be resolved. For that situation, the information used is taken from whatever the link points to (that is, the link is followed). The information about the link itself is used as a fallback if the file pointed to by the symbolic link cannot be examined. If -H is in effect and one of the paths specified on the command line is a symbolic link to a directory, the contents of that directory will be examined (though of course -maxdepth 0 would prevent this). If more than one of -H, -L and -P is specified, each overrides the others; the last one appearing on the command line takes effect. Since it is the default, the -P option should be considered to be in effect unless either -H or -L is specified.

> When the -H or -L options are in effect, any symbolic links listed as the argument of -newer will be dereferenced, and the timestamp will be taken from the file to which the symbolic link points. The same consideration applies to -anewer and -cnewer.

- $ find ~/Movies -mmin -30 
> Find files have been modified within the last 30 minutes:

- $ find . -name '*.doc' -name questionnaire*
> ind .doc files that also start with 'questionnaire' (AND)

- $ find . -name '*.doc' -name questionnaire* -delete
> Then delete them...

- $ find ./music -name "*.mp3" 
> List filenames ending in .mp3, searching in the music folder and subfolders:

- $ find . -iname "alice" -print0
> List filenames matching the name Alice or ALICE (case insensitive), search in the current folder (.) and all subfolders:


### **stat**
> Display file or file system status. Mandatory arguments to long options are mandatory for short options too.

- Syntax:
-       stat [OPTION]... FILE...

-   -L, --dereference
> follow links

-    -f, --file-system
> display file system status instead of file status

-    -c  --format=FORMAT
> use the specified FORMAT instead of the default; output a newline after each use of FORMAT --printf=FORMAT ike --format, but interpret backslash escapes, and do not output a mandatory trailing newline; if you want a newline, include \n in FORMAT

-    -t, --terse
> print the information in terse form



- $ stat -c%A ss64.sh 
- -rw-r--r--
> List the file permissions for ss64.sh:


- $ stat -f /etc
-  File: "/etc"
- ID: 0 Namelen: 255 Type: reiserfs
- Block size: 4096 Fundamental block size: 4096
- Blocks: Total: 1977922 Free: 1272318 -Available: 1272318
- Inodes: Total: 0 Free: 0
> Display file system (directory) information for /etc:

### **groups**
> Print group names a user is in.

- Syntax
-     groups [username]...

>Prints the names of the primary and any supplementary groups for each given username, or the current process if no names are given.

>If names are given, the name of each user is printed before the list of that user's groups.

### **chmod**
> Change access permissions, change mode

- Syntax
-        chmod [Options]... Mode [,Mode]... file...

-        chmod [Options]... Numeric_Mode file...

-        chmod [Options]... --reference=RFile file...



> chmod changes the permissions of each given file according to mode, where mode describes the permissions to modify. Mode can be specified with octal numbers or with letters.

> Using letters is easier to understand for most people. e.g. chmod +x filename.sh to make filename.sh executable.

- -f, --silent, --quiet   
> Suppress most error messages.

-  -v, --verbose           
> Output a diagnostic for every file processed.

-  -c, --changes           
>like verbose but report only when a change is made.

- --reference=RFile   
> use RFile's mode instead of MODE values.

- -R, --recursive         
> Change files and directories recursively Take care to not run recursive chmod on the root '/' directory or any other system directory.


- $ chmod a-x file
> Deny execute permission to everyone:

- chmod a+r file
> Allow read permission to everyone:

