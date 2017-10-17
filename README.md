# taskwarrior

Scripts and tools to help with using TaskWarrior, both in the terminal (scripts) and on MacOS (applets, services, etc.).

## scripts

### taskchain

This is a bash version of the taskchain command.  Usage:

`taskchain <list of space-separated task ids>`

This command creates a dependency heirarchy of blocked tasks.  The first task must be completed before you can work on the second task.  The second task must be completed before you can work on the third task.  

Use example:

`taskchain 1 2 3`

This is the same as:

`task 2 modify depends:1`

`task 3 modify depends:2`