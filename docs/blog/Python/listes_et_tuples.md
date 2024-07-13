# Les listes et les tuples
Python offre deux types de données pour stocker des collections : les listes et les tuples. Les deux permettent de stocker une collection d'éléments, mais ils diffèrent principalement par leur mutabilité : les listes sont modifiables alors que les tuples ne le sont pas.

## Les tuples

**Considérez les tuples comme des lignes**

Les tuples sont souvent utilisés pour stocker des données qui ont une structure fixe. Imaginez un tuple comme une ligne dans une base de données ou une feuille de calcul, où chaque élément représente une donnée spécifique d'un enregistrement.

**Créer des tuples**

Pour créer un tuple, vous pouvez entourer une séquence de valeurs avec des parenthèses ```( )```, séparées par des virgules.
```python 
mon_tuple = (1, 2, 3)
print(mon_tuple)  # Affiche (1, 2, 3)
```

**Tuples et chaînes d'indexation**

Les éléments d'un tuple peuvent être accédés par leur index, tout comme les listes et les chaînes. Les index commencent à 0.
```python 
print(mon_tuple[1])  # Affiche 2
```

**Trancher les tuples et les chaînes**

Le "slicing" permet de récupérer des sous-parties d'un tuple ou d'une chaîne en spécifiant un début et une fin d'index.
```python
mon_tuple = (1, 2, 3, 4, 5)
print(mon_tuple[1:4])  # Affiche (2, 3, 4)
```

**Explorez l'immuabilité dans les tuples et les chaînes**

Les tuples et les chaînes sont immuables, ce qui signifie que vous ne pouvez pas modifier leurs éléments une fois qu'ils sont créés.
```python
mon_tuple[1] = 10  # Cela provoquera une erreur TypeError
```

**Sachez que les tuples et les chaînes sont itérables**

Vous pouvez itérer sur les éléments d'un tuple ou d'une chaîne avec une boucle for.
```python
for item in mon_tuple:
    print(item)
```

**Décompresser les tuples**

La décompression de tuple vous permet d'assigner les éléments d'un tuple à des variables distinctes.
```python
a, b, c = mon_tuple
print(a, b, c)  # Affiche 1 2 3
```

**Inspecter les types de retour de base de données**

Lors de l'utilisation de bases de données, il est courant de recevoir des données sous forme de tuples, représentant des lignes d'une table.
```python
ligne = (93200, "Kylian", "Mbappe")
id, prenom, nom = ligne
print(prenom)  # Affiche Kylian
```

**Vérifier l'existence des éléments**

Utilisez **`in`** pour vérifier si un élément est présent dans un tuple ou une chaîne.
```python
if "Kylian" in ligne:
    print("Kylian est présent.")
``` 

**Renvoyer plusieurs valeurs à partir d'une fonction**

Les fonctions peuvent retourner plusieurs valeurs sous forme d'un tuple, qui peut ensuite être décomposé en variables.
```python
def obtenir_info():
    return "Kylian", "Mbappe", 25  # Retourne un tuple

prenom, nom, age = obtenir_info()
print(prenom, age)  # Affiche Kylian 25
```

**Exercice**

=== "Sujet"
    Voici quelques exercices pour vous entraîner à manipuler des tuples :
    
    1. Créez un tuple avec les jours de la semaine.
    2. Accédez au mercredi dans le tuple.
    3. Récupérez les jours de week-end.
    4. Vérifiez si "Samedi" est dans le tuple.
    5. Créez un tuple avec trois nombres : 1, 2, 3 et décompressez-les en trois variables.
    
=== "Proposition de corrigé"
    ```python
    jours = ("Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi", "Dimanche")
    mercredi = jours[2]
    weekend = jours[5:7]
    print("Samedi" in jours)  # True
    x, y, z = (1, 2, 3)
    print(x, y, z)  # Affiche 1 2 3
    ```

## Les listes

Les listes en Python sont des structures de données flexibles, idéales pour stocker une collection ordonnée et modifiable d'éléments. Elles sont similaires aux tableaux dans d'autres langages de programmation mais sont plus puissantes en raison de leur flexibilité et de leur capacité à stocker différents types de données.

**Créer des listes**

Pour créer une liste, utilisez les crochets **[ ]** et séparez les éléments par des virgules.
```python
ma_liste = [1, 2, 3, 4, 5]
print(ma_liste)  # Affiche [1, 2, 3, 4, 5]
```

**Travailler avec des listes**

Les listes sont itérables et chaque élément peut être accédé par son index, où l'index commence à 0.
```python
print(ma_liste[0])  # Affiche 1
```

**Modifier des éléments dans une liste**

Vous pouvez modifier un élément de la liste directement par son index.
```python
ma_liste[0] = 10
print(ma_liste)  # Affiche [10, 2, 3, 4, 5]
```

**Ajouter et supprimer des éléments de liste**

Utilisez **append()** pour ajouter et **remove()** pour supprimer un élément spécifique.
```python
ma_liste.append(6)
print(ma_liste)  # Affiche [10, 2, 3, 4, 5, 6]

ma_liste.remove(6)
print(ma_liste)  # Affiche [10, 2, 3, 4, 5]
```

**Travailler avec des listes de nombres**

Vous pouvez effectuer des opérations telles que le tri ou la recherche de la somme des éléments.
```python
print(sum(ma_liste))  # Affiche 24
ma_liste.sort()
print(ma_liste)  # Affiche [2, 3, 4, 5, 10]
```

**Créer des compréhensions de liste**

Les compréhensions de liste fournissent une manière concise de créer des listes.
```python
carres = [x**2 for x in ma_liste]
print(carres)  # Affiche [4, 9, 16, 25, 100]
```

**Imbriquer vos listes**

Les listes peuvent contenir d'autres listes comme éléments.
```python
liste_imbriquee = [1, 2, [3, 4], 5]
print(liste_imbriquee)  # Affiche [1, 2, [3, 4], 5]
```

**Créer une deuxième référence à un objet de liste**

Assigner une liste à une nouvelle variable crée une référence à l'objet original.
```python
nouvelle_reference = ma_liste
nouvelle_reference.append(20)
print(ma_liste)  # Affiche [2, 3, 4, 5, 10, 20]
```

**Créer une copie superficielle d'une liste**

Une copie superficielle crée une nouvelle liste, mais partage les éléments internes.
```python
copie_superficielle = ma_liste[:]
copie_superficielle.append(30)
print(copie_superficielle)  # Affiche [2, 3, 4, 5, 10, 20, 30]
print(ma_liste)             # Affiche [2, 3, 4, 5, 10, 20]
```

**Créer une copie complète d'une liste**

Utilisez **deepcopy** pour les listes imbriquées où les copies indépendantes des sous-listes sont nécessaires.
```python
from copy import deepcopy
copie_profonde = deepcopy(liste_imbriquee)
copie_profonde[2].append(99)
print(copie_profonde)  # Affiche [1, 2, [3, 4, 99], 5]
print(liste_imbriquee) # Affiche [1, 2, [3, 4], 5]
```

**Triez vos listes**

Utilisez la fonction **sort()**.
```python
ma_liste.sort()
print(ma_liste)  # Affiche [2, 3, 4, 5, 10, 20]
```

**Passer une fonction intégrée pour le tri**

Tri par longueur d'éléments ou d'autres critères avec **sorted()**.
```python
noms = ["Yahya", "Adama", "Zara"]
noms_tries = sorted(noms, key=len)
print(noms_tries)  # Affiche ['Zara', 'Yahya', 'Adama']
```

**Utiliser une fonction personnalisée pour le tri**

Définissez une fonction pour spécifier le critère de tri.
```python
def obtenir_dernier_caractere(chaine):
    return chaine[-1]

noms_tries_par_dernier = sorted(noms, key=obtenir_dernier_caractere)
print(noms_tries_par_dernier)  # Affiche ['Adama', 'Zara', 'Yahya']
```

**Exercice**

=== "Sujet"
    Voici quelques exercices pour vous entraîner à manipuler les listes :
    
    1. Créer et afficher une liste de nombres pairs de 2 jusqu'à 10.
    2. Ajouter un élément à la liste et supprimer un élément de la liste.
    3. Trier une liste de chaînes par la longueur des chaînes.
    4. Utiliser une compréhension de liste pour créer une liste des carrés des nombres de 1 à 5.
    5. Imbriquer une liste dans une autre liste et accéder à un élément de la liste imbriquée.
    
=== "Proposition de corrigé"
    ```python
    pairs = [2, 4, 6, 8, 10]
    print(pairs) # Affiche [2, 4, 6, 8, 10]
    pairs.append(12)
    pairs.remove(2)
    noms.sort(key=len)
    carres = [x**2 for x in range(1, 6)]
    liste_imbriquee = [[1, 2], [3, 4]]
    print(liste_imbriquee[1][0])  # Affiche 3
    ```

## En résumé
Les listes et les tuples sont des structures fondamentales en Python pour la gestion des collections de données. Les listes sont modifiables et très flexibles, tandis que les tuples sont immuables et souvent utilisés pour les données qui ne doivent pas être modifiées après leur création.