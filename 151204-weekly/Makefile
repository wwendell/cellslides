all: index2.html index.html

index.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 index.adoc -o index2.html

copies: Makefile | imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_t100_n100.svg imgs		
	cp -u ~/work/cells/imgs/hs_steps_F0.59.svg imgs/
	
	cp -u ~/work/cells/imgs/inherent_found_n100_t100.svg imgs/
	
	cp -u ~/work/cells/imgs/rearrange_n100_s68_F0.005.mp4 imgs/
	cp -u ~/work/cells/imgs/micro-rearrange_n100_s22_F0.001.mp4 imgs/
	
	cp -u ~/work/cells/imgs/cartoon-rearrange-lowphi.svg imgs/
	cp -u ~/work/cells/imgs/cartoon-rearrange-midphi.svg imgs/
	cp -u ~/work/cells/imgs/cartoon-rearrange-highphi-arrow.svg imgs/
	
imgs:
	mkdir imgs

clean:
	rm -f index{,2}{,_local}.html

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
