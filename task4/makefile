all: myapp
P1o=prog1.o
P2o=prog2.o
P3o=prog3.o
P4o=prog4.o
dro=driver.o
P1c=prog1.c
P2c=prog2.c
P3c=prog3.c
P4c=prog4.c
drc=driver.c
myapp: $(P1o) $(P2o) $(P3o) $(P4o) $(dro)
	gcc $(P1o) $(P2o) $(P3o) $(P4o) $(dro) -o myapp
$(P1o): $(P1c)
	gcc -c $(P1c)
$(P2o):  $(P2c)
	gcc -c $(P2c)
$(P3o): $(P3c)
	gcc -c $(P3c)
$(P4o): $(P4c)
	gcc -c $(P4c)
$(dro): $(drc) header.h
	gcc -c $(drc)
clean:
	rm -f *.o
install: myapp
	@cp myapp /usr/bin
	@chmod a+x /usr/bin/myapp
	@chmod og-w /usr/bin/myapp
	@echo "myapp installed successfully"
uninstall: 
	@rm -f /usr/bin/myapp
	@echo "myapp successfully un-installed"
