
CSE331
Homework4
programming problem 5
03/05/2015

- All functions are included in one file, main.cpp.
  NOTES: I am using a dictionary to save a node with 
         its parent. Output 2&3 will be ordered based
 	 based on ASCII value not the flow of the graph.
         They may seem printed wrong, however, the value     
         of the distance and parent are correct to each  
         corresponding node.

- A makefile is provided to ease compiling the program

- Type “make” or “make BFS” to compile this program.
  you could also type “g++ -std=c++11 main.cpp” to compile it

- To run, type “BFS” followed by input file and starting node
  if you used first method, you could run it by typing “a.out” followed by in-file and node

- Type “make clean” to remove the compiled files
  if you used g++, type “rm -rf a.out”

*************************Sample output***************************************

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 1
starting node: 1
Number of Nodes: 6

BFS
D = 1 2 3 4 5 6
1.p=nil, 2.p=1, 3.p=1, 4.p=2, 5.p=3, 6.p=4,
1.d=0, 2.d=1, 3.d=1, 4.d=2, 5.d=2, 6.d=3,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 6
starting node: 6
Number of Nodes: 6

BFS
D = 6
6.p=nil,
6.d=0,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 5
starting node: 5
Number of Nodes: 6

BFS
D = 5 6
5.p=nil, 6.p=5,
5.d=0, 6.d=1,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 4
starting node: 4
Number of Nodes: 6

BFS
D = 4 6
4.p=nil, 6.p=4,
4.d=0, 6.d=1,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 3
starting node: 3
Number of Nodes: 6

BFS
D = 3 5 6
3.p=nil, 5.p=3, 6.p=5,
3.d=0, 5.d=1, 6.d=2,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 2
starting node: 2
Number of Nodes: 6

BFS
D = 2 4 6
2.p=nil, 4.p=2, 6.p=4,
2.d=0, 4.d=1, 6.d=2,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test1 1
starting node: 1
Number of Nodes: 6

BFS
D = 1 2 3 4 5 6
1.p=nil, 2.p=1, 3.p=1, 4.p=2, 5.p=3, 6.p=4,
1.d=0, 2.d=1, 3.d=1, 4.d=2, 5.d=2, 6.d=3,

Yousefs-MacBook-Pro:project4 Gtat$ make
make: `out' is up to date.
Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test3 1
starting node: 1
Number of Nodes: 5

BFS
D = 1 2 3 4 5
1.p=nil, 2.p=1, 3.p=1, 4.p=2, 5.p=2,
1.d=0, 2.d=1, 3.d=1, 4.d=2, 5.d=2,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test3 2
starting node: 2
Number of Nodes: 5

BFS
D = 2 4 5 3
2.p=nil, 3.p=4, 4.p=2, 5.p=2,
2.d=0, 3.d=2, 4.d=1, 5.d=1,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test3 3
starting node: 3
Number of Nodes: 5

BFS
D = 3
3.p=nil,
3.d=0,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test3 4
starting node: 4
Number of Nodes: 5

BFS
D = 4 3 5
3.p=4, 4.p=nil, 5.p=4,
3.d=1, 4.d=0, 5.d=1,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test3 5
starting node: 5
Number of Nodes: 5

BFS
D = 5
5.p=nil,
5.d=0,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 1
starting node: 1
Number of Nodes: 7

BFS
D = 1 2 3 4 5 6
1.p=nil, 2.p=1, 3.p=1, 4.p=2, 5.p=3, 6.p=5,
1.d=0, 2.d=1, 3.d=1, 4.d=2, 5.d=2, 6.d=3,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 2
starting node: 2
Number of Nodes: 7

BFS
D = 2 4 3 5 6
2.p=nil, 3.p=4, 4.p=2, 5.p=4, 6.p=5,
2.d=0, 3.d=2, 4.d=1, 5.d=2, 6.d=3,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 3
starting node: 3
Number of Nodes: 7

BFS
D = 3 2 5 4 6
2.p=3, 3.p=nil, 4.p=2, 5.p=3, 6.p=5,
2.d=1, 3.d=0, 4.d=2, 5.d=1, 6.d=2,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 4
starting node: 4
Number of Nodes: 7

BFS
D = 4 3 5 2 6
2.p=3, 3.p=4, 4.p=nil, 5.p=4, 6.p=5,
2.d=2, 3.d=1, 4.d=0, 5.d=1, 6.d=2,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 6
starting node: 6
Number of Nodes: 7

BFS
D = 6
6.p=nil,
6.d=0,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 5
starting node: 5
Number of Nodes: 7

BFS
D = 5 6
5.p=nil, 6.p=5,
5.d=0, 6.d=1,

Yousefs-MacBook-Pro:project4 Gtat$ ./BFS test4 7
starting node: 7
Number of Nodes: 7

BFS
D = 7 2 4 3 5 6
2.p=7, 3.p=4, 4.p=7, 5.p=4, 6.p=5, 7.p=nil,
2.d=1, 3.d=2, 4.d=1, 5.d=2, 6.d=3, 7.d=0,
