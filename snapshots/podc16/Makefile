all: paper.pdf

paper.pdf: paper.tex defs.tex lstcoq.tex mathpartir.sty cover.tex abstract.tex intro2.tex readpair.tex overview.tex jy-snapshot.tex jy-histories.tex jy-reorder.tex fcsl-snapshot.tex fcsl-sts.tex auxiliary.tex formal2.tex jy-relink.tex proof.tex clients.tex related.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix.tex
	pdflatex paper 
	bibtex paper -min-crossrefs=5
	pdflatex paper 
	pdflatex paper 

quick:
	pdflatex --jobname=paper-nosts "\def\nosts{}\input{paper}"
	bibtex paper-nosts -min-crossrefs=5
	pdflatex --jobname=paper-nosts "\def\nosts{}\input{paper}"
	pdflatex --jobname=paper-nosts "\def\nosts{}\input{paper}"

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf paper-nosts.pdf


