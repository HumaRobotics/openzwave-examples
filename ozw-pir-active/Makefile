CC=g++

top_srcdir=/usr/local/include/openzwave/

INCLUDES:= -I $(top_srcdir) -I $(top_srcdir)command_classes -I $(top_srcdir)platform -I $(top_srcdir)value_classes
LIBS:= -lopenzwave -pthread -ludev
LDFLAGS += -L/usr/local/lib -Wl,-R/usr/local/lib '-Wl,-R$$ORIGIN',-L/usr/local/lib64 

all:	ozw

ozw: Main.cpp
	$(CC) $(INCLUDES) -c Main.cpp -o ozw-pir-active.o
	$(CC) ozw-pir-active.o -o ozw-pir-active.out  $(LIBS) $(LDFLAGS) 

clean:
	rm -rf *.o *.out
