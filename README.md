# Notestex for Markdown
 A simple template to convert markdown files to pdf using [**Pandoc**](https://pandoc.org/) and the package [NotesTeX](https://github.com/Adhumunt/NotesTeX).

## Folder
- **example :** A simple example of markdown file with the configuration for creating a pdf with the package NotesTex
- **filter :** Local Pandoc files necessary to create the pdf file with Notestex.
- **notestex:** Copy of files from the Notestex Github.
- **template:** The template used to create the pdf file using Pandoc. See the example file or makefile for parameters to Pandoc.

## Introduction
To create a document, simply write a normal markdown file using your favorite program (for example [**Zettlr**](https://www.zettlr.com/)). When you wish to create a pdf file.
The minimal yaml header is

```yaml
title : TITLE_DOC
author: Your name
institute: INSTITUTE
numbersections: true
email: email@mail
```

If you don't use that the cover and table of contents is not going to create.

The magic of this template is when you use [**Pandoc**](https://pandoc.org/). The minimal command for creating the pdf is:

```bash
pandoc INPUT_FILE.md --template ./template_notestex.tex -o ./OUTPUT_FILE.pdf

```

the template files can be found in the folder `template\template_notestex.tex`. Is necessary that Latex and Notestex there installed. 

For a more complex example, please see the `example` folder. For more command see the documentation on the official Github for [**NotesTeX**](https://github.com/Adhumunt/NotesTeX).

