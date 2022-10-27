# Unix commands

You will learn the following commands.

- `ls`
- `cat`
- `head`
- `wget` or `curl`
- `tr`
- `grep`
- `cut`
- `sed`
- `xargs`

## `ls`

Command that lists directory contents of files and directories.

```bash
ls
```

## `cat`

Command to reads data from the file and gives their content as output.

```bash
cat [file...]
```

## `head`

Commands to print the top N number (default is top 10) of data of the given input.

```bash
head [file]
```

## `wget` or `curl`

Commands that can download contents from FTP, HTTP(S).


```bash
wget -q -O - https://example.com/
# -q means `quiet`
# -O - means return results to standard output

# The above command is equivalent to the following:
curl https://example.com/
```

## `tr`

Command for translating or deleting characters

```bash
echo "AAACCC" | tr "A" "T"

# reverse complement
echo "AAACCC" | tr "ACGT" "TGCA" | rev
```

## `grep`

Command for searching text and strings

```bash
# Search "S"
printf "Suzuki\nSato\nYamada\n" | grep "S"

# Search "a"
printf "Suzuki\nSato\nYamada\n" | grep "a"
```

## `cut`

Command for cutting out the sections from each line of files

```bash
echo "chr1,100,1000,tba" | cut -d, -f 1
#=> chr1
echo "chr1,100,1000,tba" | cut -d, -f 1-3
#=> chr1,100,1000
```

## `sed`

Command for substitution or for find and replace.

```bash
echo "TBA" | sed "s/TBA/Tsukuba Bioinfo Assembly/"
#=> Tsukuba Bioinfo Assembly
```


## `xargs`

Command for executing commands from standard input.

```bash
find data/ -type f |
    xargs grep "Tsukuba Bioinfo Assembly"

# The above command is equivalent to the following two commands:
grep data/tba1.html
grep data/tba2.html
```
