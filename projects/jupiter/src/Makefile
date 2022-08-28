all: jupiter

jupiter: main.c
	gcc -g -O0 -o $@ main.c
clean:
	-rm jupiter

check: all
	./jupiter |grep "Hello from .*jupiter!"
	@echo "*** ALL TESTS PASSED ***"

install:
	# MacOS prefers /usr/local
	cp jupiter /usr/local/bin
# not allowed on MacOS?
#	chown root:root /usr/bin/jupiter
	chmod +x /usr/local/bin/jupiter

.PHONY: all clean check install

