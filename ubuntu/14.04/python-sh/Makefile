SHELL := /bin/bash

NAME=sh
VERSION=1.11

.PHONY: all clean prepare package_deb
.SILENT: desc

all: desc

desc:
	echo "usage: please use make package_deb"

clean:
	rm -f python-$(NAME)*.deb

prepare:
	# nothing to do here

package_deb: prepare
	fpm -s python \
	    -t deb \
	    -m "Jochen Breuer <brejoc@gmail.com>" \
	    --license "MIT License" \
	    -v $(VERSION) \
	    --deb-user root \
	    --deb-group root \
	    -d "python2.7" \
            -d "python (>=2.7.1-0ubuntu2)" \
            -d "python (<<2.8)" \
	    $(NAME)
