
TRGS = sssp sssp_outer sssp_outer_atomic

LIBS += -lpthread -lrt -lm -lm5

##BOOST_PATH = /run/pkg/boost-/1.53.0-gcc_4.7.3

##BOOST_FLAGS = -I$(BOOST_PATH)/include -L$(BOOST_PATH)/lib -lboost_graph

CXXFLAGS = -g -pg -static --std=c++0x -O3 -I/home/yuan/Capcom/capcom-gem5 -I/home/yuan/Capcom/capcom-gem5/include -L/home/yuan/Capcom/capcom-gem5/util/m5/build/x86/out

CXXFLAGS += -Wall -Werror

all: $(TRGS)

sssp: sssp.cc
sssp_outer: sssp_outer.cc
sssp_outer_atomic: sssp_outer_atomic.cc

clean:
	rm -f $(TRGS) *.o *.dot

%: %.cc ;
	$(CXX) $(CXXFLAGS) $< -o $@ $(LIBS)
