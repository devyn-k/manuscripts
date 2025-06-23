# Makefile for compiling icaif23-2.tex

TEX=pdflatex
BIBTEX=bibtex
TITLE=cbfds_icaif25

SRC=$(TITLE).tex
BIB=references.bib
PDF=$(TITLE).pdf
AUX=$(TITLE).aux

all: $(PDF)

$(PDF): $(SRC) $(BIB) $(wildcard figures/*.png)
	$(TEX) $(SRC)
	$(BIBTEX) $(TITLE)
	$(TEX) $(SRC)
	$(TEX) $(SRC)
	open $(PDF)

clean:
	rm -f *.aux *.bbl *.blg *.log *.out *.toc *.lof *.lot *.gz *.nav *.snm *.synctex.gz *.fdb_latexmk *.fls *.vrb *.bcf *.run.xml *.xdv *.pdf

.PHONY: all clean 