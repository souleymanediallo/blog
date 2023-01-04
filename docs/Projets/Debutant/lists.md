# Les Listes

## Définition

Les listes sont des séquences ordonnées pouvant contenir divers types d'objects. En d'autres termes, une liste est une collection d'éléments ordonnés et modifiables.

## Créer une liste

```py linenums="1"
Une liste de chaînes de caractère
>>> ma_liste = ["Mbabbe", "Ronaldo", "Neymar", "Benzema"]

Une liste de nombres
>>> ma_liste = [1, 2, 3, 4, 5, 7, 8, 9, 10]

Une liste mixte de nombres et de chaîne de caractère
>>> ma_liste = [75, "Paris", 13, "Marseille", 69, "Lyon"]

Une liste de listes
>>> ma_liste = [['Un', 'Deux', 'Trois'], ['Cinq', 'Six', 'Sept']]
```

Comme vous pouvez le voir, les éléments sont entre crochets, c'est-à-dire `[]` et chaque élément est séparé par une virgule. Une liste peut contenir des types de données tels que des chaînes, des entiers, des nombres flottante, etc. En plus de cela, les listes peuvent également être imbriquées, c'est-à-dire que vous pouvez inclure une liste dans une liste.

## Index

Les listes prennent en chargent l'indexation et le découpage en tranches, tout comme les chaînes de caractère. L'index de liste est sa position. La numérotation de l'index commence à zéro.

```py linenums="1"
nom_de_ma_liste = ['Paris', 'Marseille', 'Lyon']
index_de_ma_liste  [0]        [1]          [2]
```

Donc, si nous voulons obtenir le premier élément de la liste c'est-à-dire `75`, nous tapons le nom de la liste suivi de crochets et l'index zéro.

```py linenums="1"
>>> ma_liste = [75, "Paris", 13, "Marseille", 69, "Lyon"]
>>> ma_liste[0]
75
```

Ensuite, le quatrième élément `Marseille` est à l'index trois

```py linenums="1"
>>> ma_liste = [75, "Paris", 13, "Marseille", 69, "Lyon"]
>>> ma_liste[3]
'Marseille'
```

Les listes sont également modifiales après leur création.

Créer une liste vide puis ajouter chaque élément en utilisant la méthode append

```py linenums="1"
>>> jour_de_semaine = []
>>> jour_de_semaine.append('Lundi')
>>> jour_de_semaine.append('Mardi')
>>> jour_de_semaine.append('Mercredi')
```

Si nous exécutons la commande nous pouvons voir les trois éléments que nous avons ajoutés : Lundi, Mardi et Mercredi.

```py linenums="1"
>>> jour_de_semaine
['Lundi', 'Mardi', 'Mercredi']
```

Pour supprimer un élément vous pouvez utiliser la méthode `remove` et transmettre la valeur. Par exemple supprimer `Monaco`

```py linenums="1"
>>> ville = ["Nice", "Marseille", "Monaco"]
>>> ville.remove("Monaco")
>>> ville
['Nice', 'Marseille']
```

Vous pouvez supprimer un élément par un index. Pour ce faire, utilisez le mot clé `del` suivi de l'indice de l'élément

Comment pouvons-nous vérifier si un élément est dans une liste ?
En ulisant une instruction if comme dans l'exemple ci-dessous. Nous vérions si le chiffre `1` est dans la liste d'afficher vrai.

```py linenums="1"
>>> if 1 in [1, 2, 3]:
	print('True')


True
>>>
```

## Boucle for

Nous pouvons utiliser la boucle for afficher chaque élément de la liste

```py linenums="1"
>>> villes = ["Nice", "Marseille", "Monaco"]
>>> for ville in villes:
    # l'intérieur de la boucle est mis en retrait (l'indentation)
	print(ville)


Nice       # première boucle
Marseille  # deuxième boucle
Monaco     # troisième boucle
>>>
```

## Fonction range
La fonction range en Python génère et retourne une séquence de nombres entiers basé sur les arguments de la fonction.
```py linenums="1"
>>> range(10)
range(0, 10)
>>> 
```
Une liste avec 10 entre parenthèses, crée une séquence de chiffres de 0 à 9.
```py linenums="1"
>>> range(0, 10, 1)
# La valeur de début est 0.
# La valeur d'arrêt est 10.
# Le nombre de pas 1.
>>> 
```
Nous pouvons utiliser une boucle for comme nous l'avons vu auparavant avec la séquence générée par range.

```py linenums="1"
>>> for i in range(11):
    # Cela nous permet de boucler un certain nombre de fois.
	print(i)

	
0
1
2
3
4
5
6
7
8
9
10
```