# Linux command sheetsheet
Have fun Harry!!

## How directory names work
The root directory is `/`, that is the very highest folder of your computer

Your home directory is where you start, you can reference your home directory with `/home/your_username` or the shortcut `~/`

If you want to reference the current directory use `./`. For example say you have an executable `hello_world.sh`, use `./hello_world.sh` because it's in the current directory.

If you want to reference the directory above use `../`. For example you could move up a directory with `cd ../`
## Moving around
### Change directory
To change directory use `cd`:
```
$ cd your_directory
```
Examples:
```
$ cd Programming/doeppner_dance_club
```
Which move from your current directory --> Programming --> doeppner_dance_club
```
$ cd ../backups
```
Which moves up a directory, then into backups
### List directory
To list the contents of the current directory use:
```
$ ls
```
To list the contents of a specific directory use
```
$ ls your_directory
```
## Creating, editing, moving, and deleting files and directories
### Create file
To create a file use `touch`:
```
$ touch your_file
```
Multiple filenames separated with spaces will create multiple files.
### Create directory
To create a directory use `mkdir`:
```
$ mkdir your_directory
```
### Editing files
To edit a file use your choice of text editor, good choices are `vim` or `nano` (these are just command line options, you can also use gui programs like `vscode` and `apostrophe` which I'm using to write this)

Open the file with:
```
$ your_editor your_file
```
If you open a file and it says something like "file is read only", close the file and use:
```
$ sudo your_editor your_file
```
### Moving files or directory
To move a file or directory use `mv`:
```
$ mv source destination
```
Example:
```
$ mv hello_world.asm asm_programs
```
Which moves hello_world.asm into the asm_programs directory.

Beware, if the destination you are moving the source into doesn't exist, it will rename the file to whatever directory you typed.

Though, this is useful for renaming.
### Renaming a file or directory
To rename a file or directory use `mv`, and set the destination as a name that doesn't exist in the current directory:
```
$ mv hello_world.txt hehehehaw.txt
```
Which renames hello_world.txt to hehehehaw.txt. This also works for directories
### Deleting a file or directory
To delete a file use `rm`:
```
$ rm your_file
```
If you want to remove a directory, use the `-r` (recursive) flag:
```
$ rm -r your_directory
```
If the file or directory is protected and you still want to remove it use `sudo` and the `-f` (force) flag:
```
$ sudo rm -f protected_file
```
```
$ sudo rm -rf protected_directory
```
## Extracting
If you get a file like a `.zip` or a `.tar` you need to extract it.

### Zip files
To extract a zip (`.zip`) use `unzip`
```
$ unzip your_zip.zip
```
### Tarballs
To extract a tarball (anything that has `.tar` in the extension) use `tar -xvf`
```
$ tar -xvf your_tarball.tar.gz
```
## Installing programs
Programs come in a variety of ways, the most common are:
- Distrobution specific packages like `.deb` files which can be stored either in the official repositories or elsewhere
- Tarballs
- App Images
- Flatpaks
### Distrobution specific
To install a distrobution specific package use (for debian based):
```
$ sudo apt install package_name
```
If it isn't in your distrobution's repository, search for it in a web browser and use whatever they have.

If they have a distrobution specific package, download it, `cd` to it and use (for debian):
```
$ sudo apt install package_name.deb
```
