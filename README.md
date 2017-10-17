# taskwarrior

Scripts and tools to help with using TaskWarrior, both in the terminal (scripts) and on MacOS (applets, services, etc.).

## scripts

### taskchain

This is a bash script version of the taskchain command.

#### Installation:

You may want to install this in /usr/local/bin, or you can run it directly from your home directory.

You will need to set executable permissions on the file:

`chmod +x taskchain`

If the file is in your executable path you can run it directly:

`taskchain 1 2 3	`

If the file is in your home directory, you can run it anywhere with:

`~/taskchain 1 2 3`

#### Usage:

`taskchain <list of space-separated task ids>`

This command creates a dependency heirarchy of blocked tasks.  The first task must be completed before you can work on the second task.  The second task must be completed before you can work on the third task.  

Use example:

`taskchain 1 2 3`

This is the same as:

`task 2 modify depends:1`

`task 3 modify depends:2`