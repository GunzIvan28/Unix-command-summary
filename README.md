# Unix-command-summary
A basic break down of unix-based commands

**1. man - Accessing On-Line Manual Pages**
In the terminal, the "man" command looks up the manual page for a command. The format of man is man <commandname> for example:
	
    man ls


    man pwd


    man cat
  
**2. pwd - Print the Working Directory**
The "pwd" command prints the full pathname of your current working directory. The syntax for pwd is:
pwd for example:

    $pwd


    /home/gunz

**3. cd - Changing Directory**
The "cd" command changes the current working directory to the directory speciﬁed. The format of cd is:
cd <directorypath>. If you do not specify directory, cd changes to your home directory for example:
	
    $ cd /


    /$ pwd 	/  (notice that the directory has changed to the root folder)


    /$ cd ~


    $ pwd 	/home/gunz (realize we have returned to the original home directory)

**4. ls - Listing the Contents of Directories**
The "ls" command lists the contents of one or more speciﬁed directories or lists information about one or more speciﬁed ﬁles. By default, it lists only files which are not hidden/ without a dot (".") at the beginning. Therfore, one has to add options to it in order to view such files for example:


    ls -a Lists all ﬁles, including those that begin with a “.”.

    -F Marks directories with a / and executable ﬁles with a *. 
   
    -l Produces a longer, more informative listing
		 
**5.  mkdir - Making Directories**
The "mkdir" command makes directories with speciﬁed names. The syntax of the mkdir command is: 


    mkdir <directory1> <directory2> <directory(n)> 
	
**6. rmdir - Removing Directories**
The rmdir command removes empty directories with speciﬁed names. The format of the rmdir command is rmdir directory(1) directory(2)... directory(n). The rmdir command will not remove a directory with ﬁles in it - for this use the rm -r command, described later in this section, but be careful!. For example:


    $ ls -F Mail/ prog/ thesis/ zeta/ zeta.f 


    $ rmdir zeta 


    $ ls -F Mail/ prog/ thesis/ zeta.f 

**7. cp - Copying a File**
The "cp" command makes a copy of a ﬁle or copies multiple ﬁles into a directory. The format of the cp command is: 

    cp <source-ﬁle> <destination-ﬁle> or 

    cp <source-ﬁle(1) source-ﬁle(2)... source-ﬁle(n)> <destination-directory>. 
	
The ﬁrst form makes a copy of the ﬁle source-ﬁle called destination-ﬁle and the second copies series of ﬁles source-ﬁle(1..n) into directory destination-directory.

**8. cat - Printing Files Onto the Screen**
The "cat" command prints out the contents of a series of ﬁles one after the other. The syntax of the at command is:

    cat ﬁlename(1) ﬁlename(2)... ﬁlename(n).For example, to read the “message of the day”:

    $ cat /etc/motd.

**9. more - Printing Files One Screen at a Time**
The "more" command prints out the contents of named ﬁles, one screen full at a time. The format of the more command is: 

    more ﬁlename(1) ﬁlename(2)... ﬁlename(n).
    
To quit more, press the q key, to move one line at a time press the RETURN key or the SPACE bar to move one screen full at a time.

**10. mv - Moving and Renaming Files**
The "mv" command changes the name or location of a ﬁle or directory. The formats of the mv command are: 

    mv <oldﬁle> <newﬁle> or  
    
    mv ﬁle(1) ﬁle(2)... ﬁle(n)directory or 
    
    mv olddir newdir 

**11.  rm - Removing Files and Directories**
The rm command removes ﬁles and directories. Caution: There is no way to reverse this process  The format of the rm command is :

rm [-i] [-r] fd(1) fd(2)... fd(n)

    where fd(1..n) are ﬁles or directories.
    
    -i Inquire before removing a ﬁle (“y” to delete, anything else to not delete). 
    
    -r Recursively remove a directory and all its contents and subdirectories (To be used with extreme care).

**12. chmod - Changing Access Permissions**
The chmod command changes the “permissions” on a ﬁle or directory. It gives or removes access for another user or group of users to read, change or run one of the ﬁles owned by you. Users on the system fall into three categories:
user You, group Anyone in the same class as yourself, such as pg 1999, staﬀ or postdoc. other Anyone who uses the Institute Computers (sometimes called world).
The format of the chmod command is: chmod ugo+-=rwx fd(1) fd(2)... fd(n) where fd(1..n) may be a ﬁle or directory where:

    ugo Specify u (user), g (group) or o (other).
    
    +-= Specify + (add), - (subtract) or = (set).
    
    rwx Specify r (read), w (write) or x (execute).

**13. grep - Searching for Strings in Files**
The "grep" command scans a ﬁle for the occurrence of a word or string and prints out any line in which it is found. The format of grep is: 

    grep [-i] ’string’ ﬁlename(1) ﬁlename(2)...

**14. wc - Counting Words**
The "wc" command counts the lines, words and characters in a ﬁle. The syntax of wc is:

    wc [-l] [-w] [-c] ﬁlename...
    
    -l Prints the number of lines in the ﬁles.
    
    -w Prints the number of words in the ﬁles. 
    
    -c Prints the number of characters in the ﬁles.

**15. Wildcards**
Most shells have a mechanism which indicates groups of letters. For example: 

    $ ls abc* - to list all the ﬁles in a directory which begin with the letters abc

    $ ls ???h - to list all the four–letter ﬁles which end in h

    $ cp [0-9]* <dir>: copies all files ranging from 0-9 irrespective of its format or extensions
	
    $ cp [[:upper:]]* <dir>: copies all files with upper case letters irrespective of its format or extensions
	
    $ cp [[:lower:]]* <dir>: copies all files with lower case letters irrespective of its format or extensions
	
    $ cp *[[:digit:]] <dir>: copies all files that end with digits
	
    $ cp [[:alnum:]] <dir>: copies all files with letters & numerals






