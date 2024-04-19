
TRGS = tsp

LIBS += -lpthread -lrt -lm -lm5

CXXFLAGS = -g -pg -static --std=c++0x -O3
CXXFLAGS += -I/home/yuan/Capcom/capcom-gem5 -I/home/yuan/Capcom/capcom-gem5/include -L/home/yuan/Capcom/capcom-gem5/util/m5/build/x86/out

all: $(TRGS)

tsp: tsp.cc

clean:
	rm -f $(TRGS) *.o *.dot

%: %.cc ;
	$(CXX) $(CXXFLAGS) $< -o $@ $(LIBS)
