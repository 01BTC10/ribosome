CHECKS := $(wildcard *.check)
PORTS  := node

all: $(PORTS)

$(PORTS): %: %-premsg $(CHECKS:%.check=%-%) %-postmsg

%-premsg:
	@echo "Running $* tests."

%-postmsg:
	@echo

%-node:
	@./runtest.sh node js $*

clean:
	rm -f *.out *.log
