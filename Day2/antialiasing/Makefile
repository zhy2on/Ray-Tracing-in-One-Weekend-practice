SRCS = main.cpp
OBJS = $(SRCS:.cpp=.o)

CXX = g++
CXXFLAGS = -std=c++11 
LIBFLAGS = -lSDL2
INCFLAGS = -I$(INC_DIR)

NAME = a.out

INC_DIR = ../../incs/

all: $(NAME)

$(NAME): $(OBJS)
	$(CXX) $(CXXFLAGS) $(OBJS) -o $@ $(INCFLAGS) $(LIBFLAGS)

$(OBJ_DIR)%.o : $(SRC_DIR)%.cpp $(INC_DIR)*.h
	@mkdir -p $(dir $@)
	$(CXX) $(CXXFLAGS) -c $< -o $@ $(INCFLAGS)

clean:
	rm -rf $(OBJS)

fclean: clean
	rm -rf $(NAME)

re: fclean all

.PHONY: all clean fclean re