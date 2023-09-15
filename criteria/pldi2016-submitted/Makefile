all: paper.pdf ext comments

paper.pdf: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

comments: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex
	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"
	bibtex paper-commented -min-crossrefs=5
	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"
	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"

ext: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex
	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"
	bibtex paper-extended -min-crossrefs=5
	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"
	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"

quick:
	pdflatex paper




clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf

zip:
	zip paper.zip paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex

