# Iterative

T(n)=t(n-1)+n
T(n) = T(n-3)+T(n-2)...n
T(n) = T(n-k)+2+3..(n-1)+n
for k = n
T(n) = 1+2+3..+n
sum of first n natural numbers
T(n) = n(n+1)/2


T(n) = (n-1)+1

T(n) = T(n-1)+1
T(n)=T(n-2)+1+1
T(n)=T(n-3)+1+1+1
T(n)=T(n-k)+...+1
assuming  n=k
`T(n) = 1*n`


T(n) = 2T(n/2) + n
T(n) = 2* (2T(n/4) + n)  + n
`T(n) = 2*2* (2T(n/8)+n) +n+n`
`t(n) = 2^k (T(n/2^k)) + kn)
for 2^k=n
`t(n) = 2^k*t(1) +kn`
taking 2^k = n and k=logn
`t(n) = n+nlog(n)`


## Masters Theorem
`T(n) = a*T(n/b)+F(n)`

Find N^(logB(A))
Compare F(n) AND N^(logB(A))
Greater is answer, otherwise
F(n)log(n)

For something like 
T(n) = T(root(N))+C
Assume n=2^k
now T(2^k) = T(2^(k/2))+c
Let T(2^k)= S(K)
S(K)=S(K/2)+C

log(k) but since we know n=2^k
then complexity is log2log2(n)