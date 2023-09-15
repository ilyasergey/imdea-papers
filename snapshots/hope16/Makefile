all: paper.pdf

paper.pdf: paper.tex defs.tex mathpartir.sty abstract.tex intro2.tex references.bib procs.bib 
	echo "\def\draftflag{1}">flags.tex
	pdflatex --jobname=paper paper
	bibtex paper -min-crossrefs=5 
	pdflatex paper --jobname=paper paper
	pdflatex paper --jobname=paper paper

sub:
	echo "">flags.tex
	pdflatex --jobname=paper-sub paper
	bibtex paper-sub -min-crossrefs=5
	pdflatex --jobname=paper-sub paper
	pdflatex --jobname=paper-sub paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl *.vtc flags.tex paper.pdf paper-sub.pdf
