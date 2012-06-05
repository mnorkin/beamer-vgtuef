This is a simple color template, based on Vilnius Gediminas Technical University logo color pallete.


# INSTALLATION
* Copy/Move `beamercolorthemevgtuef.sty` file to `/use/share/texmf-dist/tex/latex/beamer/themes/color`
* Run `texhash` in command promp


# USAGE
* After defining all the require packages, include this line, before document tag:

  $  \usetheme{Dresden}
  $  \usecolortheme{vgtuef}


# ALSO
* It is also quite recommended to define these lines before color scheme definition:

  $  \newcommand*\oldmacro{}
  $  \let\oldmacro\insertshortinstitute % save previous 	definition
  $  \renewcommand*\insertshortinstitute{
  $    \leftskip=.3cm
  $    \oldmacro\hfill\insertframenumber\,/\,\inserttotalframenumber
  $  }
  $  \let\oldshorttitle\insertshorttitle
  $  \renewcommand*\insertshorttitle{
  $    \leftskip=0.4cm
  $    \oldshorttitle\hfill Vilnius
  $  }

