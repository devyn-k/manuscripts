# Makefile for compiling icaif23-2.tex

TEX=pdflatex
BIBTEX=bibtex
SRC=icaif23-2.tex
BIB=references.bib
PDF=icaif23-2.pdf
AUX=icaif23-2.aux

all: $(PDF)

$(PDF): $(SRC) $(BIB) $(wildcard figures/*.png)
	$(TEX) $(SRC)
	$(BIBTEX) icaif23-2
	$(TEX) $(SRC)
	$(TEX) $(SRC)
	open $(PDF)

clean:
	rm -f *.aux *.bbl *.blg *.log *.out *.toc *.lof *.lot *.gz *.nav *.snm *.synctex.gz *.fdb_latexmk *.fls *.vrb *.bcf *.run.xml *.xdv *.pdf

.PHONY: all clean 