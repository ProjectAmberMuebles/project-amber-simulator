
OUTDIR=out
SRCDIR=src
SOURCES=src/main.cpp
INCLUDES=

OBJS = %.o 
CC = g++
DEBUG = -g
CFLAGS = -Wall -c $(DEBUG)
LFLAGS = -Wall -lm $(DEBUG)

all: simulator

clean: 
	@rm -rf $(OUTDIR) *.exe

simulator: clean out/$(OBJS)
	@$(CC) $(LFLAGS) out/$(OBJS) -o simulator.exe

out/$(OBJS): outdirs $(INCLUDES) $(SOURCES)
	@$(CC) $(CFLAGS) $(SOURCES)

$(OUTDIR)/%.o: $(SRCDIR)%.cpp
	@$(CC) $< -o $@

outdirs:
	@mkdir $(OUTDIR)