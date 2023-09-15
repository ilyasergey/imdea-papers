all: paper.pdf

paper.pdf: paper.tex sigplanconf.cls abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty authors.tex exchange_code.tex client_fig.tex exchange_proof.tex
	pdflatex paper
	bibtex paper -min-crossrefs=5
	pdflatex paper
	pdflatex paper

paper-self.pdf: paper.tex sigplanconf.cls abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty authors.tex exchange_code.tex client_fig.tex exchange_proof.tex
	pdflatex --jobname=non-linearizable-oopsla16 "\def\crflag{}\input{paper}"
	bibtex non-linearizable-oopsla16 -min-crossrefs=5
	pdflatex --jobname=non-linearizable-oopsla16 "\def\crflag{}\input{paper}" 
	pdflatex --jobname=non-linearizable-oopsla16 "\def\crflag{}\input{paper}"

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
	zip paper.zip Makefile paper.tex sigplanconf.cls abstract.tex lstcoq.tex mathpartir.sty bibmacros.bib references.bib proceedings.bib sigplanconf.cls defs.tex Makefile intro1.tex discussion.tex counting.tex overview1.tex related.tex cal1.tex background1.tex counter.pdf chist.pdf qclients.tex conclusion.tex chist2.pdf queue.pdf evaluation.tex exchanger_outline.tex oopsla2016.sty authors.tex exchange_code.tex client_fig.tex exchange_proof.tex aec-badge.pdf

