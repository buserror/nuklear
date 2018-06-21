# Install
BIN = mishell

# Flags
CFLAGS += -Wall -std=c99 -Og -g
CFLAGS += -Wno-unused-function -Wno-unused-but-set-variable

LDFLAGS += -lX11 -lm

CFLAGS += ${shell pkg-config --cflags xft}
LDFLAGS += ${shell pkg-config --libs xft}

SRC = ${wildcard *.c}
OBJ = $(SRC:.c=.o)

$(BIN):
	@mkdir -p bin
	rm -f bin/$(BIN) $(OBJS)
	$(CC) $(SRC) $(CFLAGS) -D_POSIX_C_SOURCE=200809L -o bin/$(BIN) -lX11 ${LDFLAGS}
