# Fermat's Little Theorem
###### If p is a prime number and a is a natural number, then
 * a^p=a (mod p). 	
###### Furthermore, if p does not divide a, then there exists some smallest exponent d such that
 * a^d-1=0 (mod p) 	
###### and d divides p-1. Hence,
 * a^(p-1)-1=0 (mod p). 	
###### The theorem is sometimes also simply known as "Fermat's theorem" (Hardy and Wright 1979, p. 63).

# Approve Fermat's Lettle Theorem
费马小定律的证明
　　若n不整除a-b，x>0，(x,n)=1，則n也不整除x(a-b)。取整數A为所有小於p的集（p不整除A），B为A中所有元素乘以a的集合。因任何两个A中的元素差都不能被p整除，所以任何两个B中的元素差也无法被p整除。因此:

　　1 \cdot 2 \cdot 3 \cdot \dots \cdot (p-1) = (1 \cdot a)\cdot(2 \cdot a)\cdot\dots\cdot ((p-1) \cdot a) \pmod{ p},

　　即:

　　W = W\cdot a^{p-1} \pmod{p},

　　在这里W=1·2·3·...·(p-1)。将整个公式除以W即得到:

　　ap − 1 = 1(mod p)
