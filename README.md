# File Manager

File Manager is a simulation, which provides a user-friendly interface for managing files and directories similar to the bash shell. With this simulation, you can create, delete, find, move, and print the working directory, among other features.

The implementation of the File Manager simulation is based on a binary tree data structure, where each node is represented by an array. This allows for up to 10 files or directories to be added to each directory, providing flexibility and scalability for managing large amounts of data.

The simulation is designed to be intuitive and easy to use, making it accessible for both novice and experienced users. With its powerful features and robust data management capabilities, File Manager simulation is a valuable tool for anyone looking to efficiently manage their files and directories.


## Installation

Use the package manager [git clone](https://git-scm.com/docs/git-clone) to install Order of Complexity Calculator.

```bash
git clone https://github.com/ritessshhh/FileManager
```

## How to use?

1. Get the program using above steps.
2. Run the main method inside BashTerminal.java
3. Start Entering commands.
```bash
Starting bash terminal.
[anyName@Kali]: $
```

## Commands Examples
Example 1:
```bash
// General use.
Starting bash terminal.
[user@host]: $ pwd
root
[user@host]: $ mkdir dev
[user@host]: $ mkdir home
[user@host]: $ mkdir bin
[user@host]: $ ls
dev home bin
[user@host]: $ cd dev
[user@host]: $ pwd
root/dev
[user@host]: $ touch ttys0
[user@host]: $ touch ttys1
[user@host]: $ ls
ttsy0 ttsy1
[user@host]: $ cd /
[user@host]: $ pwd
root
[user@host]: $ cd bin
[user@host]: $ touch sublime
[user@host]: $ touch gcc
[user@host]: $ cd /
[user@host]: $ ls -R

|- root             // Note directories begin with '|-'
    |- dev 
        - ttys0     // Note files begin with '-'
        - ttys1
    |- home
    |- bin
        - sublime
        - gcc

[user@host]: $ cd home
[user@host]: $ mkdir user
[user@host]: $ cd user
[user@host]: $ pwd
root/home/user
[user@host]: $ mkdir Documents
[user@host]: $ mkdir Pictures
[user@host]: $ mkdir Downloads
[user@host]: $ cd Documents
[user@host]: $ touch hw5.java
[user@host]: $ touch resume.pdf
[user@host]: $ ls
hw5.java resume.pdf
[user@host]: $ cd /
[user@host]: $ cd home
[user@host]: $ cd user
[user@host]: $ cd Pictures
[user@host]: $ touch puppies.jpg
[user@host]: $ cd /
[user@host]: $ ls -R

|- root
    |- dev
        - ttys0
        - ttys1
    |- home
        |- user
            |- Documents
                - hw5.java
                - resume.pdf
            |- Pictures
                - puppies.jpg
            |- Downloads
    |- bin
        - sublime
        - gcc

[user@host]: $ cd home
[user@host]: $ cd user
[user@host]: $ pwd
root/home/user
[user@host]: $ ls -R

|- user
    |- Documents
         - hw5.java
         - resume.pdf
    |- Pictures
         - puppies.jpg
    |- Downloads

[user@host]: $ exit
Program terminating normally


// Special cases.
...
[user@host]: $ pwd
root/dev
[user@host]: $ ls -R

|- dev
     - ttys0
     - ttys1
     - ttys2

[user@host]: $ touch ttys3
ERROR: Present directory is full.
[user@host]: $ cd ttys2
ERROR: Cannot change directory into a file.
[user@host]: $ cd nonexistantDirectory
ERROR: No such directory named 'nonexistantDirectory'.
[user@host]: $ exit
Program terminating normally
```

Example 2:
```bash
[user@host]: $ pwd
root
[user@host]: $ ls -R

|- root
    |- dev
         - ttys0
         - ttys1
    |- home
        |- user
            |- Documents
                - hw5.java
                |- myFolder
                     - file1.txt
                     - file2.txt
                     - file3.txt
            |- Pictures
                 - puppies.jpg
    |- tmp
         - puppies.jpg

[user@host]: $ find puppies.jpg
root/home/user/Pictures/puppies.jpg
root/tmp/puppies.jpg
[user@host]: $ find kittens.jpg
ERROR: No such file exits.
[user@host]: $ cd home/user // Note cd with path.
[user@host]: $ pwd
root/home/user
[user@host]: $ cd .. // Move up to parent.
[user@host]: $ pwd
root/home
[user@host]: $ cd ..
[user@host]: $ pwd
root
[user@host]: $ cd ..
ERROR: Already at root directory.
[user@host]: $ pwd
root
[user@host]: $ mv root/home/user/Documents/myFolder root/tmp // Note absolute paths.
[user@host]: $ ls -R

|- root
    |- dev
         - ttys0
         - ttys1
    |- home
        |- user
            |- Documents
                 - hw5.java
            |- Pictures
                 - puppies.jpg
    |- tmp
        - puppies.jpg	
        |- myFolder
             - file1.txt
             - file2.txt
             - file3.txt

[user@host]: $ exit
Program terminating normally
```


## License

[MIT](https://choosealicense.com/licenses/mit/)
