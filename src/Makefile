CC = g++

all: bmcontrol

%.o: %.c
	$(CC) $(CFLAGS) $(EXTRA_CFLAGS) -c -I. -I/usr/include -lusb -o $@ $^


bmcontrol: main.o
	$(CC) -I/usr/include -L/usr/lib -lusb -o $@ $^


clean: 
	rm -f *.o bmcontrol