# frcc/cng2001_bashlab


# Bash Lab 1 (Graded)

Write a bash script that:

1.  Reads a Name
2.  displays the contents of the file `data/file_1.txt` **but** changes the word Knowledge to the inputed name

## Input
Prompt the user for a name, example: 
```
$ ./scriptname.sh
What is your name?
SomeName
```
## Output
The contents of file `data/file_1.txt` with the word Knowledge replaced with the input name	

## Hints

Use `read`,`cat` and the variable expansion `${}` for regular expressions: `${varname/sometext/othertext}`

## Steps
1. `cd ~`
2. clone this repo: `git clone https://github.com/swgraham/frcc_cng_2001_bashlab.git`
3. `cd frcc_cng_2001_bashlab`
4. You should now have a `data/file_1.txt` to process as described above.
5. When finished, upload your bash script and a screenshot of your output. 

# Bash Lab 2 (Graded)

Create a bash script that takes a directory as an argument and prints the list of files and how many lines and words are in each file. If the directory doesn't exist it should notify user.

## Script Name

script should be named `username_lab2.sh` where username is YOUR userid.  Ex: `swgraham_lab2.sh`

## Input

Use the directories `data` and `data2` in this repo as the Directory names

Example: 
./swgraham_lab2.sh data

## Output
```
$ ./swgraham_lab2.sh data
==========================================================
=             Script Author: Scott Graham                =
=              Files in Directory: data                  =
==========================================================
somedir: Skipping, it is a directory
file_1.txt has       21 lines and      209 words
file_10.txt has       69 lines and      665 words
file_2.txt has       22 lines and      219 words
file_3.txt has       77 lines and      728 words
file_4.txt has       44 lines and      429 words
file_5.txt has       23 lines and      221 words
file_6.txt has       93 lines and      885 words
file_7.txt has       75 lines and      714 words
file_8.txt has       21 lines and      214 words
file_9.txt has       45 lines and      430 words
```
## Errors
1. The script should output SIMILAR to the above
  a. It **must** have your name in the output.
  b. It **must** have the directory you used. This script should work on both `data` and `data2` directories
  c. If there are directories in the directory passed, Note that you are skipping them as in output above.

2. If no argument is passed at the commandline the script should respond with the usage and exit with code 101.
```
$ ./swgraham_lab2.sh
Usage: ./swgraham_lab2.sh dirname
$ echo $?
101
```

3. If the Directory does not exist, the script should output and exit with code 102:
   ```
   $ lab2.sh missingdirectory
   Error: the directory "missingdirectory" does not exist
   $ echo $?
   101
   ```
