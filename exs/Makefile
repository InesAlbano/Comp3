.SUFFIXES: .$(EXT) .asm
COMP=../diy # compiler
EXT=diy # file extension: .$(EXT)
LIB=diy # runtime library: lib$(LIB).a
RUN=../run # runtime directory
AS=nasm -felf32 # assembler command
LD=ld -melf_i386 # loader command

SRC=hello.diy ack.diy string.diy factorial.diy iter.diy recurs.diy mean.diy rand.diy 
EXE=$(SRC:%.diy=%)

all:: compiler $(EXE)

compiler::
	make -C ..

%:%.$(EXT)
	$(COMP) $<

clean::
	rm -f *.o *.asm *.s *~ $(EXE)
