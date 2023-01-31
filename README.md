# Clean-Thesis

This repository contains the template for my phd thesis, that I am sharing in the hope that it might be useful to someone.

The template uses the Komascript classes as a base, and LuaLaTeX to improve and simplify the fonts management. Moreover, it uses the package `glossaries` to manage the acronyms and symbols lists, and the `biblatex` package with `biber` backend to manage the bibliography.

To build the pdf file, it should be sufficient to run `make` from the root of the project, while `make clean` is also available to remove all the auxiliary files.

Moreover, `make continuos` opens an instance of a pdf viewer and continuosly whatch the document to detect for saved changes in order to trigger a recompilation.

## Note for windows users

I have no idea how to make a `make` equivalent on windows, so thats a problem. The `.latexmkrc` file should still work though, so one could in principle copy the command present in the `Makefile`, for conveniency reported here:

```bash
latexmk -pdf -bibtex-cond1 -lualatex -use-make thesis.tex
```

Still, there are some changes to do in the `.latexmkrc` file, that should be easy to notice by reading the file content.
