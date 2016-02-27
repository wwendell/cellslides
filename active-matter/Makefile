all: index2.html index.html

index.html: index-ref.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index-ref.adoc -o index.html

index2.html: index-ref.adoc imgs/* Makefile
	asciidoctor -b html5 index-ref.adoc -o index2.html
	
index-ref.adoc: index.adoc cell-diffusion-bibtex.bib
	asciidoc-bib -b cell-diffusion-bibtex.bib -s "american-physics-society" index.adoc

copies: Makefile | imgs
	cp -uv ../150521/imgs/janus-h202-traj.png imgs/
	cp -uv ../150521/imgs/f62_r{0,20}.mp4 imgs/
	cp -uv ~/work/cells/imgs/randkick4H-MSD-cut-f0.5-R20-N40-e10.svg imgs/
	cp -uv ~/work/cells/imgs/randkick4H-MSD-cut-f0.63-R20-N40-e1000.svg imgs/
	cp -uv ~/work/cells/imgs/randkick4H-MSD-cut-f0.63-R200-N40-e1000.svg imgs/
	
imgs:
	mkdir imgs

clean:
	rm -f index{,2}{,_local}.html index-ref.adoc

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
