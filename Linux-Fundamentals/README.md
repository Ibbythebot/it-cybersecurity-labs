# Linux Fundamentals

## Overview

This lab covers the basics of Linux using Ubuntu through Windows Subsystem for Linux (WSL).

I practiced navigating the Linux filesystem, identifying users, using elevated privileges, creating and reading files, and managing file permissions.

## Environment

* Operating System: Ubuntu
* Platform: WSL (Windows Subsystem for Linux)
* Username: `ibbythebot`

## Commands Practiced

### `pwd`

Displays the current working directory.

My Linux home directory was `/home/ibbythebot`.

### `ls`

Lists files and directories in the current location.

### `cd`

Changes the current directory.

Examples:

* `cd ..` moves up one directory.
* `cd ~` returns to my Linux home directory.

### `whoami`

Displays the user account currently being used.

My username was `ibbythebot`.

### `sudo`

Allows a user to run a specific command with elevated privileges.

I used `sudo whoami`, which returned `root`.

`root` is the Linux superuser with administrative privileges.

## File Creation and Reading

I created a file using `touch lab.txt`.

I then wrote text to the file using:

`echo "Linux security lab" > lab.txt`

I read the contents using `cat lab.txt`.

### `>` vs `>>`

* `>` overwrites the existing contents of a file.
* `>>` appends text to the existing contents.

## Linux File Permissions

I used `ls -l` to view file permissions.

An example permission string is:

`-rw-r--r--`

The permissions are divided between:

* Owner
* Group
* Others

The permission letters mean:

* `r` = read
* `w` = write
* `x` = execute
* `-` = permission not granted

## `chmod`

I practiced changing file permissions with:

`chmod 400 lab.txt`

This gave the owner read-only access while removing permissions for the group and others.

I then restored the permissions with:

`chmod 644 lab.txt`

## Security Takeaways

File permissions are important in cybersecurity because they control who can read, modify, or execute files.

Excessive permissions can allow users or processes to access files they should not have access to.

This connects to the security principle of **least privilege**, where users and processes should receive only the permissions they actually need.

## What I Learned

I learned the basic structure of a Linux environment and how to navigate it from the terminal.

I also learned how Linux identifies users, how administrative privileges work, how files are created and read, and how permissions can be used to control access to files.
