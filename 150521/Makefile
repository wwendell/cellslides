all: index2.html index.html

index.html: index-ref.adoc
	asciidoctor -T ~/code/ascreveal/templates/slim index-ref.adoc -o index.html

index2.html: index-ref.adoc
	asciidoctor index-ref.adoc -o index2.html
	
index-ref.adoc: index.adoc cell-diffusion-bibtex.bib
	asciidoc-bib -b cell-diffusion-bibtex.bib -s "american-physics-society" index.adoc
	
clean:
	rm -f index{,2}.html index-ref.adoc