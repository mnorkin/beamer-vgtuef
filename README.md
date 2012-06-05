# VGTU EF BEAMER COLOR TEMPLATE

[![](https://dummas.files.wordpress.com/2012/06/screen.png)](http://dummas.wordpress.com)

This is a simple color template, based on Vilnius Gediminas Technical University logo color pallete.


# INSTALLATION
* Copy/Move `beamercolorthemevgtuef.sty` file to `/use/share/texmf-dist/tex/latex/beamer/themes/color`
* Run `texhash` in command promp


# USAGE
* After defining all the require packages, include this line, before document tag:

```
\usetheme{Dresden}
\usecolortheme{vgtuef}
```

# ALSO
* It is also quite recommended to define these lines before color scheme definition:

```
\newcommand*\oldmacro{}
\let\oldmacro\insertshortinstitute % save previous 	definition
\renewcommand*\insertshortinstitute{
  \leftskip=.3cm
  \oldmacro\hfill\insertframenumber\,/\,\inserttotalframenumber
}
\let\oldshorttitle\insertshorttitle
\renewcommand*\insertshorttitle{
  \leftskip=0.4cm
  \oldshorttitle\hfill Vilnius
}
```

# EXAMPLE

```
\documentclass{beamer}
\usepackage[lithuanian]{babel}
\usepackage[utf8x]{inputenc}
\usepackage[L7x]{fontenc}
\usepackage{lmodern}
\usepackage{caption}
\usepackage{subfig}
\usepackage{graphicx}

\newcommand*\oldmacro{}
\let\oldmacro\insertshortinstitute % save previous definition
\renewcommand*\insertshortinstitute{
  \leftskip=.3cm % before the author could be a plus1fill ...
  %\insertframenumber\,/\,\inserttotalframenumber\hfill\oldmacro}
  \oldmacro\hfill\insertframenumber\,/\,\inserttotalframenumber}
  
\let\oldshorttitle\insertshorttitle
\renewcommand*\insertshorttitle{
	\leftskip=0.4cm
\oldshorttitle\hfill Vilnius
}

\usetheme{Dresden}
\usecolortheme{vgtuef}

\logo{\includegraphics[height=20px]{img/vgtu_ef.jpg}}

\title[Foo bar]{Foo bar line 1\\Foo bar line 2}
\author[F. Bar]{Foo Bar, FB-99}
\institute[VGTU Elektronikos fakultetas]{
  Vilniaus Gedimino technikos universitetas\\
  Elektronikos fakultetas\\
  Elektroninių sistemų katedra\\
  \texttt{foo@bar.org}
}

\begin{document}

  \begin{frame}
    \titlepage
  \end{frame}

\end{document}
```
