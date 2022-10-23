# HTML 101

## Angle brackets `<` `>` represents one content in HTML

HTML elements consist of a left angle bracket (<), followed by name of the tag and closed by a right angular bracket (>).

```html
<p> Hello TBA! </p>
```

# So what...???

Since **one line represents one content in (almost all) Unix commands**, you need to convert a format to parse HTML.

In a nutshell, the following two lines are the exactly same in HTML,

```html
# data/tba1.html
<p> Hello! Tsukuba Bioinfo Assembly! </p>
```

```html
# data/tba2.html
<p>
Hello!
Tsukuba Bioinfo Assembly!
</p>
```

On the other hands, the following commands return different outputs.

```bash
grep 'e' data/tba1.html
# <p> Hello! Tsukuba Bioinfo Assembly! </p>
```

```bash
grep 'e' data/tba2.html
# Hello!
# Tsukuba Bioinfo Assembly!
```
