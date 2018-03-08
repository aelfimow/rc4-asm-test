CXXFLAGS  = -O2 -m64
CXXFLAGS += -I${RC4_ASM_PATH}

RC4FUNC_OBJ = ${RC4_ASM_PATH}/rc4func.o

WARNINGS  = -Wall
WARNINGS += -Wextra
WARNINGS += -pedantic
WARNINGS += -Weffc++
WARNINGS += -std=c++17

all: compile link run
	@echo No errors

compile:
	g++ -c Golden_rc4.cpp -o Golden_rc4.o ${CXXFLAGS} ${WARNINGS}
	g++ -c Test_rc4.cpp -o Test_rc4.o ${CXXFLAGS} ${WARNINGS}
	g++ -c main.cpp -o main.o ${CXXFLAGS} ${WARNINGS}

link:
	g++ Golden_rc4.o Test_rc4.o main.o ${RC4FUNC_OBJ} -o rc4test.exe ${CXXFLAGS} ${WARNINGS}

run:
	./rc4test.exe
