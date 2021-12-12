# Compte rendu du TP2

# Objectif :
Le but de ce TP est :
* Découvrir la méthode de calcul du polynôme d'interpolation de Lagrange.
* Observer le phénomène de Runge.
* Découvrir la méthode de calcul du polynôme de Newton.

# Polynôme d'interpolation de Lagrange
Le polynôme d’interpolation de Lagrange est l’unique polynôme de degré au plus n passant par une famille de n + 1 points (xi,yi) de R2, d’abscisses distinctes. 
L'interpolation de Lagrange consiste à chercher un polynôme qui passe par un ensemble des points (xi, yi) . Si le valeurs yi sont obtenues en évaluant une fonction f aux points xi , donc yi = f(xi) , on parle d’un polynôme de Lagrange associé à la fonction f aux points (xi).
Soit n>0 un nombre entier et soient (xi)0<i<n nombres réels distincts. Soient (yi)0<i<n nombres réels. Il est facile à voir qu’il existe un unique polynôme P de degré au plus n tel que : P(xi) = yi
Pour déterminer le polynôme P satisfaisant les égalités (P) il suffit de considérer un polynôme P = sum(ai*Xi) et d’utiliser les relations (P) afin de déterminer les coefficients ai.

# Le phénomène de Runge 
Le phénomène de Runge se traduit par une mauvaise interpolation, lorsque l'on augmente le degré du polynôme d'interpolation de Lagrange, de la fonction f définie sur R par:
f(x) = 1/(1+x^2)

Dans ce TP on va observer ce phénomène et mettre en oeuvre une meilleure répartition des points d'interpolation à l'aide des racines des polynômes de Tchebycheff puis constater l'atténuation du phénomène de Runge. Plus particulièrement, on va implémenter des fonctions permettant de calculer le polynôme d'interpolation de Lagrange par la méthode directe. L'interpolation par la méthode de Lagrange et celle de Newton nous est ensuite donnée. Enfin, à partir de la méthode de Newton, on fera l'interpolation en utilisant les points de Tchebycheff.

# Polynôme de Newton
La méthode de Newton, comme pour celle de Lagrange, permet d'exprimer le polynômed'interpolation de Lagrange dans une base de polynômes, qui sont les polynômes de Newton. Étant donné une fonction f et un ensemble (xj) de points d'interpolation, le polynôme d'interpolation p s'exprime comme:
p(x)=sum(zj*Nj,n(x))
avec Nj,n la base de polynôme de Newton donnée par:
Nj,n(x) = prod(x-xk)
et (zj) les coefficients qui sont solution du système triangulaire.

# Conclusion
Interpolation polynomiale:
  *évaluer la fonction en un point : Polynôme de Lagrange 
  *compiler la fonction : Polynôme de Newton 
-------  
Phénomène de Runge:
  *comparer les differents méthodes de calcul
-------  
Interpolation polynomiale par morceau : 
  *spline cubique d’interpolation
  *spline cubique d’approximation 
 






