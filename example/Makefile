SRCS := $(wildcard *.c)

EXECS := $(SRCS:.c=)

CC ?= gcc

all : $(EXECS)

%: %.c
	$(CC) $< -o $@

clean:
	rm -f $(EXECS)

run: all
	@for exec in $(EXECS); do echo "Running $$exec...";./$$exec; done

.PHONY: all clean run
