CC = g++
# CFLAGS = -g -std=c++17 -lpthread -ljemalloc
CFLAGS = -g -std=c++17 -lpthread
# CFLAGS = -g -std=c++17 -lpthread -L`jemalloc-config --libdir` -Wl,-rpath,`jemalloc-config --libdir` -ljemalloc `jemalloc-config --libs`
# LD_PRELOAD="/lib64/libjemalloc.so"
run: test
	./test

test: bench_lfss.cc lock_free_skip_set.h skipset.h skipset.cc vectskipset.h vectskipset.cc
	$(CC) $(CFLAGS) bench_lfss.cc skipset.cc vectskipset.cc -o test

# lockfree: lock_free_skip_set.cc 



# .SUFFIXES: .cpp .c
# .cpp.o:
# 	$(CC) $(CFLAGS) -c $<
# .c.o:
# 	$(CC) $(CFLAGS) -c $<

clean:
	@rm -f test
