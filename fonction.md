# Les Fonctions

## Que savons déjà concernant les fonctions ?

En mathématiques, une fonction f associe à une variable $x$ une valeur notée $f(x)$. 

- Par exemple: Soit la fonction f qui a $x$ associe $2x+1$. On sait que si $x$ vaut 2, la valeur de $f(x)$ sera 5. En algorithmique, on dira que la fonction f retourne (ourenvoie) la valeur 5. 
En python, cela s'écrit:
~~~

# on definit la fonction par def nom de la fonction (variable1, variable2, ...)
def f(x)
return 2*x+1 "valeur de retour 2x+1"
# Corps du programme
resultat = f(2) #on appelle la fonction f en lui passant la valeur 2
              #la valeur renvoyee est stockee dans resultat
print resultat #affiche la valeur de f(2)         

~~~

## Ecrivons nos propres fonctions
 1. Ecrire une fonction qui reçoit deux arguments x et y et qui renvoie leur produit.
 2. Ecrire une fonction qui renvoie le message "pair" si un nombre est pair et "impair" si le nombre est impair.

## Autres usages des fonctions
On a besoin souvent de la même suite d'instructions, alors plutôt que de répéter les mêmes lignes de programmes, on appelle une fonction. Cette fonction n'a pas de paramètres. 

~~~
def salut()
    print 'Bonjour'
>>>salut()
Bonjour

~~~
### Curiosité intéressante...

Une fonction peut s'appeler elle-même ! Cela signifie que dans les instructions qui définissent la fonction, on trouve un appel de cette même fonction. 

**Exemple:** la fonction factorielle définie par $n!=1\times2\times3\times .... \times (n-1) \times n$ peut être vue comme le produit $n\times (n-1)!$ c'est à dire que pour calculer factorielle n on appelle la fonction factorielle avec comme paramètre $n-1$ et on multiplie par $n$.
Comment écrire cela en python ?

~~~
def factorielle(n):
    if n==1: #par definition 1! = 1 
        return 1
    return n*factorielle(n-1) 

monEntier=input("Entrer un nombre")
print "La factorielle de ",monEntier,"est ",factorielle(monEntier)
~~~

## Portée des variables
Les variables déclarées dans une fonction sont appelées \textbf{variables locales}. Ces variables ne sont connues qu'à l'intérieur de la fonction.

~~~
def mafonction():
    x = 2
    print 'x vaut',x,'dans la fonction'
""" Corps du programme"""
mafonction()
~~~

## Au travail
A vous de coder les fonctions suivantes.

1. La fonction RangMin qui reçoit une liste de 10 nombres non classés et renvoie la position du plus petit nombre présent dans cette liste.
2. 
[Retour au Sommaire][sommaire]


[sommaire]: http://physiquelycee.fr/ISN/sommaire.html "Le sommaire"