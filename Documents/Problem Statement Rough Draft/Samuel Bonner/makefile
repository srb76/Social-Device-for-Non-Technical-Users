TARGET=group_29
HTML=main_html
SRC={group_29_writeup}

latex: 
	latex group_29.tex
	dvips -R -Poutline -t letter group_29.dvi -o group_29.ps
	ps2pdf group_29.ps
	
clean: 
	rm group_29.ps
	rm group_29.aux
	rm group_29.dvi
	rm group_29.log