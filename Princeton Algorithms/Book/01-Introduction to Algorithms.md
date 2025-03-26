# Introduction to Algorithms

Algorithms are step-by-step procedures for solving problems. They are independent of specific programming languages and can be implemented on various computers.  They are finite, deterministic (always produce the same output for the same input), and effective (guaranteed to solve the problem).  

Data Structures are ways of organizing data to facilitate efficient algorithm execution.  Algorithms and data structures are closely related – the choice of data structure often influences the efficiency of an algorithm.

For large problems, the choice of algorithm significantly impacts speed and resource usage. A well chosen algorithm can make a program millions of times faster.  This efficiency can make the difference between a feasible solution and an impossible one.

> Learning about algorithms provides tools for tackling complex problems by breaking them down into smaller, manageable sub-tasks.

Re-implementing algorithms allows adapting to new computing environments and leveraging their unique features for optimal performance. While libraries provide pre-built implementations, understanding the underlying principles enables better utilization and customization.

## Euclid's Algorithm

>[!Abstract]
>Compute the greatest common divisor of two non-negative integers p and q as follows,  If q is 0, the answer is p. If not, divide p by q and take the remainder r.  The answer is the greatest common divisor of q and r.

```Java
//Euclid's Algorithm in Java
public static int gcd(int p,int q){
if(q == 0) return p;
int r = p % q;
return gcd(q,r);
}
```

## Related Notes