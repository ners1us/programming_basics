OUT = a.out
OBJDIR = obj
SRC = main.c argparse.c gof.c
OBJS = $(patsubst %,${OBJDIR}/%,${SRC:.c=.o})
CFLAGS = `sdl2-config --libs --cflags` -Wall -lSDL2_image -lSDL2main -DSDL -lSDL2

all: build ${OBJS}

$(OBJS): obj/%.o: %.c
	${CC} -c ${CFLAGS} $< -o $@

build: ${OBJS}
	${CC} ${CFLAGS} ${OBJS} -o ${OUT}

debug: ${OBJS}
	${CC} ${CFLAGS} -g -DDEBUG ${SRC}
