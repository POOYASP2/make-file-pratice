CC := gcc

CFLAGS := -Wall -MMD -MP

TARGET := app

SRCS := $(wildcard *.c)
OBJS := $(SRCS:.c=.o)
DEPS := $(OBJS:.o=.d)
all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(CFLAGS) -o $@ $^

%o: %.c
	$(CC) $(CFLAGS) -o $@ -c $<
clean:
	$(RM) $(TARGET) $(OBJS) $(DEPS)


.PHONY: clean all
-include $(DEPS)
