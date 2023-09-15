all: sub.pdf

sub.pdf: paper.tex defs.tex abstract.tex intro3.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion2.tex related2.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex
	pdflatex  paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.vtc flags.tex paper.pdf 
