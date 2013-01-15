all: drawafriend.pdf
	
drawafriend.pdf: drawafriend.bbl *.tex
	pdflatex drawafriend.tex 

drawafriend.bbl: *.bib
	pdflatex drawafriend.tex 
	bibtex drawafriend
	pdflatex drawafriend.tex 

# pdf: paper.pdf
# 
# paper.dvi: *.tex figures/*.eps *.bib
# 	latex paper.tex
# 	bibtex paper
# 	latex paper.tex
# 	latex paper.tex
# 
# paper.pdf: paper.dvi
# 	dvips -Ppdf -G0 -o paper.ps paper.dvi
# 	ps2pdf -dCompatibilityLevel=1.3 -dMaxSubsetPct=100 -dSubsetFonts=true -dEmbedAllFonts=true -dAutoFilterColorImages=false -dAutoFilterGrayImages=false -dColorImageFilter=/FlateEncode -dGrayImageFilter=/FlateEncode -dMonoImageFilter=/FlateEncode paper.ps paper.pdf
# 	cp paper.pdf paper2.pdf

clean:
	rm -fv *.log *.pdf *.ps *.dvi *~ *.aux *.blg *.bbl
