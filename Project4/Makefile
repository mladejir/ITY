SHELL = /usr/bin/env bash
NAME = proj4

$(NAME).pdf: $(NAME).ps
	pdflatex $(NAME).tex

$(NAME).ps: $(NAME).dvi
	dvips -sPAPERSIZE=a4 $(NAME).dvi

$(NAME).dvi: $(NAME).tex 
	latex $(NAME).tex
	bibtex $(NAME)
	latex $(NAME).tex
	latex $(NAME).tex
clean:
	-rm $(NAME).ps $(NAME).dvi $(NAME).aux  $(NAME).log $(NAME).out
zipit:
	zip xmlade01-fit.zip $(NAME).tex Makefile czechiso.bst $(NAME).bib
