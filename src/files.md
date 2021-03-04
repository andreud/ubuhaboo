# Files

In Unix [Everything is a file](https://en.wikipedia.org/wiki/Everything_is_a_file)

## Reading files

Basics 

```shell
$ cat
$ more # You can use / for search
$ less # You can use / for search and n for navigate. used by man
$ head
$ tail

```

Getting only the lines that contain a given string ("foo"):
```shell
$ grep foo README.txt
# Optianlly include a number of lines Before and After
$ grep -B 3 -A 2 foo README.txt
```
## Searching for files

```shell
# Files in /path with log extension
$ find /path -type f -name "*.log" 

# Files/dirs by name case insensitive
$ find / -iname Company

# Files edited in the las 10 minutes
$ find / -mtime 10

```
