# 3. La notation Big-O

La notation Big-O, également appelée notation O, est une notation utilisée en informatique pour décrire la complexité temporelle ou spatiale des algorithmes. Elle exprime la limite supérieure du temps de calcul ou de l'espace mémoire nécessaire en fonction de la taille de l'entrée. Cette notation permet de comparer l'efficacité des algorithmes et d'analyser leur performance, surtout pour les grandes entrées.

## 3.1 Principales classes de complexité en notation Big-O :

### 1. O(1) – Constant Time :

- **Description :** L'exécution de l'algorithme prend un temps constant, quelle que soit la taille de l'entrée.
- **Exemple :** Accéder à un élément d'un tableau par son index.

### 2. O(log n) – Logarithmic Time :

- **Description :** Le temps de l'algorithme croît logarithmiquement avec la taille de l'entrée.
- **Exemple :** Recherche binaire dans une liste triée.

### 3. O(n) – Linear Time :

- **Description :** Le temps de l'algorithme croît linéairement avec la taille de l'entrée.
- **Exemple :** Parcourir tous les éléments d'une liste.

### 4. O(n log n) – Linearithmic Time :

- **Description :** Le temps de l'algorithme est proportionnel à n log n.
- **Exemple :** Tri rapide (Quick Sort) et tri fusion (Merge Sort).

### 5. O(n²) – Quadratic Time :

- **Description :** Le temps de l'algorithme croît quadratiquement avec la taille de l'entrée.
- **Exemple :** Tri à bulles (Bubble Sort) et tri par insertion (Insertion Sort).

### 6. O(2^n) – Exponential Time :

- **Description :** Le temps de l'algorithme double à chaque ajout d'un élément à l'entrée.
- **Exemple :** Algorithmes de résolution de problèmes combinatoires comme le problème du voyageur de commerce (brute force).

### 7. O(n!) – Factorial Time :

- **Description :** Le temps de l'algorithme croît de manière factorielle avec la taille de l'entrée.
- **Exemple :** Génération de toutes les permutations d'un ensemble.

## 3.2 Exemples et explications

### Exemple 1 : Recherche linéaire

```python
def recherche_lineaire(liste, cible):
    for element in liste:
        if element == cible:
            return True
    return False
```

- **Complexité :** O(n)
- **Explication :** Dans le pire des cas, l'algorithme doit vérifier chaque élément de la liste une fois, donc le temps de calcul est proportionnel à la taille de la liste.

### Exemple 2 : Tri rapide (Quick Sort)

```python
def tri_rapide(liste):
    if len(liste) <= 1:
        return liste
    pivot = liste[len(liste) // 2]
    gauche = [x for x in liste if x < pivot]
    milieu = [x for x in liste if x == pivot]
    droite = [x for x in liste if x > pivot]
    return tri_rapide(gauche) + milieu + tri_rapide(droite)
```

- **Complexité :** O(n log n) en moyenne, O(n²) dans le pire des cas.
- **Explication :** L'algorithme divise la liste en deux parties à chaque étape, et chaque division nécessite un temps proportionnel à la taille de la liste.

### Exemple 3 : Accès à un élément d'un tableau

```python
element = tableau[index]
```

- **Complexité :** O(1)
- **Explication :** Accéder directement à un élément d'un tableau par son index prend un temps constant, indépendamment de la taille du tableau.

### En résumé 

**Pourquoi la notation Big-O est importante**

- **Comparaison d'algorithmes :** Elle permet de comparer différents algorithmes et de choisir le plus efficace pour une tâche donnée.
- **Analyse de performance :** Elle aide à prévoir comment un algorithme se comportera à grande échelle, ce qui est crucial pour les applications nécessitant un traitement de grandes quantités de données.
- **Optimisation :** Comprendre la complexité des algorithmes permet aux développeurs de les optimiser et d'améliorer les performances globales des logiciels.

La notation Big-O est un outil essentiel en informatique pour évaluer et comparer les performances des algorithmes de manière théorique et pratique.