# OverTheWire: Bandit Writeup

## Introduction
The Bandit challenge helps us get hands-on with Linux basics and sharpen our command-line skills. The levels teach us how to navigate directories and explore file contents. 

---

## Level 0 → Level 1
### Aim:
- To log in to the Bandit server and find the password in the `readme` file.

### Steps:
1. Use the SSH command to connect to the Bandit server:
   ```bash
   ssh bandit0@bandit.labs.overthewire.org -p 2220
- When prompted, use the password: bandit0.
2. Once logged in, look for a file named readme. It's right there in the home directory. ls command can be used to list directory contents of files.
   ```bash
   ls
- The cat command is used to read its contents:
   ```bash
   cat readme
- This will display the password for Level 1.


## Level 1 → Level 2
### Aim:
- To find the password in a file called -. 

### Steps:
1. Log in to Level 1 using the password which is obtained from Level 0:
   ```bash
   ssh bandit1@bandit.labs.overthewire.org -p 2220
2. Run ls and there'll be a file named -. Also To handle it as a filename, use ./:
   ```bash
   cat ./-
- That will show the password for Level 2.


## Level 2 → Level 3
### Aim:
- To find the password hidden in a file called spaces in this filename.

### Steps:
1. Log in to Level 2 with the password from Level 1:
   ```bash
   ssh bandit2@bandit.labs.overthewire.org -p 2220
2. Run ls to see the file:
   ```bash
   ls
- Note: To read the file with spaces in it's name we need to wrap the filename in quotes:
   ```bash
   cat "spaces in this filename"
- This will show the password for Level 3.
