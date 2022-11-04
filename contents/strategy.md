# How to think about a problem

## Set your goal⛳

The first and most important point is to consider what your goal is.

For me, the goal is to summarize lists of all the URLs from [the site](https://www.jsbi.org/activity/nintei/sankou_mondai_kako/).  

The input is the follwoing HTML.  

<details>
<summary>Details</summary>

### Input: HTML

```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="format-detection" content="telephone=no" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <title>参考問題・過去問 | Japanese Society for Bioinformatics - JSBi</title>

(~~~Omitted 中略~~~)

    <p>過去の問題・解説</p>

    <p>2021年度（令和3年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2021%E8%A7%A3%E8%AA%AC.pdf" style="margin-right: 5px; margin-left: 5px; background-color: rgb(255, 255, 255);">解説</a></p>

    <p>2020年度（令和2年度）※2020年度より解説のみの掲載となりました。 <a href="media/files/2020%E8%A7%A3%E8%AA%AC.pdf">解説</a></p>

    <p>2019年度（平成31年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf">解説</a></p>

    <p>2018年度（平成30年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2018_H30_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2018_H30_kaisetsu.pdf">解説</a></p>

    <p>2017年度（平成29年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2017_H29_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2017_H29_kaisetsu.pdf">解説</a></p>

    <p><span style="color:#FF0000;"><strong>※2017年度出題 問18について、解説に以下補足をいたします。</strong></span></p>

    <p><span style="color:#FF0000;">一般に単為生殖は有性生殖の一形態とされること<wbr />が多いが、子の遺伝子セットが親のものと同一になるという点で無<wbr />性生殖に含める立場もある。<wbr />その点で選択肢3は曖昧さがあったが、選択肢１は明らかに不適切<wbr />であることから、こちらを正解とする。</span><span style="font-size: 11px;">（解説文には後日追記をいたします）</span></p>

    <p>2016年度（平成28年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2016_H28_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2016_H28_kaisetsu.pdf">解説</a></p>

    <p>2015年度（平成27年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2015_H27_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2015_H27_kaisetsu.pdf">解説</a></p>

    <p>2014年度（平成26年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2014_H26_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2014_H26_kaisetsu.pdf">解説</a></p>

    <p>2013年度（平成25年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2013_H25_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2013_H25_kaisetsu.pdf">解説</a></p>

    <p>2012年度（平成24年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2012_H24_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2012_H24_kaisetsu.pdf">解説</a></p>

    <p>2011年度（平成23年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2011_H23_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2011_H23_kaisetsu.pdf">解説</a></p>

    <p>2010年度（平成22年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2010_H22_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2010_H22_kaisetsu.pdf">解説</a></p>

    <p>2009年度（平成21年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2009_H21_mondai_kaitou_ver2.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2009_H21_kaisetsu.pdf">解説</a></p>

    <p>2008年度（平成20年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2008_H20_mondai_kaitou.pdf">問題と解答</a></p>

    <p>2007年度（平成19年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2007_H19_mondai_kaitou.pdf">問題と解答</a></p>
</div>

(~~~Omitted 以下略~~~)
```
</details>

The output is a list of the URLs.

<details>
<summary>Details</summary>

### Output: URLs of the PDFs

```text
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2018_H30_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2018_H30_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2017_H29_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2017_H29_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2016_H28_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2016_H28_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2015_H27_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2015_H27_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2014_H26_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2014_H26_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2013_H25_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2013_H25_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2012_H24_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2012_H24_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2011_H23_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2011_H23_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2010_H22_mondai.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2010_H22_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2009_H21_mondai_kaitou_ver2.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2009_H21_kaisetsu.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2008_H20_mondai_kaitou.pdf
https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2007_H19_mondai_kaitou.pdf
```

</details>

After getting the list, you can download all files using `for loop`, `while loop`, or `xargs`, whichever you want.

```bash
cat output_lists.txt | xargs wget
```


From now on, Let's consider how to reach the goal.


## Divide a problem

We can divide the problem into these parts.

- Download HTML
- Find links to PDFs
- Format the links

### 1. Download HTML

You can use `wget` or `curl` to download HTML.

```bash
# return HTML to standard output
wget -O - https://www.jsbi.org/activity/nintei/sankou_mondai_kako/
```

```bash
# return HTML to standard output
curl https://www.jsbi.org/activity/nintei/sankou_mondai_kako/
```

### 2. Find links to PDFs

First, you need to modify the HTML format a little bit.  
Elements of HTML are separated into tags, which start from `<`.  
In contrast, the elements of files that Shell can handle are separated in a new line, which is `\n`.  
This means Shell prefers **one element per line**.

Here is an example of HTML.  

This HTML is unsuitable because we need two links in one line.  

```html
# data/example.html
    <p>2019年度（平成31年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf">問題</a> <a href="media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf">解説</a></p>
```

We need **one link per line**.

To get one link per line, use `tr` command to translate `>` to `\n` and use `grep`.

```bash
cat data/example.html | tr ">" "\n" | grep pdf
# 2019年度（平成31年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf"
#  <a href="media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf"
```

### 3. Format links

We got links to PDFs. So far, so good!😀  

However, this output includes unrelated characters such as "2019年度（平成31年度） <a href=".  

```text
2019年度（平成31年度） <a href="media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf"
  <a href="media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf"
```

You can delete these characters one by one but wait a minute⏲️

Let's focus on separators.

If you separate the text by `"`, you can extract only the links by selecting Field 2.

| Field 1                         | Field 2                                                            | Field 3 |
| ------------------------------- | ------------------------------------------------------------------ | ------- |
| 2019年度（平成31年度） <a href= | media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf     |         |
| <a href=                        | media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf |         |

To separate the text, use `cut`✂️.

```bash
cat data/example.html | tr ">" "\n" | grep pdf | cut -d '"' -f 2
# media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf
# media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf
```

Lastly, add `https://www.jsbi.org/` at the beginning to make a complete URL using `sed`.

```bash
cat data/example.html | tr ">" "\n" | grep pdf | cut -d '"' -f 2 | sed "s|^|https://www.jsbi.org/|"
# https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_mondai.pdf
# https://www.jsbi.org/media/files/activity/nintei/sankou_mondai_kako/2019_kaisetsu_r.pdf
```

Finally, you get the complete URLs to PDFs.

Then you can download PDFs using `xargs` and `wget`.

```bash
cat data/example.html | tr ">" "\n" | grep pdf | cut -d '"' -f 2 | sed "s|^|https://www.jsbi.org/|" | xargs wget
```

FYI, if you are not uncomfortable using `xargs`, you can use `while`.

```bash
cat data/example.html | tr ">" "\n" | grep pdf | cut -d '"' -f 2 | sed "s|^|https://www.jsbi.org/|" |
    while read url; do
        echo "$url" is now downloading...
        wget -q "$url"
    done
```


This is it. Hooray!🎉
