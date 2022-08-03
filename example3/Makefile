TARGET = prog

$(TARGET): main.o lib1.a lib2.so
	gcc $< lib1.a -o $@ -l2 -L`pwd`

main.o: main.c
	gcc -c $< -o $@

lib1.a: lib1.o
	ar rcs $@ $^

lib2.so: lib2.o
	gcc -shared -o lib2.so lib2.o

lib1.o: lib1.c lib1.h
	gcc -c -o $@ $<

lib2.o: lib2.c lib2.h
	gcc -c -fpic -o $@ $<

clean:
	rm -f *.o *.a *.so $(TARGET)
