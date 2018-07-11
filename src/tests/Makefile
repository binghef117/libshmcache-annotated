.SUFFIXES: .c .o

COMPILE = $(CC) -g -O1 -Wall -D_FILE_OFFSET_BITS=64 -g -DDEBUG_FLAG
INC_PATH = -I../../depend -I..   #-I/usr/include/fastcommon -I/usr/include/shmcache
LIB_PATH = ../libshmcache.a ../../depend/libfastcommon.a -lpthread -ldl -lm # -lshmcache

ALL_PRGS = tests

all: $(ALL_PRGS)
.c:
	$(COMPILE) -o $@ $< $(LIB_PATH) $(INC_PATH)
.c.o:
	$(COMPILE) -c -o $@ $<  $(INC_PATH)
clean:
	rm -f $(ALL_PRGS)

