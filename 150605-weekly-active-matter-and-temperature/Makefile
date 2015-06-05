all: index2.html index.html

index.html: index.adoc
	asciidoctor -T ~/code/ascreveal/templates/slim index.adoc -o index.html

index2.html: index.adoc
	asciidoctor index.adoc -o index2.html
	
clean:
	rm -f index{,2}.html index-ref.adoc
