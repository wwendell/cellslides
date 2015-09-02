all: index2.html index.html

index.html: index.adoc
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc
	asciidoctor -b html5 index.adoc -o index2.html

copies:
	cp ~/work/cells/imgs/randkick4H-MSD-cut-f0.72-R20-N40-e72.svg imgs/
	cp ~/work/cells/imgs/randkick4H-MSD-cut-f0.72-R20-N40-e1000.svg imgs/
	cp ~/work/cells/imgs/randkick4H-MSD-f0.68-R20-N40-e1000.svg imgs/
	cp ~/work/cells/imgs/rsqsbis5-{MSD,a2,a2-relaxed}-t2000.svg imgs/
	cp ~/work/cells/imgs/rsqsbis5-relaxtimes.svg imgs/
	cp ~/work/cells/imgs/randkick4H-MSD-f0.72-R20-N40-e72.svg imgs/

clean:
	rm -f index{,2}.html index-ref.adoc

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
