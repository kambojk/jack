CC = ~/Downloads/cross/x86_64-elf-4.9.1-Linux-x86_64/bin/x86_64-elf-gcc
GCC = gcc
AR = ar rcs

CCFLAGS = -Wall -c -g -ffreestanding -nostdlib -I../../libc/include -I../include

SRCFILES = kb.c

LIB = driver.a
OBJS = $(SRCFILES:.c=.o)

all : $(LIB)

$(LIB) : $(OBJS)
	$(AR) $(LIB) $(OBJS)

$(OBJS) :
	$(CC) $(SRCFILES) $(CCFLAGS)

.PHONY: clean
clean:
	rm -f *.o
	rm -f *.a