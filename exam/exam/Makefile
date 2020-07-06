CCBIN=/usr/bin/gcc
CC=$(CCBIN) -Wall -Wextra -Werror -std=c99 -pedantic -g 
CCD=$(CCBIN) -Wall -Wextra -Werror -std=c99 -pedantic -g -DDEBUG
C_LIBS=lib/xalloc.c lib/ht.c lib/stacks.c lib/queues.c lib/boardutil.c lib/heaps.c

default: lightsout lightsout-d

loplayer: $(C_LIBS) lib/*.h loplayer.c 
	$(CC) -O3 -o loplayer $(C_LIBS) loplayer.c

lightsout: $(C_LIBS) lib/*.h bitarray.c ba-ht.c lightsout.c 
	$(CC) -O3 -o lightsout $(C_LIBS) bitarray.c ba-ht.c lightsout.c

lightsout-d: $(C_LIBS) lib/*.h bitarray.c ba-ht.c lightsout.c 
	$(CCD) -o lightsout-d $(C_LIBS) bitarray.c ba-ht.c lightsout.c

.PHONY: clean
clean:
	rm -Rf *.o lib/*.o loplayer lightsout lightsout-d *.dSYM
