slides.html: slides.md Makefile
	filepp slides.md | pandoc -t s5 -s -o slides.html

clean:
	rm -f *.html

.PHONY: clean
