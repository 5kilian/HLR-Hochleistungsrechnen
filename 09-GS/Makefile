# Common definitions
CC = mpicc

# Compiler flags, paths and libraries
CFLAGS = -std=c11 -pedantic -Wall -Wextra -Ofast
LFLAGS = $(CFLAGS)
LIBS   = -lm

OBJS = partdiff-par.o askparams.o 

# Rule to create *.o from *.c
.c.o:
	$(CC) -c $(CFLAGS) $*.c

# Targets ...
all: partdiff-par

partdiff-par: $(OBJS) Makefile
	$(CC) $(LFLAGS) -o $@ $(OBJS) $(LIBS)

clean:
	$(RM) *.o *~

partdiff-par.o: partdiff-par.c Makefile

askparams.o: askparams.c Makefile
