# HTML et CSS

## Contexte
La page internet que vous visualisez actuellement est le produit de deux choses :

* Du contenu : le texte que vous lisez, et sa structure : titre, sous-titre, paragraphe, lien etc...
* D'une mise en forme du contenu : police de caractère, alignement, choix des couleurs etc...

Une page web élémentaire peut se contenter uniquement de contenu. Ce contenu est alors stocké dans un fichier dont l'extension est html.

##Notre première page html

Nous allons créer un fichier texte (texte brut) dans un éditeur type notepad. Ce texte va contenir les informations que l'on souhaite afficher sur la page web et il est codifié afin d'être interprété par le navigateur internet.

~~~
<!DOCTYPE html>
<html>
<head>
    <title> Le titre de ma page</title>
</head>

<body>

<h1> Un titre </h1>
Du texte au kilomètre ... 
</body>
</html>
~~~
La première ligne indique que le fichier contient des informations structurées en HTML. En regardant la suite du code, on observe la présence de **balises**.
Elles vont par pair. On dit que la première est ouvrante et que la seconde est fermante.

Par exemple :
~~~
<h1> Un titre </h1>
~~~
h1 est une balise de titre, le code précédent, signifie que ce qui est entre les deux balises h1 sera un texte qui sera affiché avec le formatage d'un titre1.


## Quelques balises
~~~

<img src="image.jpg" alt="arc en ciel">
<a  href="http://physiquelycee.fr"> Allez faire un tout là </a>
<ul> 
        <li> Proposition 1 </li> 
        <li> Proposition 2 </li> 
        <li> Proposition 3 </li> 
    </ul>
~~~
Pour découvrir l'usage d'autre balises je vous recommande les liens suivants : 
[w3 school][w3c]


[w3c]: http://www.w3schools.com/ "W3C"

# CSS 
## Ce qu'est un fichier css
Un fichier css est un fichier supplémentaire au fichier html qui renseigne sur les attributs des balises utilisées dans le fichier html.
Concrètement dans la page html, il y a un titre 1, c'est à dire une balise \<h1> 
Le navigateur exploré le fichier css pour savoir quelle mise en forme appliquée à ce titre. Quelle police ? Quelle taille ? Quelles couleurs etc... 

En effet ces renseignements sont dans le fichier css.

## Observons
Regardons l'effet d'un fichier css sur page html simple.
[page html simple sans css][page simple]
[page html avec css][page avec css]

## Que doit on modifier dans la page html ?
Il faut indiquer au navigateur la présence de ce fichier css. Cela se fait en insérant dans le bloc \<head>
\<link rel="stylesheet" type="text/css" href="style.css">
Ainsi on a:
~~~
<!DOCTYPE html>
<html>
<head>
    <title>
        Ma première page ouaib
    </title>
    <meta http-equiv="Content-Type" content="text/html ; charset=UTF-8">
<link rel="stylesheet" type="text/css" href="style.css">

</head>

~~~

## Et le fichier CSS ?
Puisque la page html appelle le fichier *style.css*, il faut le créer. Dans un éditeur de texte on crée un fichier dont le nom est exactement style.css

Ce fichier contient le code css suivant: 
~~~
/* on définit les caractéristique de body
fond gris et largeur 500 pix pour le texte */

body{
    
background-color:gray;
width:500px;

}
/* Le titre 1 est rose */
h1{
    color:pink;
}

/* les paragraphes sont en Times, taille 18, ils sont inscrit dans un rectangle de 500 pix
par 200 pix, overflow: auto permet de faire défiler le texte si il y a pas assez de place dans le cadre
*/

p{
    font-size:18px;
    font-family:"Times New Roman";
    width:500px; height:200px; overflow:auto; border:solid 1px black;
}

/* les div sont écrits en taille 9 et centré */
div{
        font-size:9px;
    font-family:"Arial";
    text-align : center
}
/* Les liens hypertexte sont violet et avec une ombre*/
a{
    color:#bbbbff;
    text-shadow: 5px 5px 5px #FF00FF
}
~~~

Pour télécharger le ficher css : [style.css](http://physiquelycee.fr/ISN/TP_html/style.css)
Pour télécharger l'image : [image](http://physiquelycee.fr/ISN/TP_html/images.jpeg)
Pour télécharger le projet entier : [TP_html](http://physiquelycee.fr/ISN/TP_html.zip)

[page simple]: http://physiquelycee.fr/ISN/TP_html/page_simple.html
[page avec css]: http://physiquelycee.fr/ISN/TP_html/page_avec_css.html
