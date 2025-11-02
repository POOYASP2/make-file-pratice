CC := gcc

TARGET := app

SRCS := $(wildcard *.c)

all: $(TARGET)

$(TARGET): $(SRCS)
	$(CC) $^ -o $@ 
run:
	./$(TARGET)

clean:
	rm -f $(TARGET)
.PHONY: all clean run
