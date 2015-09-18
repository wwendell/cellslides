all: index2.html index.html

index.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 index.adoc -o index2.html

copies: Makefile
	cp ~/work/cells/imgs/hs_a2.svg imgs/
	cp ~/work/cells/imgs/hs_a2_log_fit.svg imgs/
	cp ~/work/cells/imgs/aging_cartoon.svg imgs/

movie: Makefile
	ffmpeg -y -i ~/work/cells/mov/poly_N160_F0.55.mp4  -acodec libvorbis -aq 5 -ac 2 -qmax 25 -threads 2 imgs/poly_N160_F0.55.webm

clean:
	rm -f index{,2}.html index-ref.adoc

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
