# flex
Implementing regular expressions 
Program written in C using flex
# Dalio, Brian A.
# dalioba
# 2020-09-24

PROJS  = hmwk_02
CC     = gcc
CFLAGS = -g -Wall -Wextra -fsanitize=address -fsanitize=leak -static-libasan

all : $(PROJS)

hmwk_02 : hmwk_02.l
	flex hmwk_02.l
	$(CC) $(CFLAGS) -o hmwk_02 lex.yy.c

clean:
	rm -f *.o $(PROJS) lex.yy.[ch] hmwk*.tab.[ch]

