-Short-term storage devices that use a clock timing system.

## Set Reset Flip Flop

![[Pasted image 20230817102826.png]]

Characteristic Table

| S   | R   | CurrState | NextState |
| --- | --- |:---------:| ---------:|
| 0   | 0   |     0     |         0 |
| 0   | 0   |     1     |         1 |
| 0   | 1   |     0     |         0 |
| 0   | 1   |     1     |         0 |
| 1   | 0   |     0     |         1 |
| 1   | 0   |     1     |         1 |
| 1   | 1   |     0     |         X |
| 1   | 1   |     1     |         X |

Excitation Table

| Current | Next |  S  | R   |
| ------- | ---- |:---:| --- |
| 0       | 0    |  0  | X   |
| 0       | 1    |  1  | 0   |
|1         |  0    |   0  |1     |
| 1       | 1    |  X  | 0   |

S and R define the value that you want the flip flop to hold, and C defines if the flip flop is allowed to shift or not, it can only be altered while C is active

S -> Set
C -> Clock
R -> Reset



## Delay Flip Flop

![[Pasted image 20230817103535.png]]

Subset of the SR flip flop, where R = ~S, this makes it so that there is no prohibited condition, but also that there is no "Don't change" condition. Alternatively, the don't change condition can be achieved by disabling the clock, or arranging a feedback.
Mostly used to implement a slight delay in your circuit.

## JK Flip Flop

![[Pasted image 20230817104012.png]]

Subset of SR flip flop, which converts the prohibited 1,1 condition to their complement, forwarding all (1,1) -> (0,0), which is no change

J  -> S -> Switch
K -> R -> Reset
C -> Clock

## Toggling Flip Flop

![[Pasted image 20230817104314.png]]

Subset of JK flip flop, where J and K are combined to a single input, where K is compliment of J.
Thus, if T is 0, no change, if T is 1, then the flip flop is reversed.

T -> 
	J -> S && K -> R


![[Pasted image 20230821175320.png]]
[[Truth Table]] -> [[Characteristic Table]] -> [[Excitation Table]]
	Characteristic is a truth table of two inputs J,K, and then the previous state, and next state
Excitation table is the inverse of the same, for all prev and next states, it displays what are the required inputs
Registers:
	Holds values, larger than 1 bit. The basic building block of RAM
	