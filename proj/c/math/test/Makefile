PWD = $(shell pwd)

INC_DIRS += -I$(PWD)/../lib

LIBS = -lm

SRCS = $(wildcard *.c)
OBJS = $(SRCS:%.c=%.o)

LIB_DIR = $(PWD)/../lib
LIB_OBJS = $(shell find $(LIB_DIR) -name '*.o')

TARGET = complex_test

all: $(OBJS)
all: $(TARGET)

$(TARGET): $(OBJS)
complex_test: complex_test.o
	$(CC) -o $@ $< $(LIB_OBJS) $(LIBS)

.c.o:
	@echo "**********************************"
	@echo "********** Main Program **********"
	@echo "**********************************"
	$(CC) -c $< -o $@ $(INC_DIRS)

clean:
	rm -rf *.o
	rm -rf $(TARGET)
