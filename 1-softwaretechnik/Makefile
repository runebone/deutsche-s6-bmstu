PDF = index.pdf
CC = pdflatex
FLAGS = 
SHIT = *.aux *.log *.out *.toc *.bbl *.blg *.nav *.snm

all: pres

pres : main.tex # preamble.tex
	-$(CC) $(FLAGS) $<
	-$(CC) $(FLAGS) $<
	-mv main.pdf $(PDF)
	make moveout

moveout:
	-mkdir -p out > /dev/null
	# -mkdir -p out/report > /dev/null
	-mv $(SHIT) out > /dev/null
	# -cd report && mv *.aux ../out/report > /dev/null

resurrect:
	# -mv out/report/* report > /dev/null
	-mv out/* . > /dev/null

clean:
	-rm  $(SHIT) > /dev/null
	# -cd report && rm $(SHIT) > /dev/null
	rm -rf out

.PHONY: all, clean, bib, moveout, resurrect
