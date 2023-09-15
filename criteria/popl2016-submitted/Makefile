all: paper.pdf

paper.pdf: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview.tex related.tex intro.tex cal.tex background.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

quick:
	pdflatex paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf

zip:
	zip paper.zip paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro.tex discussion.tex counting.tex overview.tex related.tex intro.tex cal.tex background.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf

