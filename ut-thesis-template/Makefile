# make -f Makefile_pdflatex

R = ut-thesis
STY = *.cls
FIG = images/*.pdf

pdf: $(R).pdf

$(R).bbl: $(R).bib
	pdflatex $(R)
	bibtex $(R)
	pdflatex $(R)

$(R).pdf: *.tex $(STY) $(FIG) $(R).bbl
	pdflatex $(R)
	pdflatex $(R)
	pdflatex $(R)

clean:
	rm -f $(R).log $(R).aux $(R).bbl $(R).blg $(R).out $(R).toc $(R).pdf
