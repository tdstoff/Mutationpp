FC=gfortran							# Fortran compiler
FFLAGS=-O3 -Wall -Wextra -std=f2008 # Optimization (for level 3) flags, compiler warnings and the strictest adherence to the latest standards
LIB=../../../install/lib -lmutation++ -lmutation++_fortran
INCLUDE=../../../install/include/mutation++
SRC=wrapper_test.f90
#
FLAGS=$(FFLAGS)
FLAGS+=-L$(LIB)
FLAGS+=-I$(INCLUDE)
#
%.f90:
	$(FC) $(SRC) $(FLAGS) -o ${SRC:.f90=.x}
#
main: %.f90
#
clean: #cleans all the old compilation files
	@rm -f *.mod *.x
