all: paper.pdf

paper.pdf: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty authors.tex exchange_code.tex client_fig.tex exchange_proof.tex
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

cover: cover.tex
	pdflatex cover
	pdflatex cover

# comments: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex
# 	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"
# 	bibtex paper-commented -min-crossrefs=5
# 	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"
# 	pdflatex --jobname=paper-commented "\def\extcomm{}\input{paper}"

# ext: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex
# 	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"
# 	bibtex paper-extended -min-crossrefs=5
# 	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"
# 	pdflatex --jobname=paper-extended "\def\extflag{}\input{paper}"

quick:
	pdflatex paper




clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl paper.pdf
	rm -rf diff

zip:
	zip paper.zip paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty paper.bbl authors.tex exchange_code.tex client_fig.tex exchange_proof.tex

prediff: paper.tex abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty authors.tex exchange_code.tex client_fig.tex exchange_proof.tex
	rm -rf diff
	mkdir diff
	cp ./{paper.tex,abstract.tex,authors.tex,exchange_code.tex,client_fig.tex,exchange_proof.tex,client_fig.tex,lstcoq.tex,mathpartir.sty,bibmacros.bib,references.bib,proceedings.bib,sigplanconf.cls,defs.tex,counter.pdf,chist.pdf,chist2.pdf,queue.pdf,oopsla2016.sty} diff
	latexdiff ../oopsla2016-first/paper.tex ./paper.tex > diff/paper.tex
	latexdiff ../oopsla2016-first/intro1.tex ./intro1.tex > diff/intro1.tex
	latexdiff ../oopsla2016-first/discussion.tex ./discussion.tex > diff/discussion.tex
	latexdiff ../oopsla2016-first/counting.tex ./counting.tex > diff/counting.tex
	latexdiff ../oopsla2016-first/overview1.tex ./overview1.tex > diff/overview1.tex
	latexdiff ../oopsla2016-first/cal1.tex ./cal1.tex > diff/cal1.tex
	latexdiff ../oopsla2016-first/background1.tex ./background1.tex > diff/background1.tex
	latexdiff ../oopsla2016-first/qclients.tex ./qclients.tex > diff/qclients.tex
	latexdiff ../oopsla2016-first/authors.tex ./authors.tex > diff/authors.tex
	latexdiff ../oopsla2016-first/conclusion.tex ./conclusion.tex > diff/conclusion.tex
	latexdiff ../oopsla2016-first/evaluation.tex ./evaluation.tex > diff/evaluation.tex
	latexdiff ../oopsla2016-first/related.tex ./related.tex > diff/related.tex
	latexdiff ../oopsla2016-first/exchanger_outline.tex ./exchanger_outline.tex > diff/exchanger_outline.tex


diff: prediff
	cd ./diff; pdflatex paper; bibtex paper -min-crossrefs=5; pdflatex paper; pdflatex paper


cleandiff:
	rm -rf diff
