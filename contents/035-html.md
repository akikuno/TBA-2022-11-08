# HTML 101

## What is HTML?

HTML stands for Hyper Text Markup Language for creating Web pages.

This is a simple example of HTML.

```html
<!DOCTYPE html>
<html>
<head>
<title>Page Title</title>
</head>
<body>

<h1>My First Heading</h1>
<p>My first paragraph.</p>

</body>
</html>
```

## Angle brackets `<` `>` represents one content in HTML

HTML elements consist of a left angle bracket (<), followed by name of the tag and closed by a right angular bracket (>).

```html
<p> Hello TBA! </p>
```

## So what...???

Since **one line represents one content in (almost all) Unix commands**, you need to convert a format to parse HTML.

The following two HTMLs are the exactly same.

```html
# data/tba1.html
<p> This is TBA </p> <p> This is Tsukuba Bioinfo Assembly </p>
```

```html
# data/tba2.html
<p>
    This is TBA
</p>

<p>
    This is Tsukuba Bioinfo Assembry
</p>

```

In contrast, the following commands return different outputs.

```bash
grep 'TBA' data/tba1.html
# <p> This is TBA </p> <p> This is Tsukuba Bioinfo Assembly </p>
```

```bash
grep 'TBA' data/tba2.html
#  This is TBA
```

**To parse HTML, transform `>` to `\n`.**  
`\n` means a new line.

```bash
cat data/tba1.html | tr ">" "\n" | grep 'TBA'
#  This is TBA </p
```

```bash
cat data/tba2.html | tr ">" "\n" | grep 'TBA'
#  This is TBA
```

