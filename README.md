# Shortest-distance-Dijkstra

Find the shortest path between two nodes in a weighted graph based on Dijkstra algorithm

test case


            B    1     D   6
       5  .-+---------.'-------F
       .-'  |       .' |
    A.'     |2    .'   |
      `.    |   .'4    |3
       1`-. | .'       |
           `.'---------+
            C     8    E

current node: A
PriorityQueue: [(C,A,1), (B,A,5)]
Parents: {A=null}

Visited: [A]

current node: C
PriorityQueue: [(A,C,2), (B,A,5), (B,C,3), (D,C,5), (E,C,9)]
Parents: {A=null, C=A}
Visited: [A, C]

current node: B
PriorityQueue: [(D,B,4), (B,A,5), (D,C,5), (A,B,8), (C,B,5), (E,C,9)]
Parents: {A=null, B=C, C=A}

Visited: [A, B, C]

current node: D
PriorityQueue: [(B,A,5), (C,B,5), (D,C,5), (E,D,7), (E,C,9), (B,D,5), (C,D,8), (A,B,8), (F,D,10)]
Parents: {A=null, B=C, C=A, D=B}

Visited: [A, B, C, D]

current node: E
PriorityQueue: [(A,B,8), (E,C,9), (C,D,8), (F,D,10), (C,E,15), (D,E,10)]
Parents: {A=null, B=C, C=A, D=B, E=D}

Visited: [A, B, C, D, E]
# shortest path between A and F: [A, C, B, D, F]





current node: D
PriorityQueue: [(B,D,1), (C,D,4), (E,D,3), (F,D,6)]
Parents: {D=null}
Visited: [D]

current node: B
PriorityQueue: [(D,B,2), (C,B,3), (E,D,3), (A,B,6), (C,D,4), (F,D,6)]
Parents: {B=D, D=null}
Visited: [B, D]

current node: C
PriorityQueue: [(E,D,3), (C,D,4), (B,C,5), (A,B,6), (A,C,4), (F,D,6), (D,C,7), (E,C,11)]
Parents: {B=D, C=B, D=null}
Visited: [B, C, D]

current node: E
PriorityQueue: [(C,D,4), (A,C,4), (B,C,5), (A,B,6), (E,C,11), (F,D,6), (D,C,7), (C,E,11), (D,E,6)]
Parents: {B=D, C=B, D=null, E=D}
Visited: [B, C, D, E]
# shortest path between C and F: [C, B, D, F]




current node: C
PriorityQueue: [(A,C,1), (B,C,2), (D,C,4), (E,C,8)]
Parents: {C=null}
Visited: [C]

current node: A
PriorityQueue: [(B,C,2), (C,A,2), (D,C,4), (E,C,8), (B,A,6)]
Parents: {A=C, C=null}
Visited: [A, C]

current node: B
PriorityQueue: [(C,A,2), (B,A,6), (D,B,3), (E,C,8), (A,B,7), (C,B,4), (D,C,4)]
Parents: {A=C, B=C, C=null}
Visited: [A, B, C]

current node: D
PriorityQueue: [(C,B,4), (B,A,6), (D,C,4), (E,D,6), (A,B,7), (B,D,4), (C,D,7), (E,C,8), (F,D,9)]
Parents: {A=C, B=C, C=null, D=B}
Visited: [A, B, C, D]

current node: E
PriorityQueue: [(A,B,7), (E,C,8), (C,D,7), (F,D,9), (C,E,14), (D,E,9)]
Parents: {A=C, B=C, C=null, D=B, E=D}
Visited: [A, B, C, D, E]
# shortest path between D and A: [D, B, C, A]
