# Nombre del ejecutable final
PROGRAMA := programa

# Compilador y flags
CC     := gcc
CFLAGS := -Wall


SRCS := main.c operaciones.c

OBJS := $(SRCS:.c=.o)

# Regla principal
all: $(PROGRAMA)

# Regla para linkear los objetos y generar el ejecutable
# TODO 3: Completá el comando de linkeo
#         Usá $(CC), la variable automática $^ (todos los prerequisitos)
#         y el flag -o $(PROGRAMA)
$(PROGRAMA): $(OBJS)
	$(CC) $^ -o $(PROGRAMA)

# TODO 4: Escribí la regla de patrón para compilar cada .c en su .o
#         Formato: %.o : %.c
#         El comando debe usar $(CC) $(CFLAGS), la variable automática
#         $< (el primer prerequisito, es decir el .c) y el flag -c
#         para compilar sin linkear, y -o $@ para nombrar el .o

%.o : %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Regla para limpiar archivos generados
clean:
	rm -f $(PROGRAMA) $(OBJS)

# TODO 5: Declarar los targets que NO son archivos usando .PHONY
#         Agregá: all y clean
.PHONY: all clean