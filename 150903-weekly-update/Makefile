all: index2.html index.html

index.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 index.adoc -o index2.html

copies: imgs/* Makefile
	cp ~/work/cells/imgs/exp_a2.svg imgs/
	cp ~/work/cells/imgs/exp_MSD.svg imgs/
	cp ~/work/cells/imgs/exp_hs_compare_a2.svg imgs/
	cp ~/work/cells/imgs/exp_hs_compare_msd.svg imgs/
	cp ~/work/cells/imgs/hs_a2.svg imgs/
	cp ~/work/cells/imgs/HS-WCA-a2-F0.58.svg imgs/
	cp ~/work/cells/imgs/WCA-potential.svg imgs/
	cp ~/work/cells/imgs/WCA-LJ-potential.svg imgs/
	cp ~/work/cells/imgs/hs_steps_F0.55.svg imgs/
	cp ~/work/cells/imgs/hs_steps_F0.57.svg imgs/
	cp ~/work/cells/imgs/hs_steps_F0.58.svg imgs/
	cp ~/work/cells/imgs/hs_steps_F0.582.svg imgs/
	cp ~/work/cells/imgs/Pdr_T0.44_t1e6_s3_N100_n1.0_vadd.svg imgs/LJ_steps.svg
	

clean:
	rm -f index{,2}.html index-ref.adoc

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
