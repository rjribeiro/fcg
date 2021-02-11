./bin/Linux/main-fan: src/main-fan.cpp src/glad.c include/utils.h
	mkdir -p bin/Linux
	g++ -std=c++11 -Wall -Wno-unused-function -g -I ./include/ -o ./bin/Linux/main-fan src/glad.c src/main-fan.cpp ./lib-linux/libglfw3.a -lrt -lm -ldl -lX11 -lpthread -lXrandr -lXinerama -lXxf86vm -lXcursor

./bin/Linux/main: src/main.cpp src/glad.c include/utils.h
	mkdir -p bin/Linux
	g++ -std=c++11 -Wall -Wno-unused-function -g -I ./include/ -o ./bin/Linux/main src/glad.c src/main.cpp ./lib-linux/libglfw3.a -lrt -lm -ldl -lX11 -lpthread -lXrandr -lXinerama -lXxf86vm -lXcursor

.PHONY: clean run
clean:
	rm -f bin/Linux/main

run: ./bin/Linux/main
	cd bin/Linux && ./main


.PHONY_fan: clean_fan run_fan

clean_fan:
	rm -f bin/Linux/main-fan

run_fan: clean_fan ./bin/Linux/main-fan
	cd bin/Linux && ./main-fan
