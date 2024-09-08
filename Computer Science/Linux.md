[[linux-commands-handbook.pdf]]
# Commands
### man / tldr
Explains the use of another command
- `man <command>`
tldr is a simplified version of man
- `tldr <command>`

### ls
List directory contents
- `ls -a` : List all files
- `ls -1` : List in a column
- `ls -F` : List all files classified with symbols
- `ls -l` : Long format list with size
- `ls -lh` : Long format list with size in units

### cd
Change Directory
- `cd path/to/destination` : Go to destination
- `cd ..` : Go back to parent directory
- `cd  ` : Home directory
- `cd /` : Root directory

### pwd
Print working directory
- `pwd`

### mkdir
Create a directory
- `mkdir path/to/destination`

### rmdir
Remove a directory
- `rmdir path/to/destination`

### mv
Move a file/directory or rename a file/directory
- `mv source destination` : move to destination
- `mv source unexisting_target` : rename source to target if it does not exist
### cp
Copy a file 
- `cp file destination` : copy file to destination
- `cp -r file destination` : copy folder and its contents to destination

### touch
Create a file 
- `touch file_name`

### find
Find files matching a particular search pattern.
- `find . -name '*.extension'`

### gzip
Compress files
- `gzip file` : Compress file and replace it with the compressed `.gz` version.
- `gzip -k:` Compress a file and keep the original file
- `gzip -c filename > filename.gz` : Compress a file and and specify the name.
- `gzip -d` : Decompress file and replace it with the decompressed `.gz` version.
- `gzip -c -d filename.gz > filename` : Decompress file and specify the name.
