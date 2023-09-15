all: paper.pdf note.pdf

sub: sub.pdf note.pdf

paper.pdf: paper.tex defs.tex abstract.tex intro3.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion2.tex related2.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex appendix-fcsl.tex appendix-clients.tex appendix-auxiliaries.tex appendix-stability.tex
	echo "\def\draftflag{1}">flags.tex
	pdflatex --jobname=paper paper
	bibtex paper -min-crossrefs=5 
	pdflatex paper --jobname=paper paper
	pdflatex paper --jobname=paper paper

note.pdf: note.tex
	pdflatex --jobname=note-to-reviewers note
	pdflatex --jobname=note-to-reviewers note

sub.pdf: paper.tex defs.tex abstract.tex intro3.tex relink-figure.tex readpair.tex overview.tex jy-histories3.tex jy-reorder.tex fcsl-snapshot2.tex specification2.tex formal3.tex specs.tex clients.tex fcsl-auxcode.tex auxiliary.tex proof2.tex atomics2.tex proof-write.tex proof-scan.tex discussion2.tex related2.tex conclusions.tex references.bib procs.bib jy-snapshot2.tex
	echo "\def\subflag{1}">flags.tex
	pdflatex --jobname=relink-ecoop paper
	bibtex relink-ecoop -min-crossrefs=5
	pdflatex --jobname=relink-ecoop paper
	pdflatex --jobname=relink-ecoop paper

clean:
	rm -f *~ *.aux *.log *.blg *.dvi *.bm *.vrb *.toc *.nav *.out *.snm *.lof *.lot *.zip *.rel *.ps *.bbl *.vtc flags.tex paper.pdf relink-ecoop.pdf note.pdf note-to-reviewers.pdf
