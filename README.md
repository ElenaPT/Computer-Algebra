# Computer-Algebra
Collection of computer algebra algorithms implemented in Maple.

## gcd.mws
This file contains the **Euclidean Algorithm** for several rings.
The Euclidean Algorithm calculates the *greatest common divisor* of two elements of a particular field, using Euclidean division and reminders.

This algorithm is implemented for the following rings:
- Z
- Q\[x]
- Z\[x]
- F_p\[x] (where p is a prime number)
- F_q\[x] (where q=p^n, given p prime)

## extendedGcd.mws
This file contains the **Extended Euclidean Algorithm** for several rings.
The Extended Euclidean Algorithm works as the Euclidean Algorithm, but it also returns two coefficients such that the gcd can be expressed as linear combination of the original elements: gcd(a,b)=as+bt.

This algorithm is implemented for the following rings:
- Z
- Q\[x]
- F_p\[x] (where p is a prime number)
- F_q\[x] (where q=p^n, given p prime)

## chineseRemainder.mws
This file contains the **Chinese Remainder** algorithm for several rings.
The Chinese Remainder Theorem states that, given an integer *n*, if the remainders of the Euclidean division of *n* by several integers are known, then the remainder of the division of *n* by the product of those integers can be uniquely determined.

This algorithm is implemented for the following rings:
- Z
- F_p\[x] (where p is a prime number)

## inverse.mws
This file contains two methods to calculate the inverse of an element in finite fields.
Both methods are based on the Extended Euclidean Algorithm.

This algorithm is implemented for the following finite fields:
- F_p (where p is a prime number)
- F_q\[x] (where q=p^n, given p prime)

## FqxPolynomials.mws
This file contains several methods to calculate the elements of F_q\[x]: the field of polynomials with coefficients in the finite field of q elements, where q=p^n, p prime. The input arguments for the method are the prime number *p* and some polynomial *f* such that F_q=F_p/f.

The main method is *Fq*. *BaseFq* and *MatrixFq* are auxiliary methods.

## irreducibility.mws
This file contains a method that checks if an element of the finite field F_q is irreducible.
This method is based on the Euclidean algorithm for F_q.

## discreteLogarithm.mws and shanks.mws
These two files contain algorithms that calculate the discrete logarithm in finite fields.

### discretelogarithm.mws
This file contains three methods:
- **TablaLog** calculates a table containing the different logarithms of the polynomial, one for each logarithmic base.
- **LogDiscreto** is the main method. It returns the logarithm of the given polynomial in the given base, by searching for it in the table previously created.
- **MultConLog** calculates the product of two polynomials, using the table.
All three methods work for polynomials in F_q\[x] (the field of polynomials with coefficients in the finite field of q elements, where q=p^n, p prime).

### shanks.mws
This file contains the **Shanks Algorithm** (also known as Baby-step giant-step), which calculates the discrete logarithm in a more efficient way.

This algorithm is implemented for the following finite fields:
- F_p (where p is a prime number)
- F_q\[x] (where q=p^n, given p prime)

## squarefreeTest.mws
This file contains methods that check if a given polynomial is squarefree.

This method is implemented for the following rings:
- Z\[x]
- F_p\[x] (where p is a prime number)
- F_q\[x] (where q=p^n, given p prime)

## factorizationFqx.mws
This file contains several algorithms to factorize polynomials following different criteria. All of them are implemented for F_q\[x] (the field of polynomials with coefficients in the finite field of q elements, where q=p^n, p prime).

The algorithms included in this file are:
- **Squarefree factorization** is a factorization algorithm that, given a polynomial, returns a factor decomposition such that none of the factors is a square.
- **Distinct degree factorization** is a factorization algorithm that, given a squarefree polynomial, returns a factor decomposition such that every factor is the product of polynomials of the same degree.
- **Same degree factorization** is a factorization algorithm that, given a polynomial which is factorizable in factors of the same degree, returns that factorization.
- **Berlekamp algorithm** is a factorization algorithm that, given a squarefree monic polynomial, returns its factorization in irreducible factors.
- **Berlekamp-Cantor-Zassenhaus algorithm** is a factorization algorithm that, given a squarefree monic polynomial, returns its factorization in irreducible factors.
- **2 step factorization** is an algorithm that calculates the factorization of a polynomial in irreducible factors, using squarefree factorization and Berlekamp algorithm.
- **3 step factorization** is an algorithm that calculates the factorization of a polynomial in irreducible factors, using squarefree factorization, distinct degree factorization and same degree factorization.

## factorizationZx.mws
This file contains two algorithms to factorize polynomials with integer coefficients.

The algorithms included in this file are:
- **Kroneker Method** is a deterministic brute-force algorithm that factorizes polynomials with integer coefficients.
- **Modular Approach Method** is a deterministic algorithm that factorizes polynomials with integer coefficients, using Berlekamp Algorithm and Hensel Lifting.

## aks.mws
This file contains the **AKS primality test** (also known as Agrawal-Kayal-Saxena primality test). It is a deterministic algorithm that checks, in polynomial time, if a given number is prime.


# Developers
This project has been developed by [Elena Pérez Tirador](https://github.com/ElenaPT) and Beatriz Coronado Sanz for the course in Computer Algebra in Universidad Complutense de Madrid
