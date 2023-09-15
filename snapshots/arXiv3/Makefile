
ext: paper.tex defs.tex abstract.tex intro2.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix-fcsl.tex appendix-clients.tex appendix-auxiliaries.tex appendix-stability.tex
	pdflatex --jobname=relink-extended paper
	bibtex relink-extended -min-crossrefs=5
	pdflatex --jobname=relink-extended paper
	pdflatex --jobname=relink-extended paper
	mv relink-extended.bbl paper.bbl 

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.vtc flags.tex paper.pdf relink-esop.pdf relink-extended.pdf *.bbl

