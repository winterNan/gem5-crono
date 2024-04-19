
TRGS = bc bc_non_partitioned

LIBS += -lpthread -lrt -lm -lm5 -I/home/yuan/Capcom/capcom-gem5 -I/home/yuan/Capcom/capcom-gem5/include -L/home/yuan/Capcom/capcom-gem5/util/m5/build/x86/out

##BOOST_PATH = /run/pkg/boost-/1.53.0-gcc_4.7.3

##BOOST_FLAGS = -I$(BOOST_PATH)/include -L$(BOOST_PATH)/lib -lboost_graph

CXXFLAGS = -g -pg -static --std=c++0x -O3
CXXFLAGS += -Wall -Werror

all: $(TRGS)

bc: bc.cc
bc_non_partitioned: bc_non_partitioned.cc

##boost_dijk_real: boost_dijk_real.cc

clean:
	rm -f $(TRGS) *.o *.dot

%: %.cc ;
	$(CXX) $(CXXFLAGS) $< -o $@ $(LIBS)
