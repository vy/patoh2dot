PATOH2DOT = ../patoh2dot
DOT2TEX   = /usr/bin/dot2tex
LATEX     = /usr/bin/latex
PDFLATEX  = /usr/bin/pdflatex

%.dot: %.g
	$(PATOH2DOT) $*.g $@

%.tex: %.dot
	$(DOT2TEX) -tmath --prog neato $*.dot >$@

%.pdf: %.tex
	$(PDFLATEX) $*

all:
	make hypergraph-{0,1,2,3}.dot
	make hypergraph-{0,1,2,3}.tex
	make hypergraph-{0,1,2,3}.pdf
	rm -f *.log *.aux

clean:
	rm -f *.tex *.dot *.aux *.log *.pdf

.PHONY: all clean
