all: artifact.pdf

artifact.pdf: artifact.tex
	pdflatex --jobname=fcsl-artifact artifact
	pdflatex --jobname=fcsl-artifact artifact

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl *.vtc fcsl-artifact.pdf
