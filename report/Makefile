# Makefile to create PDF documents from LaTeX files
# Author: Samuel Diebolt <samuel@diebolt.io>
# No license

DOC=main

COMPILER=/Library/TeX/texbin/pdflatex
ARGS=--shell-escape

RM=/bin/rm

$(DOC).pdf: $(DOC).tex
	$(COMPILER) $(ARGS) $(DOC).tex -draftmode
	$(COMPILER) $(ARGS) $(DOC).tex 

.PHONY: all clean cleanall

all: $(DOC).pdf

clean:
	$(RM) -f *.tox *.aux *.log *.out *.glg *.gls *.glo *.ist *.log *.toc *.acn *.acr *.alg *.bbl *.blg

cleanall: clean
	$(RM) -f *.pdf
