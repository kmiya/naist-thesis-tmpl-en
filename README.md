naist-thesis-tmpl-en
===============================

A modern LaTeX template for your doctoral dissertation or master's thesis of NAIST Graduate School of Information Science.

(Japanese version is [here](https://github.com/kmiya/naist-thesis-tmpl))

## Features
The template:

- consists of some `.tex` files instead of a `.sty` file for the sake of usability and customizability.
- uses the [KOMA-Script](http://texcatalogue.ctan.org/entries/koma-script.html) bundle which provides replacements for the article, report, and book classes with emphasis on typography and versatility.
- uses `hyperref.sty` which produces hypertext links in the document.

## Usage

    $ git clone git@github.com:kmiya/naist-thesis-tmpl-en.git

or [click this link](https://github.com/kmiya/naist-thesis-tmpl-en/archive/master.zip) to download as zip.

### Directory Structure

```
.
├── thesis.pdf                # sample PDF file
├── thesis.tex                # main tex file
└── tex
    ├── cmembers.tex          # write your (co-)supervisor's name
    ├── personal_setting.tex  # write your student number, title, abstract, etc.
    ├── setting.tex           # write LaTeX settings such as macros
    ├── chap1.tex
    ├── chap2.tex
    ├── chap3.tex
    ├── conclusions.tex
    ├── references.tex
    ├── publist.tex
    ├── acknowledgements.tex
    └── class_setting         # you don't need to change the following files
        ├── eabstract.tex
        └── titlepage.tex
```

#### `tex/personal_setting.tex`
Write the following items to the file:

- **type** of the thesis (`Doctoral Dissertation` or `Master's Thesis`)
- **degree** (`Doctor` or `MASTER`)
- **major** (`ENGINEERING` or `SCIENCE`)
- **student number** (e.g., doctor: `DD123456`, master: `MT123456`)
- **title** of your thesis
- **your name**
- **abstract** of the thesis
- **keywords** of the thesis

## FAQ

#### ``Contents'' should contain itself
Change the following line of `setting.tex`

```tex
\usepackage[nottoc]{tocbibind}
```

to

```tex
\usepackage{tocbibind}
```

Notice that the change might break the layout of ``Contents'' on a certain LaTeX environment. (Thanks [matcha-shake](https://github.com/matcha-shake)).
