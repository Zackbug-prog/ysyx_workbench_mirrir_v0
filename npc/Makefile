VERILATOR= verilator
TOP_MODULE = top

.PHONY:sim

all:
	@echo "Write this Makefile by your self."

sim:
	$(call git_commit, "sim RTL") # DO NOT REMOVE THIS LINE!!!
	@echo "Write this Makefile by your self."
	$(VERILATOR) --cc --exe --build -j 0 -Wall \
		--trace-fst \
		--top-module $(TOP_MODULE) \
		top.v sim.cpp
	./obj_dir/V$(TOP_MODULE)
	gtkwave wave.fst

include ../Makefile
