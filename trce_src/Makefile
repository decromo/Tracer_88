CC=gcc -std=c99 -Wall
TARGET: all
all: t88


88.o: 88.h macro.h 88.c
	$(CC) -c -O 88.c 

88def.o: 88.h 88def.c
	$(CC) -c -O 88def.c

adr.o: 88.h macro.h  adr.c
	$(CC) -c -O adr.c 
 
cond.o: 88.h macro.h cond.c
	$(CC) -c -O cond.c 

main.o: 88.h macro.h main.c
	$(CC) -c -O main.c 
 
doscurs.o: doscurs.c 
	$(CC) -c -O doscurs.c 
 
t88: 88.o adr.o cond.o 88def.o main.o doscurs.o Makefile 
	$(CC) -O0 -o t88 88.o adr.o cond.o 88def.o main.o doscurs.o; \
	cp t88 ../exercises/t88; cp t88 ../examples/t88; cp t88 ../bin/t88
 
.PHONY : clean
clean:
	rm -f *~
	rm -f *.o
	rm -f t88
