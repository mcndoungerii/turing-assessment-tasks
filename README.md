# turing-assessment-tasks

## My attemp to solve following two assessment task for turing.com

## Task 1 Prompt

Have you heard of the fibonacci sequence? It is defined by $f_0 = 0, f_1 = 1$ and $f_n=f_{n-1}+ f_{n-2}$ for $n\geq 2$.

This question is about a similar sequence, called gibonacci sequence. It is defined by $g_0 = x, g_1 = y$ and $g_n=g_{n-1}- g_{n-2}$ for $n\geq 2$. Different possible starting values of the gibonacci sequence may lead to different gibonacci sequences.

### Task
You are given three arguments: `n, x, y`. Your task is to find $g_n$ using the above definition of a gibonacci sequence starting with $g_0=x, g_1=y$

Write a function `gibonacci(n, x, y)` that takes in 3 arguments.

### Inputs

It is guaranteed that $n,x,y$ are integers and $0 \leq n,x,y \leq 10^9$.

### Outputs

`gibonacci(n, x, y)` should return $g_n$ given that $g_0=x, g_1=y$.

### Examples

`gibonacci(0, 0, 1) = 0`

`gibonacci(1, 0, 1) = 1`

`gibonacci(2, 0, 1) = 1`

`gibonacci(3, 0, 1) = 0`



## Task 2 Prompt

There are $n$ ($n$ is even) players, conveniently labelled $1, 2, \ldots n$. These players will play $m$ rounds of games. In each round of games, the players are split into two teams of $\frac{n}{2}$ players each. Two players $x < y$ are said to have played against each other if they were on different teams for one of the $m$ games.

### Task
You are given three arguments: `n, m, games`. Your task is to check that for all pairs of players $1 \leq x, y \leq n$, player $x$ has played against $y$. `games` is a 2-dimensional list that represents the $m$ rounds of games among $n$ players.

Write a function `check(n, m, games)` that takes in 3 arguments.

### Inputs

It is guaranteed that $n, m$ are integers and $1 \leq n \leq 20,000$, $1\leq m \leq 30$. It is also guaranteed that $n$ is even.

 `games` is a 2 dimensional list with `m` rows and `n` columns, where `games[i]` is a permutation of `1,2,3,...,n` representing round number $i$. In particular for round `i`, `games[i][0], games[i][1], games[i][n/2-1]` is on one team, `games[i][n/2], games[i][n/2+1], games[i][n-1]` is on the other team.

### Outputs

`check(n, m, games)` should return a boolean, True if and only if all pairs of players have played against each other in the $m$ rounds of games.

### Examples

`check(2, 1, [[1, 2]]) = True`

`check(4, 2, [[1, 2, 3, 4], [4, 3, 1, 2]]) = False`

`check(4, 2, [[1, 2, 3, 4], [1, 3, 2, 4]]) = True`

`check(6, 6, [[1, 6, 3, 4, 5, 2], [6, 4, 2, 3, 1, 5], [4, 2, 1, 5, 6, 3], [4, 5, 1, 6, 2, 3], [3, 2, 5, 1, 6, 4], [2, 3, 6, 4, 1, 5]]) = True`

`check(6, 6, [[3, 1, 4, 5, 6, 2], [5, 3, 2, 4, 1, 6], [5, 3, 6, 4, 2, 1], [6, 5, 3, 2, 1, 4], [5, 4, 1, 2, 6, 3], [4, 1, 6, 2, 5, 3]]) = False`
