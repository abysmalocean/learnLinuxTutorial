### Begin of the lecture
topic using GNU compiler collection tool and demonstrate the procedure to compile and build an application of c source and 
two chian

 #### gcc -v : 
try one code 
- gcc -E code.c -o first
- gcc -E -v code.c -o fist.i

>>> gcc -E -v echoclient.c -o fist.i
Using built-in specs.
COLLECT_GCC=gcc
Target: x86_64-linux-gnu
Configured with: ../src/configure -v --with-pkgversion='Ubuntu 4.9.4-2ubuntu1' --with-bugurl=file:///usr/share/doc/gcc-4.9/README.Bugs --enable-languages=c,c++,java,go,d,fortran,objc,obj-c++ --prefix=/usr --program-suffix=-4.9 --enable-shared --enable-linker-build-id --libexecdir=/usr/lib --without-included-gettext --enable-threads=posix --with-gxx-include-dir=/usr/include/c++/4.9 --libdir=/usr/lib --enable-nls --with-sysroot=/ --enable-clocale=gnu --enable-libstdcxx-debug --enable-libstdcxx-time=yes --enable-gnu-unique-object --disable-vtable-verify --enable-plugin --with-system-zlib --disable-browser-plugin --enable-java-awt=gtk --enable-gtk-cairo --with-java-home=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64/jre --enable-java-home --with-jvm-root-dir=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64 --with-jvm-jar-dir=/usr/lib/jvm-exports/java-1.5.0-gcj-4.9-amd64 --with-arch-directory=amd64 --with-ecj-jar=/usr/share/java/eclipse-ecj.jar --enable-objc-gc --enable-multiarch --disable-werror --with-arch-32=i686 --with-abi=m64 --with-multilib-list=m32,m64,mx32 --enable-multilib --with-tune=generic --enable-checking=release --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=x86_64-linux-gnu
Thread model: posix
gcc version 4.9.4 (Ubuntu 4.9.4-2ubuntu1) 
COLLECT_GCC_OPTIONS='-E' '-v' '-o' 'fist.i' '-mtune=generic' '-march=x86-64'
 /usr/lib/gcc/x86_64-linux-gnu/4.9/cc1 -E -quiet -v -imultiarch x86_64-linux-gnu echoclient.c -o fist.i -mtune=generic -march=x86-64 -fstack-protector-strong -Wformat -Wformat-security
ignoring nonexistent directory "/usr/local/include/x86_64-linux-gnu"
ignoring nonexistent directory "/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../../x86_64-linux-gnu/include"
#include "..." search starts here:
#include <...> search starts here:
 /usr/lib/gcc/x86_64-linux-gnu/4.9/include
 /usr/local/include
 /usr/lib/gcc/x86_64-linux-gnu/4.9/include-fixed
 /usr/include/x86_64-linux-gnu
 /usr/include
End of search list.
COMPILER_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/
LIBRARY_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../../lib/:/lib/x86_64-linux-gnu/:/lib/../lib/:/usr/lib/x86_64-linux-gnu/:/usr/lib/../lib/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../:/lib/:/usr/lib/
COLLECT_GCC_OPTIONS='-E' '-v' '-o' 'fist.i' '-mtune=generic' '-march=x86-64'


- gcc -S fisrt.i -o first.s


```
>>> gcc -S -v fist.i -o first.s
Using built-in specs.
COLLECT_GCC=gcc
Target: x86_64-linux-gnu
Configured with: ../src/configure -v --with-pkgversion='Ubuntu 4.9.4-2ubuntu1' --with-bugurl=file:///usr/share/doc/gcc-4.9/README.Bugs --enable-languages=c,c++,java,go,d,fortran,objc,obj-c++ --prefix=/usr --program-suffix=-4.9 --enable-shared --enable-linker-build-id --libexecdir=/usr/lib --without-included-gettext --enable-threads=posix --with-gxx-include-dir=/usr/include/c++/4.9 --libdir=/usr/lib --enable-nls --with-sysroot=/ --enable-clocale=gnu --enable-libstdcxx-debug --enable-libstdcxx-time=yes --enable-gnu-unique-object --disable-vtable-verify --enable-plugin --with-system-zlib --disable-browser-plugin --enable-java-awt=gtk --enable-gtk-cairo --with-java-home=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64/jre --enable-java-home --with-jvm-root-dir=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64 --with-jvm-jar-dir=/usr/lib/jvm-exports/java-1.5.0-gcj-4.9-amd64 --with-arch-directory=amd64 --with-ecj-jar=/usr/share/java/eclipse-ecj.jar --enable-objc-gc --enable-multiarch --disable-werror --with-arch-32=i686 --with-abi=m64 --with-multilib-list=m32,m64,mx32 --enable-multilib --with-tune=generic --enable-checking=release --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=x86_64-linux-gnu
Thread model: posix
gcc version 4.9.4 (Ubuntu 4.9.4-2ubuntu1) 
COLLECT_GCC_OPTIONS='-S' '-v' '-o' 'first.s' '-mtune=generic' '-march=x86-64'
 /usr/lib/gcc/x86_64-linux-gnu/4.9/cc1 -fpreprocessed fist.i -quiet -dumpbase fist.i -mtune=generic -march=x86-64 -auxbase-strip first.s -version -o first.s -fstack-protector-strong -Wformat -Wformat-security
GNU C (Ubuntu 4.9.4-2ubuntu1) version 4.9.4 (x86_64-linux-gnu)
	compiled by GNU C version 4.9.4, GMP version 6.1.1, MPFR version 3.1.4-p2, MPC version 1.0.3
warning: MPFR header version 3.1.4-p2 differs from library version 3.1.5.
GGC heuristics: --param ggc-min-expand=100 --param ggc-min-heapsize=131072
GNU C (Ubuntu 4.9.4-2ubuntu1) version 4.9.4 (x86_64-linux-gnu)
	compiled by GNU C version 4.9.4, GMP version 6.1.1, MPFR version 3.1.4-p2, MPC version 1.0.3
warning: MPFR header version 3.1.4-p2 differs from library version 3.1.5.
GGC heuristics: --param ggc-min-expand=100 --param ggc-min-heapsize=131072
Compiler executable checksum: fd95943d86aba509c0b6c009e8a591e6
COMPILER_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/
LIBRARY_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../../lib/:/lib/x86_64-linux-gnu/:/lib/../lib/:/usr/lib/x86_64-linux-gnu/:/usr/lib/../lib/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../:/lib/:/usr/lib/
COLLECT_GCC_OPTIONS='-S' '-v' '-o' 'first.s' '-mtune=generic' '-march=x86-64'
```

**** what tool used in the compiler. 

*** Next step: 
addmdbiltyu to binary
use linker.
gcc -c first.s -o first.o
Translation to binary files
```
>>> gcc -C -v  first.s -o first.o 
Using built-in specs.
COLLECT_GCC=gcc
COLLECT_LTO_WRAPPER=/usr/lib/gcc/x86_64-linux-gnu/4.9/lto-wrapper
Target: x86_64-linux-gnu
Configured with: ../src/configure -v --with-pkgversion='Ubuntu 4.9.4-2ubuntu1' --with-bugurl=file:///usr/share/doc/gcc-4.9/README.Bugs --enable-languages=c,c++,java,go,d,fortran,objc,obj-c++ --prefix=/usr --program-suffix=-4.9 --enable-shared --enable-linker-build-id --libexecdir=/usr/lib --without-included-gettext --enable-threads=posix --with-gxx-include-dir=/usr/include/c++/4.9 --libdir=/usr/lib --enable-nls --with-sysroot=/ --enable-clocale=gnu --enable-libstdcxx-debug --enable-libstdcxx-time=yes --enable-gnu-unique-object --disable-vtable-verify --enable-plugin --with-system-zlib --disable-browser-plugin --enable-java-awt=gtk --enable-gtk-cairo --with-java-home=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64/jre --enable-java-home --with-jvm-root-dir=/usr/lib/jvm/java-1.5.0-gcj-4.9-amd64 --with-jvm-jar-dir=/usr/lib/jvm-exports/java-1.5.0-gcj-4.9-amd64 --with-arch-directory=amd64 --with-ecj-jar=/usr/share/java/eclipse-ecj.jar --enable-objc-gc --enable-multiarch --disable-werror --with-arch-32=i686 --with-abi=m64 --with-multilib-list=m32,m64,mx32 --enable-multilib --with-tune=generic --enable-checking=release --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=x86_64-linux-gnu
Thread model: posix
gcc version 4.9.4 (Ubuntu 4.9.4-2ubuntu1) 
COLLECT_GCC_OPTIONS='-C' '-v' '-o' 'first.o' '-mtune=generic' '-march=x86-64'
 as -v --64 -o /tmp/cceVAR0X.o first.s
GNU assembler version 2.27 (x86_64-linux-gnu) using BFD version (GNU Binutils for Ubuntu) 2.27
COMPILER_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/
LIBRARY_PATH=/usr/lib/gcc/x86_64-linux-gnu/4.9/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../../lib/:/lib/x86_64-linux-gnu/:/lib/../lib/:/usr/lib/x86_64-linux-gnu/:/usr/lib/../lib/:/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../:/lib/:/usr/lib/
COLLECT_GCC_OPTIONS='-C' '-v' '-o' 'first.o' '-mtune=generic' '-march=x86-64'
 /usr/lib/gcc/x86_64-linux-gnu/4.9/collect2 -plugin /usr/lib/gcc/x86_64-linux-gnu/4.9/liblto_plugin.so -plugin-opt=/usr/lib/gcc/x86_64-linux-gnu/4.9/lto-wrapper -plugin-opt=-fresolution=/tmp/cczW1tyj.res -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s -plugin-opt=-pass-through=-lc -plugin-opt=-pass-through=-lgcc -plugin-opt=-pass-through=-lgcc_s --sysroot=/ --build-id --eh-frame-hdr -m elf_x86_64 --hash-style=gnu --as-needed -dynamic-linker /lib64/ld-linux-x86-64.so.2 -z relro -o first.o /usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/crt1.o /usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/crti.o /usr/lib/gcc/x86_64-linux-gnu/4.9/crtbegin.o -L/usr/lib/gcc/x86_64-linux-gnu/4.9 -L/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu -L/usr/lib/gcc/x86_64-linux-gnu/4.9/../../../../lib -L/lib/x86_64-linux-gnu -L/lib/../lib -L/usr/lib/x86_64-linux-gnu -L/usr/lib/../lib -L/usr/lib/gcc/x86_64-linux-gnu/4.9/../../.. /tmp/cceVAR0X.o -lgcc --as-needed -lgcc_s --no-as-needed -lc -lgcc --as-needed -lgcc_s --no-as-needed /usr/lib/gcc/x86_64-linux-gnu/4.9/crtend.o /usr/lib/gcc/x86_64-linux-gnu/4.9/../../../x86_64-linux-gnu/crtn.o
```
objdemp vaew the binary files 

**** try to understand what why the executable file has a lot of code. 

din the main function execurable. have the address in begin. 

different betown executable binary and moveable binary

we have a lot of function in the executable, run time function. The linke Linker link to runtime code
Relocatable: 
offset addresses addined at compile time
fucntion call instructionss refer to relocated addinged at compil time 
fuctionality cod e

execttable: 
exectable binary carry platform spection load addressed assinged to build time'fucntion calls refer to platf
addr run time code
Functinalluty code + runtime code

why we need run time code: 
functionalluty  can not run, kerenl set of interface function request resources aad system calls 
run time code is make dirct calles tio called layer. 
is os is windows, runtime is windows
this is one of the reasons can not protable. 
_init run program starts start functon. casll start
_start finish the main ca ll _fini
_fini 


applcaition soruce (first.c ) ---cpp---> Preprocessed Source(first.i) ---Compiler ---> Assemble Source -- Assembler --> Relocateable Binary--Linker--> executable

hwo to configure a GNU compiler tool chain. 

what happedn when program loaded. address space , executable whene it loaded. 



