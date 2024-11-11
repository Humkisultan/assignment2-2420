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
