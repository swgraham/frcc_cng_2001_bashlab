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

# Bash Lab 2 (Graded)

Create a bash script that takes a directory as an argument and prints the list of files and how many lines and words are in each file. If the directory doesn't exist it should notify user.

## Input

Use the directory data in this repo as the Directory name

Example: 
./scriptname.sh data

## Output
```
==========================================================
=              Files in Directory: data                  =
==========================================================
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
1. The script should ONLY output the above, if there are directories in the directory `data` they should be ignored.

2. The script should work if the directory does not exist. The output should ONLY be:

```
$ ./scriptname.sh data1
Directory data1 does not exist
```
