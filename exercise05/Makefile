CC := gcc
CFLAGS := -Wall
LDFLAGS :=
SRCS := $(wildcard *.c)
TARGET := app

all: $(TARGET)

$(TARGET): $(SRCS)
	$(CC) $(CFLAGS) $^ -o $@ $(LDFLAGS)

run:
	./$(TARGET)

clean:
	$(RM) $(TARGET)
.PHONY: clean all run
