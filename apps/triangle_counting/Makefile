
TRGS = triangle_counting_lock triangle_counting_atomic sorted_neighbors_tri_lock 

LIBS += -lpthread -lrt -lm -lm5

CXXFLAGS = -g -pg -static --std=c++0x -O3 -I/home/yuan/Capcom/capcom-gem5 -I/home/yuan/Capcom/capcom-gem5/include -L/home/yuan/Capcom/capcom-gem5/util/m5/build/x86/out

CXXFLAGS += #-Wall -Werror

all: $(TRGS)

triangle_counting_lock: triangle_counting_lock.cc
triangle_counting_atomic: triangle_counting_atomic.cc
sorted_neighbors_tri_lock: sorted_neighbors_tri_lock.cc

clean:
	rm -f $(TRGS) *.o *.dot

%: %.cc ;
	$(CXX) $(CXXFLAGS) $< -o $@ $(LIBS)
