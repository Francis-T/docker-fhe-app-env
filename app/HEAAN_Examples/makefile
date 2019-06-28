# This sample should be run after make libHEAAN.a file in lib folder

# All Target
all: clean HEAAN run

# Tool invocations
HEAAN:
	@echo 'Building target: $@'
	@echo 'Invoking: GCC C++ Linker'
	g++ run.cpp -o "HEAAN" -L/usr/local/lib -lHEAAN -lgmp -lntl -lm -O2 -std=c++11
	@echo 'Finished building target: $@'
	@echo ' '

# Other Targets
clean:
	rm -rf HEAAN

run:
	./HEAAN
