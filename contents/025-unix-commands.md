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
# LICENSE  README.md  contents  data
```

## `cat`

Command to reads data from the file and gives their content as output.

```bash
cat data/tba1.html
# <!-- data/tba1.html -->
# <p> Hello TBA! </p> <p> Hello Tsukuba Bioinfo Assembly! </p>
```

## `head`

Commands to print the top n number (default is top 10) of data of the given input.

- `-n`: to specify the number of lines to print (default: 10).


```bash
head -n 3 data/output_lists.txt
# https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf
# https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf
# https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2018_H30_mondai.pdf
```

## `wget` or `curl`

Commands that can download contents from FTP, HTTP(S).


```bash
wget -q -O - https://example.com/
# `-q` means `quiet`
# `-O -` means return results to standard output

# The above command is equivalent to the following:
curl https://example.com/
```

## `tr`

Command for translating or deleting characters

```bash
echo "AAACCC" | tr "A" "T"
#=> TTTCCC
```

FYI: Reverse complement using `tr` and `rev`.

```bash
echo "AAACCC" | tr "ACGT" "TGCA" | rev
#=> GGGTTT
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

- `-d`: to specify a delimiter (default: TAB `\t`).
- `-f`: to select a specified field.

```bash
echo "chr1,100,1000,tba" | cut -d, -f 1
#=> chr1
echo "chr1,100,1000,tba" | cut -d, -f 1-3
#=> chr1,100,1000
```

## `sed`

Command for substitution or for find and replace.

For example, to replace 'TBA' to 'Tsukuba Bioinfo Assembly':

```bash
echo "TBA" | sed "s/TBA/Tsukuba Bioinfo Assembly/"
#=> Tsukuba Bioinfo Assembly
```

Importantly, sed can use **regular expressions**.
For example, `^` means the beggining of a word.

So if you want to add a term to the beggining of a word, you can replace `^`.

```bash
echo "TBA" | sed "s/^/Hello /"
#=> Hello TBA
```

## `xargs`

Command for executing commands from standard input.

```bash
find data/ -type f |
    xargs grep "Tsukuba Bioinfo Assembly"
```
The above command is equivalent to the following two commands:

```bash
grep data/tba1.html
grep data/tba2.html
```
