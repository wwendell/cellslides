all: index2.html index.html

index.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc imgs/* Makefile
	asciidoctor -b html5 index.adoc -o index2.html

copies: Makefile | imgs
	cp -u ~/work/cells/imgs/example-diffusion-P-t.svg imgs/
	cp -u ~/work/cells/imgs/example-mixed-P-t.svg imgs/
	cp -u ~/work/cells/imgs/example-diffusion-caged.svg imgs/
	cp -u ~/work/cells/imgs/example-gaussian-pairs-alpha2.svg imgs/
	cp -u ~/work/cells/imgs/hs_steps_F0.57.svg imgs/
	cp -u ~/work/cells/imgs/hs_steps_F0.58.svg imgs/
	cp -u ~/work/cells/imgs/hs_steps_F0.59.svg imgs/
	
	# cp -u ~/work/cells/imgs/hs_a2.svg imgs/
	cp -u ~/work/cells/imgs/hs_a2_log_fit.svg imgs/
	cp -u ~/work/cells/imgs/hardspheresNs_a2.svg imgs/
	cp -u ~/work/cells/imgs/hardspheresNs_a2_fit.svg imgs/
	# cp -u ~/work/cells/imgs/hardspheresNs_a2_fit_phistar.svg imgs/
	cp -u ~/work/cells/imgs/hardspheresNs_a2_fit_params.svg imgs/
	
	
	cp -u ~/work/cells/imgs/aging_cartoon.svg imgs/
	cp -u ~/work/cells/imgs/hslocpairs_a2_time_f0.55.svg imgs/
	cp -u ~/work/cells/imgs/hslocpairs_a2_time_f0.57.svg imgs/
	cp -u ~/work/cells/imgs/hslocpairs_a2_time_f0.58.svg imgs/
	
	cp -u ~/work/cells/imgs/hs_steps_fitted_F0.584.svg imgs/
	
imgs:
	mkdir imgs

clean:
	rm -f index{,2}{,_local}.html

local: index.html index2.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index.html > index_local.html
	sed 's_https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.4.0_file:///usr/share/mathjax_' index2.html > index2_local.html
