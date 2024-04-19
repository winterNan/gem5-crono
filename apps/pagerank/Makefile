
TRGS = pagerank pagerank_lock

LIBS += -lpthread -lrt -lm -lm5 -I/home/yuan/Capcom/capcom-gem5 -I/home/yuan/Capcom/capcom-gem5/include -L/home/yuan/Capcom/capcom-gem5/util/m5/build/x86/out

CXXFLAGS = -g -pg -static --std=c++0x -O3
CXXFLAGS += -Wall -Werror

all: $(TRGS)

pagerank: pagerank.cc
pagerank_lock: pagerank_lock.cc

clean:
	rm -f $(TRGS) *.o *.dot
	rm -f file.txt

%: %.cc ;
	$(CXX) $(CXXFLAGS) $< -o $@ $(LIBS)
