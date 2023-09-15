all: paper.pdf

paper.pdf: paper.tex defs.tex lstcoq.tex mathpartir.sty abstract.tex intro2.tex readpair.tex overview.tex jy-snapshot.tex jy-histories.tex jy-reorder.tex fcsl-snapshot.tex auxiliary.tex formal3.tex specs.tex proof.tex clients.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix-fcsl.tex  appendix-code.tex
	pdflatex --jobname=paper paper
	bibtex paper -min-crossrefs=5 
	pdflatex paper --jobname=paper paper
	pdflatex paper --jobname=paper paper

sub:
	pdflatex --jobname=paper-sub paper
	bibtex paper-sub -min-crossrefs=5
	pdflatex --jobname=paper-sub paper
	pdflatex --jobname=paper-sub paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.vtc flags.tex paper.pdf paper-sub.pdf
