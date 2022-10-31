CC = g++
TARGET = squareT
PATH_SRC = ./src/
PATH_OBJ = ./obj/
SRC = $(wildcard $(PATH_SRC)*.cpp)
$(info $(SRC))
OBJ = $(patsubst $(PATH_SRC)%.cpp, $(PATH_OBJ)%.o, $(SRC))
$(info $(OBJ))


all:$(TARGET)

$(PATH_OBJ)%.o:$(PATH_SRC)%.cpp
	 $(CC) -c $< -o $@

$(TARGET):$(OBJ)
	 $(CC) $(OBJ) -o $(TARGET)

clean:
	rm -rf *.o $(TARGET)
install:
	install ./$(TARGET) /usr/bin
uninstall:
	rm -r /usr/bin/$(TARGET)
