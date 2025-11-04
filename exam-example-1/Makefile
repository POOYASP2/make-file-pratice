CC := gcc
CFLAGS := -Wall -MMD -MP

TARGET := program.elf
SRCS := $(wildcard *.c)
OBJS := $(SRCS:.c=.o)
DEPS := $(OBJS:.o=.d)

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@
clean:
	$(RM) $(TARGET) $(OBJS) $(DEPS)
.PHONY: clean all
-include $(DEPS)
