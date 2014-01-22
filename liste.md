# Les listes

## Qu'est-ce qu'une liste pour Python ?
Dans un terminal, exécutons Python et créons une liste : maliste
~~~~
>>> maliste=['Einstein',3.14159, 2, 'Newton']
>>> maliste
['Einstein', 3.14159, 2, 'Newton']
>>> maliste[0]
'Einstein'
>>> maliste[1]
3.14159
~~~~

####Définition 
Une liste est un ensemble de données indexées. 

En effet quand on appelle maliste python affiche la liste de toutes les données. Celles-ci sont classées avec un indice de position (qui démarre à 0). 


## Modification et ajout d'un élément dans une liste
Le contenu d'une liste n'est pas figée. On peut modifier un élément de la liste.
~~~
>>> maliste[0]='Galois'
>>> maliste
['Galois', 3.14, 2, 'Newton']
~~~~
Ajoutons à notre liste un nouvel élément. En pensant liste comme variable, on peut essayer:
~~~
>>> maliste=maliste+42
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: can only concatenate list (not "int") to list
~~~
Erreur de **type** : cela signifie que nous avons voulu ajouter des torchons et des serviettes. Un peu comme en physique lorsque l'on ajoute des secondes avec des mètres !

**Moralité**: Il faut ajouter des listes avec des listes !

~~~~
>>> maliste=maliste+[42]
>>> maliste
['Galois', 3.14, 2, 'Newton', 42]
~~~~

## Avis de recherche 
Comment savoir que la liste contient tel élément ? Demandez à Python...
~~~
>>> bricabrac=["Martin",180,3.14,"Julie",5,9,"Martin"]
>>> 5 in bricabrac
True
>>> Martin in bricabrac
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'Martin' is not defined
>>> "Martin" in bricabrac 
True
~~~
Dans la liste bricabrac, on a demandé "est ce qu'il y a un élément dont la valeur est 5 ?" reponse True. L'expression 5 in braicabran est donc booléenne. 
## Méthodes des listes
Une liste est un objet. Contrairement à une variable qui se contente de stocker de l'information, un objet dispose de fonctionnalités appelées **méthodes**. Voyons quelques unes de ces méthodes.

* Ajout d'éléments à une liste
Essayez le programme suivant (dans sypder)
~~~
maliste = [1, 2, 3, 4, 5]
maliste.append(6)
print maliste
~~~
On dit que *append* est une méthode de l'objet maliste. Cette méthode a permis d'ajouter l'élément 6 dans la liste nommée maliste.
~~~
maliste = [1, 2, 3, 4, 5]
maliste.extend([6, 7, 8]) 
print maliste 
~~~
On dit que *extend* est une méthode de l'objet maliste. C'est une sorte de fonction qui est appliquée aux données de maliste.

* Suppression d'éléments
~~~
maliste = [1, 2, 3, 4, 5]
maliste.remove(1) 
print maliste
~~~
La méthode *remove* retire de la liste  un élément ici 1.

* Connaître la position d'un élément dans une liste
On utilise la méthode index
~~~
>>> liste=[1,2,"a","coucou",1.5]
>>> liste.index("coucou")
3
~~~

* Tri
On peut ordonner les éléments d'une liste en faisant appel à la méthode *sort*
~~~
maliste = [3, 1, 4, 2, 5]
maliste.sort()
print liste
~~~
On peut trier du plus grand au plus petit en utilisant l'option reverse=True
~~~
maliste = [3, 1, 4, 2, 5]
maliste.sort(reverse=True)
print maliste
~~~

## Les compréhensions de liste

On peut à partir d'une liste générer une autre liste de façon "intelligente" par exemple à partir d'une liste contenant les entiers 0, 1, 2, 3, 4 on va générer les nombres 0, 3, 6, 9, 12. 

~~~

liste_initiale = [0,1,2,3,4]
liste_triple = [3*nb for nb in liste_intiale]
print liste_triple
~~~

Cette technique qui consiste à parcourir une liste en en revoyant une autre modifiée s'appelle *la compréhension de liste* (list comprehensions en anglais)

On peut ajouter un test afin de filtrer certains éléments présents dans liste_initiale. Par exemple, on peut extraire les éléments pairs.

~~~
liste_initiale = [0,1,2,3,4]
liste_nb_paire = [nb for nb in liste_intiale if nb%2==0] """nb parcourt liste_initiale éléments après éléments, si cet élément est pair, on le stocke dans liste_nbpaire"""
print liste_nb_paire
~~~

## Conclusion
Vous avez appris à 

* Créer une liste
* Modifier les éléments d'une liste (ajout/suppression)
* Créer une liste à partir d'une liste de départ en utilisant un filtre conditionnel : nouvelle_liste=[element for element in liste_départ if condition]
* Utiliser les méthodes d'un objet dans la cas de l'objet liste

En savoir plus sur [les méthodes des listes]: [Doc_listes] 

[Retour au Sommaire][sommaire]


[sommaire]: http://physiquelycee.fr/ISN/sommaire.html "Le sommaire"
[Doc_listes]: http://docs.python.org/2/tutorial/datastructures.html