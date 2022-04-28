# Boole's Expansion Theorem
Boole's expansion theorem, also known as *Shannon expansion* or *decomposition*, states that for any [[Boolean Functions|Boolean function]] $F$,
$$F(X_{1},X_{2},\dots,X_{n})=X_{1}F(1,X_{2},\dots,X_{n})+\bar{X_1}F(0,X_{2},\dots, X_{n})$$
The [[Duality#Boolean Algebra|dual]] form of the theorem is
$$F(X_{1},X_{2},\dots,X_{n})=(X_{1}+F(0,X_{2},\dots,X_{n}))(\bar{X_{1}}+F(1,X_{2},\dots,X_{n}))$$
Repeatedly applying the theorem or its dual for each argument gives the [[Standard Forms of a Boolean Function#Sum of products form||sum of products]] form or the [[Standard Forms of a Boolean Function#Product of sums form|product of sums]] form of the function, respectively.