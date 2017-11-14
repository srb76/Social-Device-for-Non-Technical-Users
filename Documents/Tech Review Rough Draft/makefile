LATEX_SRC := $(shell egrep -l '^[^%]*\\begin\{document\}' *.tex)

all: techreview.pdf

$(LATEX_SRC:%.tex=%.pdf): %.pdf: *.tex
	latex -shell-escape -interaction=nonstopmode $*.tex
	bibtex $*
	latex -shell-escape -interaction=nonstopmode $*.tex
	latex -shell-escape -interaction=nonstopmode $*.tex
	dvips -R -Poutline -t letter $*.dvi -o $*.ps
	ps2pdf $*.ps

clean:
	rm -f *.pdf *.ps *.dvi *.out *.log *.aux *.bbl *.blg *.pyg

.PHONY: all clean