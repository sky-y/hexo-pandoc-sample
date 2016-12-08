---
title: こんにちはPandoc
date: 2016-12-09 00:13:28
tags:
---

これはPandoc拡張Markdownによって書かれた記事です。
仕様は[Pandoc - Pandoc User’s Guide](http://pandoc.org/MANUAL.html#pandocs-markdown)を参照してください。

## 定義リスト

Term 1

:   Definition 1

Term 2 with *inline markup*

:   Definition 2

        { some code, part of Definition 2 }

    Third paragraph of definition 2.

## Haskellのソースコード

```haskell
qsort []     = []
qsort (x:xs) = qsort (filter (< x) xs) ++ [x] ++
               qsort (filter (>= x) xs)
```

## いくつかのテーブル

### Simple tables

Right     Left     Center     Default
-------     ------ ----------   -------
   12     12        12            12
  123     123       123          123
    1     1          1             1

Table:  Demonstration of simple table syntax.

### Multiline tables

-------------------------------------------------------------
 Centered   Default           Right Left
  Header    Aligned         Aligned Aligned
----------- ------- --------------- -------------------------
   First    row                12.0 Example of a row that
                                    spans multiple lines.

  Second    row                 5.0 Here's another one. Note
                                    the blank line between
                                    rows.
-------------------------------------------------------------

Table: Here's the caption. It, too, may span
multiple lines.

### Grid tables

: Sample grid table.

+---------------+---------------+--------------------+
| Fruit         | Price         | Advantages         |
+===============+===============+====================+
| Bananas       | $1.34         | - built-in wrapper |
|               |               | - bright color     |
+---------------+---------------+--------------------+
| Oranges       | $2.10         | - cures scurvy     |
|               |               | - tasty            |
+---------------+---------------+--------------------+

### Pipe tables

| Right | Left | Default | Center |
|------:|:-----|---------|:------:|
|   12  |  12  |    12   |    12  |
|  123  |  123 |   123   |   123  |
|    1  |    1 |     1   |     1  |

  : Demonstration of pipe table syntax.

## 数式

$$
E = mc^2
$$

りんごが$x$個、みかんが$y$個。

$$
\left( \begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & i
\end{array} \right)
$$

is given by the formula

$$
\chi(\lambda) = \left| \begin{array}{ccc}
\lambda - a & -b & -c \\
-d & \lambda - e & -f \\
-g & -h & \lambda - i
\end{array} \right|.
$$

## 脚注

これは脚注の参照です[^1]。

[^1]: これは脚注です。
