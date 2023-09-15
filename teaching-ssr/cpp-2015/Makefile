all: paper.pdf

paper.pdf:
	pdflatex teaching-ssr
	bibtex teaching-ssr -min-crossrefs=5
	pdflatex teaching-ssr
	pdflatex teaching-ssr

quick:
	pdflatex teaching-ssr

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl

zip:
	zip teaching-ssr.zip teaching-ssr.tex lstcoq.tex mathpartir.sty references.bib proceedings.bib sigplanconf.cls
