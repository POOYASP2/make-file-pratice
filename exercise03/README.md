# Exercise 5 — makefile

You are given the following Makefile:

```makefile
CC = gcc
CFLAGS = -Wall -g
TARGET = program
SRC = main.c math_operations.c string_operations.c
OBJ = $(SRC:.c=.o)

all: $(TARGET)

$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) -o $@ $(OBJ)

%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

clean:
	rm -f $(OBJ) $(TARGET)

```

Questions:

* What is the purpose of all the rules in this Makefile?
    Generate program binary file from `main.c`, `math_operations.c` and `string_operations.c`

* Explain what the %.o: %.c rule does.
    Set target of a o file for each c file. ( main.o: main.c)

* What does the clean rule do, and when would you use it?
    Here, clean command remove all object files and our final target binary file. We must use this command when we want to clean our directory from previous make command output.
