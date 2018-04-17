CXX      = g++
CXXFLAGS = -std=c++11 -pedantic -Wall -D NDEBUG -I libcpp -static-libstdc++
OPT      = -O3
EXE_FLAGS= -s -flto
LIB_FLAGS= -flto -fPIC

all:
	${CXX} ${CXXFLAGS} ${OPT} ${EXE_FLAGS} jigsaw.cpp -o jigsaw64r
	${CXX} ${CXXFLAGS} ${OPT} ${LIB_FLAGS} jigsaw.cpp -shared -o libjigsaw64r.so
	cp jigsaw64r ../bin/LNX-64
	#rm ../bin/temp.txt
	cp libjigsaw64r.so ../lib/LNX-64
	#rm ../lib/LNX-64/temp.txt

clean:
	rm -f jigsaw64r libjigsaw64r.so