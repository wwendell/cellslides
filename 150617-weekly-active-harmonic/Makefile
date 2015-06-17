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
