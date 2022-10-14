# Fundamentals of Agro-Environmental Data Science

# Exercise 4 - Create documents with Markdown

This is a learning/reading exercise, with several tasks. You should repeat all 
the examples given in your system, and check that you obtain equivalent results.

## Introduction

Markdown [1] is a simple markup language to create formated text using a plain text editor.
Text written in Markdown is easy to read because you can apply formats to titles, 
subtitles, ordered and unordered lists, bold and italic type faces, tables, etc. 
The syntax of Markdown is very simple and easy to learn and use. It will also speed 
up your workflow.

Documents writen in Markdown normally have the extension `.md`, which facilitates 
applications to identify its format. Most text editors - Notepad++, Atom, 
Visual Studio Code, Sublime Text - have plugins to preview Markdown formated 
text, or to export to other file formats as HTML or pdf.

The goal of this exercise is to create a dummy plain text document in Markdown,
to demonstrate the different formating syntax.

## 1. Prepare your environment
For this exercise, you can use *Visual Studio Code*. But lets start by creating
an empty file in bash

1. Open a bash terminal
2. Navigate to the directory where you save your FADS exercises, using `cd`
3. Create a new directory for this exercise with the command `mkdir`. Name it,
for example, *fads-ex-04*
4. `cd` to inside the new created directory
5. Create the new empty file with the name `markdown-tutorial.md`:
   ````
   $ touch markdown-tutorial.md
   ````
6. Confirm that the new file was created, but it is empty, using `ls -l`
7. If Visual Studio Code is in your path, you can open it directly from the bash
with the command:
   ```
   $ code markdown-tutorial.md
   ```
   Visual Studio Code should recognise automatically that this is a Markdown file.
   Check that looking at the status bar, on the bottom-right corner of your 
   window.
8. If you want, you can split your window to see a preview on the right. Press 
``CTRL+k`` and then `v`.

## 2. Format Titles (headings)
To set titles, you use the the cardinal character: `#`. The number of cardinals 
defines the level of the title. 
```
# This is a main (first level) title
```
# This is a main (first level) title

```
## This is a second level title
```
## This is a second level title

```
### This is a third level title
```
## This is a third level title

## 3. Create emphasis
You can use **bold** type face or *italic* to give empahsis to your text. This 
is also very simple. To format with bold, use two asterists `*` to mark the start
and end of the bold text:
```
The following four words **are in bold typeface**, but the rest are not.
```
The following four words **are in bold typeface**, but the rest are not.

And, for italic:
```
The following four words *are in italic typeface*, but the rest are not.
```
The following four words *are in italic typeface*, but the rest are not.


Sometimes, you want to cite someones' text. For that you use ``blockquote``
```
> text blockquote
```
> text blockquote

## 4. Create lists
To create ordered lists, you simply, place a number and a point before the item:
```
1. Item one
2. Item two
3. Item three
```
1. Item one
2. Item two
3. Item three

And, if the list in not ordered (with bullets), the use a slash `-`

```
- Item one
- Item two
- Item three
```
- Item one
- Item two
- Item three

## 5. Addind code
Sometimes, it is good to highlight code, so that the reader understands that it 
should be written as it is shown in the terminal or program. The code can be 
highlighted in line with the text:
```
This sentence has `this portion of code` inline.
```
This sentence has `this portion of code` inline.

Or you can create blocks of code using ` ``` `:
````
```
def printMyName(name):
   a = name
   print(a)
```
````
```
def printMyName(name):
   a = name
   print(a)
```
## 6. Add links and images
Sometimes, you may want to include links to other documents. This can be down as the
following:
```
[Markdown Guide](https://www.markdownguide.org/)
```
[Markdown Guide](https://www.markdownguide.org/)

By the way, this is a functional link where you can learn more.

Likewise, you can include images. It is similar to the link, but you need to 
set carefully the relative paths of the image in relation to the place of the 
current markdown file:
```
![Logo do ISA](./images/logo_ISA.png)
```
![Logo do ISA](./images/LogoISA.png)

Can you explain the path to the image?

## 7. Add Tables

It is also possible to create tables in Markdowm. Simple use `|` to set the columns
and `---` below the first row with the column headings:
```
|ID| Column 1| Column 2| Column 3|
|--|---------|---------|---------|
|1 | item 1  | item 2  | item 3  |
|2 | item 4  | item 5  | item 6  |
```
|ID| Column 1| Column 2| Column 3|
|--|---------|---------|---------|
|1 | item 1  | item 2  | item 3  |
|2 | item 4  | item 5  | item 6  |

There are many online tools to convert CSV files to Markdown and vice-versa.

## 8. Explore more with a cheat sheet
To check more options, go online and check a [cheat sheet](https://www.markdownguide.org/cheat-sheet/).

## Wrap up
In this exercise, we learned 
- what is Markdown, and what's for
- the very basics of quick mark up with Markdown including:
  - headings
  - bold and italic type faces
  - lists
  - links
  - images
  - tables


# References
[1] https://daringfireball.net/projects/markdown/syntax









