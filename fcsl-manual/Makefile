all: paper.pdf

paper.pdf: paper.tex content.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls defs.tex
	pdflatex --jobname=fcsl-manual paper
	bibtex fcsl-manual -min-crossrefs=5
	pdflatex --jobname=fcsl-manual paper
	pdflatex --jobname=fcsl-manual paper

quick:
	pdflatex --jobname=fcsl-manual paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl fcsl-manual.pdf

zip:
	zip paper.zip paper.tex content.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls defs.tex Makefile 

