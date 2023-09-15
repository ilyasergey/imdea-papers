all: paper.pdf

paper.pdf: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings-short.bib sigplanconf.cls defs.tex
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

quick:
	pdflatex paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl

zip:
	zip paper.zip paper.tex lstcoq.tex mathpartir.sty references.bib proceedings-short.bib sigplanconf.cls
