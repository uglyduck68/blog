CFLAGS	= -std=c99 -march=core-avx-i -mtune=core-avx-i -O2

http_benchmark: http_hsm.o http_ngx.o http_tbl.o http_goto.o http_benchmark.o
	$(CC) -o $@ $^

%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean : FORCE
	rm -f *.o* *~ http_benchmark

FORCE :

