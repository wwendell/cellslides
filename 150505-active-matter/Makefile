all: index.html

index.html: index-ref.adoc
	asciidoctor -T ~/code/ascreveal/templates/slim index-ref.adoc -o index.html
	
index-ref.adoc: index.adoc
	asciidoc-bib -b cell-diffusion.bib -s "american-physics-society" index.adoc
	