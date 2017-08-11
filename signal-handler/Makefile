.PHONY: module
CNAME = signal-handler
CTYPE = .c
CFLAGS += -lpthread -std=gnu99 -fpie -rdynamic
FLAGS += -D__TRACE__  -D__DEBUG__ -D__PURE_BODY__
UTIL = util.h httpdef.h

module: $(CNAME)

$(CNAME): $(CNAME)$(CTYPE) $(UTIL)
	${CC} -pie -o $(CNAME) $(CNAME)$(CTYPE) $(FLAGS) $(CFLAGS)

clean:
	rm -rf $(CNAME)
run:
	./$(CNAME) 11111
