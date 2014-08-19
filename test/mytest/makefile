SRC = ./
CFLAGS = -DHAVE_CONFIG_H -I. -I../../src  -I../../src -I../../src/util \
		 -I../../src/net -I../../src/db -I../../src/exceptions \
         -I/usr/include/mysql -Wno-address -Wno-pointer-sign -g -O2 -Wall \
		 -Wunused -Wno-unused-label -funsigned-char -std=gnu99
LDFLAGS = -L/usr/lib/i386-linux-gnu -lmysqlclient -lpthread -lz -lm -lrt -ldl \
		  -lzdb

BIN_PROGRAM = myselect

all: $(BIN_PROGRAM)

clean:
	test -z "$(BIN_PROGRAM)" || rm -f $(BIN_PROGRAM)
	rm -f *.o core

$(BIN_PROGRAM): myselect.c
	gcc $(CFLAGS) -o $@ $^ $(LDFLAGS)

.PHONY: all clean