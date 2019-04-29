---
layout: post
categories: [ Jekyll, tutorial ]
image: assets/images/home.jpg
tags: featured
permalink: "tables-with-markdown"
---

### Tables

Basic table example of a table with two columns and three lines (when not
counting the header) is as follows:

```
| Column 1 | Column 2 |
|----------|----------|
| foo      | bar      |
| baz      | qux      |
| quux     | quuz     |
```

The leading and succeeding pipe characters (`|`) on each line are optional:

```
Column 1 | Column 2
---------|---------
foo      | bar
baz      | qux
quux     | quuz
```

However for one-column table, at least one of those has to be used, otherwise
it would be parsed as a Setext title followed by paragraph.

Leading and trailing whitespace in a table cell is ignored and the columns do
not need to be aligned.

```
Column 1 |Column 2
---|---
foo | bar
baz| qux
quux|quuz
```

It's possible to specify alignment of a table column by colon in the line separating table head from its body.

```
| Column 1 | Column 2 | Column 3 | Column 4 |
|----------|:---------|:--------:|---------:|
| default  | left     | center   | right    |
```

To include a literal pipe character in any cell, it has to be escaped.

```
Column 1 | Column 2
---------|---------
foo      | bar
baz      | qux \| xyzzy
quux     | quuz
```

Contents of each cell is parsed as an inline text which may contents any
inline Markdown spans like emphasis, strong emphasis, links etc.

```
Column 1 | Column 2
---------|---------
*foo*    | bar
**baz**  | [qux]
quux     | [quuz](/url2)

[qux]: /url
```
