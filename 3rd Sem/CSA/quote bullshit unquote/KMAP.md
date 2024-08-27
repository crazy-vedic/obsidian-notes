Simplified method to solve boolean expressions
minterms (x.y.z) maxterms (x+y+z)

0=~A
1=A


2 variable kmap

|`A\B`|0|1|
|-|-|-|
|0|00|01|
|1|10|11|

3 variable kmap

|`A\BC`|01|01|11|10|
|-|-|-|-|-|
|0|000|001|011|010|
|1|100|101|111|110|

4 variable kmap

|`AB\CD`|00|01|11|10|
|-|-|-|-|-|
|00|0000|0001|0011|0010|
|01|0100|0101|0111|0110|
|11|1100|1101|1111|1110|
|10|1000|1001|1011|1010|


>[!Note]
>Encircle 1s in SOP
>Encircle 0s in POS

Assignment
SOP {SUM OF PRODUCT}
Σ(1,4,5,6,7,10,12,14)

|`AB\CD`|00|01|11|10|
|-|-|-|-|-|
|00|0|1|0|0|
|01|1|1|1|1|
|11|1|0|0|1|
|10|0|0|0|1|

![[Pasted image 20230804105459.jpg]]

POS {PRODUCT OF SUM}
π(0,1,2,6,8,11,12)

|`AB\CD`|00|01|11|10|
|-|-|-|-|-|
|00|1|1|0|1|
|01|0|0|0|1|
|11|1|0|0|0|
|10|1|0|1|0|
![[Pasted image 20230804110237.jpg]]


Don't care conditions exists when for a given minterm value in kmap, the values have a "0" or "1" value.
In this case we don't bother about that what value it may have, we call it as a don't case by using "X"

![[Pasted image 20230807162717.jpg]]

Essentially the X becomes a joker card, which can be combined with a 0, or a 1, depending on whether using SOP or POS.
Solution =>
![[Pasted image 20230807163008.jpg]]

[[KMAPQ1]]


![[WhatsApp Image 2023-08-08 at 12.19.59.jpg]]


c