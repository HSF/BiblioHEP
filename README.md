# BiblioHEP - a collection of useful BibTeX references for HEP

## How to use this package

We recommend to checkout this package, so that the repository can be used in any of your documents.
Be sure to `git pull` to have the latest updates.

We recommend bibliography management with `biblatex`:
- Copy all `.bib` files under a `BiblioHEP` directory (the local `git clone` is enough).
- In your LaTeX document, add all the `.bib` files you need using biblatex's `addbibresource`.

Here is a little example:

```
% Run with, e.g.,
%    pdflatex my_test_document
%    biber my_test_document
%    pdflatex my_test_document
%    pdflatex my_test_document

\documentclass{article}

\usepackage{hyperref}
\usepackage[style=numeric,sorting=none]{biblatex}

\addbibresource{BiblioHEP/events_hep.bib}
\addbibresource{BiblioHEP/software.bib}
% ...

\begin{document}

\title{My Test Document}
\maketitle

\section{Introduction}

This is a set of useful \texttt{.bib} files prepared by the HSF~\cite{HSF}.


%\clearpage
\printbibliography[title={References},heading=bibintoc]

\end{document}
```


## Contributing

We very much welcome contributions, but please check that the references being added don't already exist in one of the `.bib` files.
If you feel it would be useful to create new `.bib` files, kindly create an issue to discuss the idea.
Otherwise, update the file relevant for events, publications, software or sites, following the simple comments at the top of each file,
which are there to help with organisation

It is a good idea to run locally a little example `.tex` document similar to the one given below with your additions, to ensure
there are no warnings and the citations render correctly.

For adding information to this page or improving it,
we follow the [pull request](https://help.github.com/articles/using-pull-requests/) workflow in GitHub:
simply fork the repository, edit the files you want to edit, push them to your fork, and open a pull request.
(No need to create a fork if you are part of the HSF team with special rights on the repository, of course.)