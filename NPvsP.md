### Solvable Problem VS Unsolvable Problem

***

1. Solvable:
It has been proved that the
problem has an algorithm
that solves it. The algorithm
may be polynomial or
exponential 

2. Unsolvable:
It has been proved that it is
impossible to develop an
algorithm even in the future.

### Tractable VS Intractable 

Tractable:
Among the existing
algorithms of this
problem type, at least
one of them has
polynomial time
algorithm O(n^k) and
they are in class P

Intractable:
It is proved that the time
complexity all
algorithms (both past
and future) is greater
than polynomial
time(neither P nor NP) 

p: : Class P is the set of all decision
problems that can be solved by deterministic
polynomial time algorithms

NP:  Class NP is the set of all decision
problems that can be solved by polynomial-time
non-deterministic algorithm.

To show P ≠ NP, find one problem in NP that is
not in P
▪To show P = NP, find polynomial-time algorithm
for each problem in NP

NP-HARD
적어도 NP문제 보다는 어려우며, “모든” NP 문제를 다항 시간 내에 어떤 문제 A로 환원(reduction)할 수 있다면, 그 A 문제를 NP-난해(NP-hard) 문제라고 한다.

NP와 NP-HARD에 동시에 포함되면 NP-complete

NP-easy
In complexity theory, the complexity class NP-easy is the set of function problems that are solvable in polynomial time by a deterministic Turing machine with an oracle for some decision problem in NP.

