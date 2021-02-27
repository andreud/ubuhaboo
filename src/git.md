# Git

## Forget files that are tracked, but are in .gitignore

### Option 1 

Remove all files from repo, and then add them again, at this time the new entries in .gitignore will take effect.
No files will be deleted from working dir (disk) due to --cache flag.

```shell
# Step 1: remove desired files from repository
$ git rm --cached <file_1> <file_2> <file_n>
#  or whole folder
$ git rm --cached -r <folder>
#  or all the files/folders
$ git rm --cached -r .


# Step 2: add files again and create a new commit
$ git add .
$ git commit -m 'Remove ignored files'
```

Option 2:

use the git clean command to recursively remove files that are not under version control.
WARNING: does remove files form dir

```shell
$ git clean -xdn # to perform a dry run and see what will be removed.
$ git clean -xdf # to execute it.
```