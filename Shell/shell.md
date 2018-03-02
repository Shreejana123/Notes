# Learning About Shell

Command line is an Interface for issuing commands to the operating System.

## **Manipulating file and directories**

## 1. pwd

This command stands for print working direcory. Returns the absolute path of current working directory.

```bash
pwd
home/pwl
```

## 2. ls

Short for "listing". Lists the contents of current working directory.

```bash
ls
```

The following displays the files in the provided directory.

    ls <directory>

**Note :** If a file path starts with `/` it is absolute else it is relative.

## 3. cd

Stands for Change Directory. Move around.

    cd PATH

## 4. cp

Stands for copy. It is used to copy a file from a specified path to another specified path. Can also copy directories

    cp <path1/file_name> <path2/new_filename>

You can also copy multiple files and save it to a directory.

    cp <file> <file> .. <directory>

## 5. mv

Stands for move. It is used to move a file to specified path. **mv also forks for directory**

    mv <file> <path>

Working method same as cp.
It can also be used to rename files directories

    mv old_file new_file

## 6. rm

Remove. removes or deletes files form specified path

    rm <files>

## 7. mkdir & rmdir

Makes and deletes directory respectively. Other commands are same for both files and directories except for these two.

```bash
rmdir directory_name
mkdir directory_name
```

**Note :** /tmp is used to store temporary files. (Linux)

## **Manipulating Data**

## 1. cat

Concatenate. Prints the content of file on screen.

    cat <files>

## 2. less

View less of the data.

    less <files>

**Note :** `:q` is used to quit `:spacebar` is used to scroll and `:n` is used to see next page.

## 3.head

Displays upto first 10 lines of the file.

    head <filename>

**Note :** `tab` can be used for completion.

## 4. flags

flags determine what extra actions to perform

    -n -F -R

* `-n` number
* `-R` Recursive
* `-F` Classify
* `-f` fields (columns)
* `-d` delimeters(seperators)

## 5. cut

Select columns from a file.

    cut -f 2-5,8 -d , values.csv

here `f` tells the number of fields to select and `-d` tells the seperator for the fields i.e `,` .`-f` must come before `-d`.

## 6. history

Lists out the past executed commands.

    history

`!` is used to call the command from history

## 7. grep

Takes a piece of text and searches it in the given file.

    grep <searchString> <filenames>

flags used in grep:

* `-c`: print a count of matching lines rather than the lines themselves
* `-h`: do not print the names of files when searching multiple files
* `-i`: ignore case (e.g., treat "Regression" and "regression" as matches)
* `-l`: print the names of files that contain matches, not the matches
* `-n`: print line numbers for matching lines
* `-v`: invert the match, i.e., only show lines that don't match

## **Combining Tools**

## 1. Storing output

`>` is used to direct an output to a destination.

    head source.txt > output.txt
