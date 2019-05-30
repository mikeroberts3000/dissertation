# make -f Makefile_pdflatex

R = 00_main
OO = mike_roberts_dissertation_
STY = *.sty
FIG = images/*/*.pdf

#Grab the GIT description
ver := $(shell git describe --dirty)

pdf: $(R).pdf

$(R).bbl: $(R).bib
	pdflatex $(R)
	bibtex $(R)
	pdflatex $(R)

$(R).pdf: *.tex $(STY) $(FIG) $(R).bbl
	pdflatex $(R)
	pdflatex $(R)
	pdflatex $(R)
	pdflatex $(R)
	cp $(R).pdf $(OO).pdf

clean:
	rm -f $(R).log $(R).aux $(R).bbl $(R).blg $(R).out $(R).toc $(R).lot $(R).lof $(R).pdf
