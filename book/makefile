latexfile = book

dvi: $(latexfile).tex
	latex $(latexfile).tex && makeindex $(latexfile).idx && bibtex $(latexfile) && latex $(latexfile).tex && latex $(latexfile).tex

ps: $(latexfile).dvi
	dvips -Ppdf -G0 $(latexfile).dvi

pdf: $(latexfile).ps
	ps2pdf $(latexfile).ps

all: $(latexfile).tex
	latex $(latexfile).tex && makeindex $(latexfile).idx && bibtex $(latexfile) && latex $(latexfile).tex && latex $(latexfile).tex && dvips -Ppdf -G0 $(latexfile).dvi && ps2pdf $(latexfile).ps

clean: 
	latexmk -c

PDF: $(latexfile).pdf
	xpdf $(latexfile).pdf
