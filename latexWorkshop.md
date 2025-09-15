# Latex workshop

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
