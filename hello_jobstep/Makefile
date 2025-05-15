#On Kestrel GPU:
#module load craype-x86-milan
#module load cuda

COMP   = CC
CFLAGS = -std=c++11
INCLUDES  = -I${CUDA_HOME}/include
LIBRARIES = -L${CUDA_HOME}/lib64 -lcudart

hello_jobstep: hello_jobstep.o
	${COMP} ${LFLAGS} ${LIBRARIES} hello_jobstep.o -o hello_jobstep

hello_jobstep.o: hello_jobstep.cpp
	${COMP} ${CFLAGS} ${INCLUDES} -c hello_jobstep.cpp

.PHONY: clean

clean:
	rm -f hello_jobstep *.o
