---
title : File Test using Notestex-Markdown
author: Josué Meneses Díaz
institute: Universidad de Santiago de Chile 
numbersections: true
email: josue.meneses@usach.cl
---

\part{Example for Notestex Markdown}
# Introduction {#sec:1} 
Notestex markdown is a simple template to convert markdown files to pdf using [**Notestex**](https://github.com/Adhumunt/NotesTeX) @dhumuntarao2021 package through Pandoc. The simple command to use is:

```bash
pandoc INPUT_FILE.md --template ./template_notestex.tex -o ./OUTPUT_FILE.pdf
```
In the Header (yaml) of markdown file, you need pass

```yaml
title : TITLE_DOC
author: Your name
institute: INSTITUTE
numbersections: true
email: email@mail
```
If you don't pass any of them parameters them pandoc not generate the cover and the table of content:

- `title:` This is the title of the document.
- `author:` The name of the author of document.
- `institute:` The name of institute 
- `numbersections:` this add the number to the part and section.
- `email:` you email adress.

You can create different part using the LaTeX command `\part{}`. In general, you can use everyone command latex available on notestex package like `margintable`, `marginfigure`, etc (see @sec:2 for examples).

# Using Margin {#sec:2}

\begin{margintable}\vspace{.8in}\footnotesize
	\begin{tabularx}{\marginparwidth}{|X}
		Introduction \ref{sec:1}\\
		Using Margin \ref{sec:2}\\
		Examples of enviroments \ref{sec:3}\\
	\end{tabularx}
\end{margintable}

\begin{marginfigure}
\begin{center}
	\begin{tikzpicture}
		\draw[black,thick] (-1,-1) -- (-.06,-.06);
		\draw[black,thick] (.06,.06) -- (1,1);
		\draw[black,thick] (-1,1) -- (1,-1);
		\filldraw[black] (-1,-1) circle (2pt) node[anchor=north] {2};
		\filldraw[black] (-1,1) circle (2pt) node[anchor=south] {1};
		\filldraw[black] (1,-1) circle (2pt) node[anchor=north] {3};
		\filldraw[black] (1,1) circle (2pt) node[anchor=south] {4};
	\end{tikzpicture}
\end{center}
\caption{Marginfigure: Tikz. Example from source of Notestex}
\end{marginfigure}

\begin{margintable}\footnotesize 
		\begin{tabularx}{\marginparwidth}{|X}
			\href{https://www.ctan.org/pkg/fontenc}{fontenc}\\
			\href{https://www.ctan.org/pkg/mathrsfs}{mathrsfs}\\			
			\href{https://www.ctan.org/pkg/array}{array}\\
			\href{https://www.ctan.org/pkg/tabularx}{tabularx}\\
			\href{https://www.ctan.org/pkg/booktabs}{booktabs}\\
		\end{tabularx}
		\caption{Links}
	\end{margintable}

The package Notestex add different margin to add on the right document. For example

```latex
\begin{margintable}\vspace{.8in}\footnotesize
	\begin{tabularx}{\marginparwidth}{|X}
		Example for Notestex Markdown \ref{sec:1}\\
		Section~\ref{sec:reqpackages}. Required Packages\\
		Section~\ref{sec:license}. Margins\\
	\end{tabularx}
\end{margintable}

```
Create a table on the margin. See notestex document for more examples.

\newpage
\part{Environments}

# Examples of environments (Notestex) \label{sec:3}
You can use equation like:

$$ \frac{\partial x}{\partial y} = \int xdx $$

And environments like  

\begin{example}
	Calculate $$y=\int xdx$$
\end{example}

\begin{definition}
		The \texttt{definition} environment and the associated \texttt{tcolorbox} are provided by the following code in \texttt{NotesTeX.sty}:
\end{definition}

# Using References on markdown notestex
You can use bibtex using the filter padoc-citeproc @macfarlane2021 to create reference on the document. 

\part{Reference}

























