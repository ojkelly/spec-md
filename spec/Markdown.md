# Markdown

Spec Markdown is first and foremost [Markdown](http://daringfireball.net/projects/markdown/syntax).
More specifically, it's based on [Github-flavored Markdown](https://help.github.com/articles/github-flavored-markdown/).

This section explains the syntax and capabilities of Markdown that Spec Markdown
supports and augments.


## Character Encoding

Markdown allows you to write text which uses &, <, and >. The output HTML will
automatically use the `&amp;`, `&lt;`, and `&gt;` entities.

Well formed HTML entities can be written inline directly. If you write `&copy;`,
it will appear in the HTML output as &copy;.


### Escape sequence

Markdown makes use of certain characters to format text, in order to render one
explicitly, place a backslash before it.

You can type \*literal asterisks\* instead of emphasis by typing
`\*literal asterisks\*`.

Escaping does not apply within code.

Spec Markdown provides backslash escapes for the following characters:

```
\   backslash
`   backtick
*   asterisk
_   underscore
{}  curly braces
[]  square brackets
()  parentheses
#   hash mark
+   plus sign
-   minus sign (hyphen)
.   dot
!   exclamation mark
|   pipe         <-- added in Spec Markdown
<   less-than    <-- added in Spec Markdown
>   greater-than <-- added in Spec Markdown
```


## Inline formatting

Markdown allows for inline stylistic and structual formatting. Inline
formatting is allowed in paragraphs, list items, and table cells.


### Links

This is an [-->*example*<--](https://www.facebook.com) of a link.

```
This is an [-->*example*<--](https://www.facebook.com) of a link.
```

The linked text can contain any inline formatting except for other links.

TODO: links do not yet support a title attribute.


### Emphasis

Wrapping asterisks *(\*)* indicate emphasis. Like Github-flavored
Markdown, Spec Markdown does not treat underscore *(_)* as emphasis.

Example of **bold** and *italic* and ***bold italic***.

```
Example of **bold** and *italic* and ***bold italic***.
```


### Inline Code

Wrapping back-ticks *(\`)* indicate inline code, text inside back-ticks is not
formatted, allowing for special characters to be used in inline code without
escapes.

This is an `example` of some inline code.

```
This is an `example` of some inline code.
```

TODO: Markdown's double-back-tick syntax is not yet supported.


### Images

```
![Specs](http://stmcoatech.com/Admin/Welding/d639c91b-f07b-4629-83fd-a00739c21b57.jpg)
```

![Specs](http://stmcoatech.com/Admin/Welding/d639c91b-f07b-4629-83fd-a00739c21b57.jpg)

TODO: the title attribute is not yet supported


## Blocks

Markdown allows for block-level structual formatting. Every block is seperated
by at least two new lines. Spec Markdown makes use of Markdown's blocks to
produce more specific structural formatting.


### Section Headers

Regular Markdown supports two styles of headers, Setext and atx, however Spec
Markdown generally only supports atx style headers.

```
# Header
```

Setext headers are not supported by Spec Markdown.

```!
Header
------
```

The number of `#` characters refers to the depth of the section. To produce an,
`<h3>`, type `###`. Optionally, a header may be "closed" by any number of `#`
characters.

Note: Spec Markdown requires that documents start with `#` and that each section
contained within is only one level deeper. An \<h1> section may only contain
\<h2> sections.


### Paragraphs

Paragraphs are the most simple Markdown blocks. Lines are appended together to
form a single \<p> tag. Any inline syntax is allowed within a paragraph.


### Lists

TODO

And this is a list

  1. this
  2. is
  3. a
    - nested
  4. list

And this is a non-indented list

1. this
2. is
3. a
  - nested
4. list


### Code Block

TODO


## Not yet implemented

TODO


### Block Quotes

TODO


### Horizontal Rules

TODO: Spec Markdown does not yet support \<hr>


### Automatic Links

TODO