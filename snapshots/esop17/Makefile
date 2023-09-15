all: paper.pdf

paper.pdf: paper.tex defs.tex lstcoq.tex mathpartir.sty abstract.tex intro2.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix-fcsl.tex appendix-clients.tex appendix-auxiliaries.tex appendix-stability.tex
	echo "\def\draftflag{1}">flags.tex
	pdflatex --jobname=paper paper
	bibtex paper -min-crossrefs=5 
	pdflatex paper --jobname=paper paper
	pdflatex paper --jobname=paper paper

sub: paper.tex defs.tex lstcoq.tex mathpartir.sty abstract.tex intro2.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex
	echo "\def\subflag{1}">flags.tex
	pdflatex --jobname=relink-esop paper
	bibtex relink-esop -min-crossrefs=5
	pdflatex --jobname=relink-esop paper
	pdflatex --jobname=relink-esop paper

ext: paper.tex defs.tex lstcoq.tex mathpartir.sty abstract.tex intro2.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix-fcsl.tex appendix-clients.tex appendix-auxiliaries.tex appendix-stability.tex
	echo "\def\extflag{1}">flags.tex
	pdflatex --jobname=relink-extended paper
	bibtex relink-extended -min-crossrefs=5
	pdflatex --jobname=relink-extended paper
	pdflatex --jobname=relink-extended paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl *.vtc flags.tex paper.pdf relink-esop.pdf relink-extended.pdf
