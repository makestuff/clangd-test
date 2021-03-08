all: tests-main

tests-main: tests/main.o tests/A.o tests/B.o
	/usr/bin/g++ -o tests-main tests/main.o tests/A.o tests/B.o

tests/main.o: tests/main.cpp
	/usr/bin/g++ -c -Wall -Wextra -std=c++17 -o tests/main.o tests/main.cpp

tests/A.o: tests/A.cpp
	/usr/bin/g++ -c -Wall -Wextra -std=c++17 -isystem /var/tmp/clangd-test/boost-1.75.0/include -o tests/A.o tests/A.cpp

tests/B.o: tests/B.cpp
	/usr/bin/g++ -c -Wall -Wextra -std=c++17 -o tests/B.o tests/B.cpp

clean: FORCE
	rm -rf tests/main.o tests/A.o tests/B.o tests-main .cache

FORCE:
