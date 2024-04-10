CC = gcc
CFLAGS = -Werror -Wextra -Wall

tests: s21_grep
	sh tests.sh

s21_grep:
	$(CC) $(CFLAGS) grep.c open.c -o s21_grep

clean:
	rm s21_grep


rebuild: clean s21_grep

clang: 
	cp ../../materials/linters/.clang-format ../../src/grep/.clang-format
	clang-format -style=Google -n *.c *.h 
	rm .clang-format