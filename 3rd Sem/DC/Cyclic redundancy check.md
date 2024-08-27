Polynomial
X7+X5+X3+X2+X+1
Convert to binary as follows:
X7 X6 X5 X4 X3 X2 X1 X0
1   0    1    0  1   1   1   1
divisor->
X3 + X + 1

X3  X2  X  1
1     0    1   1 

Since divisor bit = 4
CRC bit is divisor bit -1
So Add 3 CRC 000 bits to the initial polynomial

Now perform long division on the polynomial
(1011) divides(10101011*000*)
In place of subtraction at every bitwise, use XOR operation
CRC bit -> 101

Check this by replacing the empty crc bit with the current crc bit, should be fully divisble if correctly done.