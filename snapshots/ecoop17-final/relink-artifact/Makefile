artifact: artifact.tex references.bib
	pdflatex --jobname=relink-artifact artifact
	bibtex relink-artifact -min-crossrefs=3
	pdflatex --jobname=relink-artifact artifact
	pdflatex --jobname=relink-artifact artifact

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl *.vtc relink-artifct.pdf
