all: index2.html index.html

index.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 index.adoc -o index2.html

copies: Makefile | imgs
	cp -u ~/work/cells/imgs/n100_r1.4_s100_F0.001_t2.png imgs
	
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.00001_t100_n40.svg  imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.00002_t100_n40.svg  imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.00005_t100_n40.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.0001_t100_n40.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.0002_t100_n40.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.0005_t100_n40.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_d0.001_t100_n40.svg imgs
	
	cp -u ~/work/cells/imgs/hsdphi_steps_t100_n40.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_steps_t100_n100.svg imgs
	
	cp -u ~/work/cells/imgs/hs_steps_F0.59.svg imgs/
	
	cp -u ~/work/cells/imgs/hsdphi_a2s.svg imgs
	cp -u ~/work/cells/imgs/hsdphi_a2s_log.svg imgs
	
	cp -u ~/work/cells/imgs/hs_a2_log_fit.svg imgs/
	
imgs:
	mkdir imgs

clean:
	rm -f index{,2}{,_local}.html

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
