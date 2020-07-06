Final Exam

Programming (Lights Out)

Files you won't modify:
   lib/contracts.h     - Contracts for C
   lib/xalloc.{c,h}    - NULL-checking allocation
   lib/boardutil.{c,h} - Useful Lights-Out relevant functions
   lib/ht.{c,h}        - Hash tables
   lib/stacks.{c,h}    - Stacks
   lib/queues.{c,h}    - Queues
   lib/bitarray.h      - Interface to bit arrays
   lib/ba-ht.h         - Interface to bit array hashtables
   Makefile            - Utility for building this project

Files that don't exist yet:
   loplayer.c         - Lights-Out player implementation (needs a main() function)
   bitarray.c          - Bit array implementation
   ba-ht.c             - Bit array hashtable wrapper implementation
   lightsout.c         - Lights out solver implementation (needs a main() function)

==========================================================

Compiling your lights out player
   % make loplayer
   % ./loplayer boards/board0.txt

Compiling and running your lights out solver (with -DDEBUG)
   % make
   % ./lightsout-d boards/board0.txt

Compiling and running your lights out solver (without -DDEBUG)
   % make
   % ./lightsout boards/board0.txt 

Using a Unix pipe to run your lights out player and solver togather(with -DDEBUG)
% ./lightsout-d boards/3x3-5.txt | ./loplayer boards/3x3-5.txt

Using a Unix pipe to run your lights out player and solver togather(without -DDEBUG)
% ./lightsout boards/3x3-5.txt | ./loplayer boards/3x3-5.txt

==========================================================

Creating a tarball to submit by e-mailing to: pic.cs.hust@hotmail.com; 
   % tar -czvf <姓名>-<学号>-exam.tgz lightsout.c ba-ht.c bitarray.c loplayer.c report.doc



