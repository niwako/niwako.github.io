all: index.html

clean:
	rm -f index.html

index.html: pipes.ipynb
	jupyter nbconvert pipes.ipynb --to slides
	mv pipes.slides.html index.html

watch:
	@fswatch -o . | xargs -n1 -I{} make