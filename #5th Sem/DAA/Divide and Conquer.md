Conquer: Force the sub problem to get solved recursively (COMBINE)
Binary Search is partial DAC, because it does not COMBINE

T(n) = if N is small    1/C/K 
	`if N is large a*T(n/b)+F1(n)F2(n)`
a=> no. of sub problems
b => size of subproblem
F1 => time to divide
F2 => time to conquer