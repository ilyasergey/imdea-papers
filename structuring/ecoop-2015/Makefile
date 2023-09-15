all: paper.pdf

paper.pdf: paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib llncs.cls related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.pdf stages.pdf
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

quick:
	pdflatex paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf

zip:
	zip paper.zip paper.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib llncs related.tex intro.tex overview.tex development.tex defs.tex underhood.tex conclusion.tex evaluation.tex more.tex dependencies.pdf stages.pdf 
