
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile
	$(MAKE) -f objs/Makefile manpage

install:
	$(MAKE) -f objs/Makefile install

upgrade:
	/home/pc/ngxinx_install//sbin/nginx -t

	kill -USR2 `cat /home/pc/ngxinx_install//logs/nginx.pid`
	sleep 1
	test -f /home/pc/ngxinx_install//logs/nginx.pid.oldbin

	kill -QUIT `cat /home/pc/ngxinx_install//logs/nginx.pid.oldbin`
