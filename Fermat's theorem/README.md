# History
　　皮埃尔·德·费马于1636年发现了这个定理，在一封1640年10月18日的信中他第一次使用了上面的书写方式。在他的信中费马还提出a是一个质数的要求。这个要求实际上不存在。

The hypothesis that an integer n is prime iff it satisfies the condition that 2^n-2 is divisible by n. Dickson (2005, p. 91) stated that Leibniz believe to have proved that this congruence implies that n is prime. In actuality, this condition is necessary but not sufficient for n to be prime since, for example, 2^(341)-2 is divisible by 341, but 341=11·31 is composite.
    与费马无关的有一个中国猜想。这个猜想是中国数学家提出来的。其内容为如果，而且只有当2p = 2(modp)成立时p才是一个质数。

　　假如p是一个质数的话，则2p = 2(modp)成立（这是费马小定理的一个特殊情况）是对的。但反过来，假如2p = 2(modp)成立那么p是一个质数是不成立的（比如341符合上述条件但不是一个质数）。因此整个来说这个猜想是错误的。

　　一般认为中国数学家在费马前2000年的时候就已经认识中国猜测了。但也有人认为实际上中国猜测是1872年提出的，认为它早就为人所知是出于一个误解。
  
# Fermat's Little Theorem
如果n是一个素数，a是小于n的任意正整数，那么a的n次方与a模n同余
###### If p is a prime number and a is a natural number, then
 * a^p=a (mod p). 	
###### Furthermore, if p does not divide a, then there exists some smallest exponent d such that
 * a^d-1=0 (mod p) 	
###### and d divides p-1. Hence,
 * a^(p-1)-1=0 (mod p). 	
###### The theorem is sometimes also simply known as "Fermat's theorem" (Hardy and Wright 1979, p. 63).

# Approve Fermat's Lettle Theorem
## 费马小定律的证明
　　### 若n不整除a-b，x>0，(x,n)=1，則n也不整除x(a-b)。取整數A为所有小於p的集（p不整除A），B为A中所有元素乘以a的集合。因任何两个A中的元素差都不能被p整除，所以任何两个B中的元素差也无法被p整除。因此:

　　1 * 2 * 3 * ... * (p-1) = (1 * a) * (2 * a) * ... * ((p-1) * a) (mod p),

　　即:

　　W = W * a^{p-1} (mod p),

　　在这里W=1·2·3·...·(p-1)。将整个公式除以W即得到:

　　a^(p − 1) = 1(mod p)
  
## MILLER-RABIN检测
Miller-Rabin检测是目前应用比较广泛的一种

二次探测定理:如果p是一个素数,且0<x<p,则方程x^2%p=1的解为:x=1或x=p-1
费马小定理：a^(p-1) ≡ 1(mod p)

这就是Miller-Rabin素性测试的方法。不断地提取指数n-1中的因子2，把n-1表示成d*2^r（其中d是一个奇数）。那么我们需要计算的东西就变成了a的d*2^r次方除以n的余数。于是，a^(d * 2^(r-1))要么等于1，要么等于n-1。如果a^(d * 2^(r-1))等于1，定理继续适用于a^(d * 2^(r-2))，这样不断开方开下去，直到对于某个i满足a^(d * 2^i) mod n = n-1或者最后指数中的2用完了得到的a^d mod n=1或n-1。这样，Fermat小定理加强为如下形式：

尽可能提取因子2，把n-1表示成d*2^r，如果n是一个素数，那么或者a^d mod n=1，或者存在某个i使得a^(d*2^i) mod n=n-1 ( 0<=i<r ) （注意i可以等于0，这就把a^d mod n=n-1的情况统一到后面去了）

定理:若n是素数,a是小于n的正整数,则n对以a为基的Miller测试,结果为真.
Miller测试进行k次,将合数当成素数处理的错误概率最多不会超过4^(-k)

## 费马小定律的的实际应用
　　如上所述，中国猜测只有一半是正确的，符合中国猜测但不是质数的数被称为伪质数。

　　假如所有符合1<b<p的b、p都满足下列条件的话:

　　b^{p} = b \mod p

　　则p必定是一个质数。

　　实际上没有必要测试所有的小于p的自然数，只要测试所有的小于p的质数就可以了。

　　这个算法的缺点是它非常慢，运算率高。
  
  
  # Reference
  * 一个费马小定理的“无字”证明 https://zhuanlan.zhihu.com/p/28450259
  * 二次探测定理:如果p是一个素数,且0<x<p,则方程x^2%p=1的解为:x=1或x=p-1
  * 模运算规则：
    * (a^b) % p = ((a % p)^b) % p
    * (a * b) % p = (a % p * b % p) % p
