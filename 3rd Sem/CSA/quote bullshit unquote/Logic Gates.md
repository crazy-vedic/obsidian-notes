Digital components that are used to implement digital logic operations AND, OR, NOT
Used to create Integrated Circuits and digital electronic circuits.

1. AND gate:
| Header 1 | Header 2 | Header 3 |  
| -------- | -------- | -------- |  
| Item 1 | Item 2 | Item 3 |  
| Item 4 | Item 5 | Item 6 |

2. OR gate:
3. NOT gate:

4. Combinations
	1. NAND GATE  `AND followed by NOT`
			A B A.B ~AB
			0 0 0 1
			0 1 0 1
			1 0 0 1
			1 1 1 0
	2. NOR GATE  `OR followed by NOT`
			A B A+B ~(A+B)
			0 0 0 1
			0 1 1 0
			1 0 1 0
			1 1 1 0

	3. EXOR GATE `Only one input is active`
			A B XOR
			0 0 0
			0 1 1
			1 0 1
			1 1 0
	4. XNOR GATE `XOR followed by NOT`
			A B XOR ~XOR
			0 0 0 1
			0 1 1 0 
			1 0 1 0
			1 1 0 1
			
## USING NOR, NAND GATES TO MAKE OTHER GATES
Single input on a NAND gate becomes a NOT gate
OR GATE
![[csa2.jpg]]

AND GATE
![[csa3.jpg]]

OR GATE
![[Pasted image 20230801125439.png]]