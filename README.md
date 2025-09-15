# Latex workshop

## Create a figure

```latex
%Add the following two lines to the top of your document
\usepackage{graphicx}
\usepackage{float}

%Add the following where you want your figure to be inserted
\begin{figure}[H]
\centering
\includegraphics{img/my-image.png}
\caption{Billedtekst her}
\label{fig:my-figure-label}
\end{figure}
```

### Figure list

To add a list of your included figures, add the following line in your section
where you want it to appear

```latex
\listoffigures
```

## Create a table

```latex
\begin{table}[H]
\centering
\begin{tabular}{|c|l|}
\hline
Linje nr & Indhold \\
\hline
\hline
1 & Tabel eksempel \\
2 & Tabel eksempel \\
\hline
3 & Tabel eksempel \\
\hline
\end{tabular}
\caption{Caption}
\label{tab:my-label}
\end{table}
```

### List of figures

In the same way we can create a list of our figures, can we create a list of our
tables:

```latex
\listoftables
```

## Multiple bibliographies in latex

Main document

```latex
\documentclass{article}
\usepackage{graphicx} % Required for inserting images
\usepackage{biblatex}
\addbibresource{ref.bib}


\title{studylab-latex-workshop-demo}
\author{Oliver Starup}
\date{September 2025}

\begin{document}

\maketitle

\section{Introduction}
As seen in \cite{example2025}, which we can not see in \cite{smith2024}
\section{References}
% Primary literature
\printbibliography[
  keyword={Projekt-rapport},
  notkeyword={Samarbejdsrapport},
  title={Primær litteratur}
]

% Secondary literature
\printbibliography[
  keyword={background},
  notkeyword={Samarbejdsrapport},
  title={Sekundær litteratur}
]
\end{document}
```

ref.bib

```latex
@book{example2025,
  author    = {jane doe},
  title     = {example book},
  year      = {2025},
  publisher = {example press},
  keywords  = {Projekt-rapport,background}
}
@book{smith2024,
  author    = {John Smith},
  title     = {Advanced Example Studies},
  year      = {2024},
  publisher = {Sample Publishing},
  keywords  = {background}
}
```
