default: update build

update:
	@cd .. && make build

build: clean copy pack wildcard usemin rev check

clean:
	@rm -rf dist

copy:
	@mkdir -p dist
	@cp -r src/* dist

usemin:
	@node ../bin/usemin.js dist/*.html

pack:
	@node ../bin/pack.js 'src/**/webspoon.html' -regexp '^src' -replacement 'xxx' > dist/webspoon.html.js

wildcard:
	@node ../bin/wildcard.js 'dist/**/test7.html'

rev:
	@node ../bin/rev.js -base 'dist/test5.html' -base 'dist/dist5.js' -static 'dist/dist5.js'

check:
	@open index.html
