CC = gcc
CFLAGS = -Werror -Wextra -Wall

tests: s21_cat
	sh tests.sh

s21_cat:
	$(CC) $(CFLAGS) cat.c open.c -o s21_cat

clean:
	rm s21_cat


rebuild: clean s21_cat

clang: 
	cp ../../materials/linters/.clang-format ../../src/cat/.clang-format
	clang-format -style=Google -n *.c *.h 
	rm .clang-format