# Assignment 2 - ACIT 2420


Project 1 - Configuration Scripts


This project contains 3 main scripts and 1 user-defined package file, along with the directories "bin", "config", and "home", which are cloned from the providedgitlab repository.


Installing the packages - The "installer" script reads through the user defined file "packge" and installs each package.  If the package file is missing or a package fails to install, the installer will print an error and skip to the next step. To run this script, the user must be the root user or run the command "sudo ./installer" and "pacman" must be available.


Creating symbolic links - The "symlink" script creates symbolic links from specified source directories and files to target locations in the user's home directory. If a target file or directory already exists, it removes the existing one before creating a new link to prevent copies of the links. To run this script, the user must be the root user or run the command "sudo ./symlink".


Running the scripts - The "caller" script runs "installer", "symlink", or both scripts based on user-specified options. The user can choose between:

-a : Runs both "installer" and "symlink" scripts.
-i : Runs only the "installer" script.
-s : Runs only the "symlink" script.


If an invalid option is specified or if the specified script is missing, an error message is printed, and the script exits. To run this script, the user must be the root user or run the command "sudo ./caller -#option".




Project 2 - New User Script




This project has only one script, "new_user", which creates a new user on a Linux system, assigns them a shell, home directory, and optionally add them to specific groups. It handles UID and GID generation, group management, and the creation of the home directory with default configuration files. To run this script, the user must be the root user or use "sudo ./new_user -u user1 -s /bin/bash -g group1,group2" to run the script.


There are 3 possible command-line options for this script:

-u : Specifies the username for the new user and is required for the generation of a new user.
-s : Specifies the shell for the new user and is required for the generation of a new user.
-g : Optionally, specifies a comma-separated list of additional groups the user should be added to.


The script also prevents duplicate users by checking if the specified username already exists in /etc/passwd. If the user already exists, it exits with an error message. After user creation, the script prompts the administrator to set a password for the new user using the passwd command. 

