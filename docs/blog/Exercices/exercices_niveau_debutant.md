# Niveau Débutant

Ces exercices permettent de comprendre la création, la manipulation et l'utilisation des variables dans différents contextes.

**Exercice 1**
=== "Sujet"
    Créez deux variables : 
    une qui stocke votre prénom et une autre qui stocke votre âge. 
    Affichez ces variables avec une phrase descriptive.

=== "Proposition de correction"
    ```python
    prenom = "Youssouf"
    age = 30
    print(f"Je m'appelle {prenom} et j'ai {age} ans.")
    ```

**Exercice 2**
=== "Sujet"
    Créez deux variables contenant chacune un nombre. 
    Additionnez ces deux nombres et affichez le résultat.
    
=== "Proposition de correction"
    ```python
    nombre1 = 5
    nombre2 = 8
    resultat = nombre1 + nombre2
    print("Le résultat de l'addition est :", resultat)
    ```

**Exercice 3**
=== "Sujet"
    Créez deux variables contenant des chaînes de caractères et concaténez-les (les mettre bout à bout) pour former une seule phrase complète.
    
=== "Proposition de correction"
    ```python
    partie1 = "Bonjour, je suis "
    partie2 = "en train d'apprendre Python."
    phrase_complete = partie1 + partie2
    print(phrase_complete)
    ```

**Exercice 4**
=== "Sujet"
    Écrivez un script qui demande à l'utilisateur de saisir son nom et son année de naissance, puis calculez son âge et affichez-le.
    
=== "Proposition de correction"
    ```python
    nom = input("Entrez votre nom : ")
    annee_naissance = int(input("Entrez votre année de naissance : "))
    age = 2024 - annee_naissance  # Remplacez 2024 par l'année actuelle
    print(f"{nom}, vous avez {age} ans.")
    ```

**Exercice 5**
=== "Sujet"
    Demandez à l'utilisateur de saisir un nombre. Si ce nombre est positif, affichez "Le nombre est positif". 
    Si le nombre est zéro, affichez "Le nombre est zéro". Sinon, affichez "Le nombre est négatif".
    
=== "Proposition de correction"
    ```python
    nombre = int(input("Entrez un nombre : "))
    if nombre > 0:
        print("Le nombre est positif.")
    elif nombre == 0:
        print("Le nombre est zéro.")
    else:
        print("Le nombre est négatif.")
    ```

**Exercice 6**
=== "Sujet"
    Écrivez un programme qui demande à l'utilisateur d'entrer une lettre, puis détermine si cette lettre est une voyelle ou une consonne.
    
=== "Proposition de correction"
    ```python
    
    # Demander à l'utilisateur d'entrer une lettre
    lettre = input("Entrez une lettre : ").lower()

    # Vérifier si la lettre est une voyelle ou une consonne
    if lettre in 'aeiou':
        print("La lettre est une voyelle.")
    elif lettre.isalpha():
        print("La lettre est une consonne.")
    else:
        print("Ce n'est pas une lettre valide.")
    ```

**Exercice 7**
=== "Sujet"
    Écrivez un programme pour afficher la table de multiplication de 1 à 10 pour un nombre donné par l'utilisateur.
    
=== "Proposition de correction"
    ```python
    
    # Demander à l'utilisateur d'entrer un nombre
    nombre = int(input("Entrez un nombre : "))

    # Afficher la table de multiplication de 1 à 10 pour ce nombre
    print(f"Table de multiplication de {nombre} :")
    for i in range(1, 11):
        print(f"{nombre} x {i} = {nombre * i}")
    ```

**Exercice 8**
=== "Sujet"
    Écrivez un programme qui demande à l'utilisateur d'entrer son âge, puis détermine s'il est éligible pour voter (l'âge de vote est 18 ans ou plus).
    
=== "Proposition de corrigé"
    ```python

    # Demander à l'utilisateur d'entrer son âge
    age = int(input("Entrez votre âge : "))

    # Vérifier l'admissibilité à voter
    if age >= 18:
        print("Vous êtes éligible pour voter.")
    else:
        print("Vous n'êtes pas éligible pour voter.")
    ```

**Exercice 9**
=== "Sujet"
    Écrivez un programme pour créer liste de fruits : pomme, banane, cerise, orange, et mangue. Utiliser une boucle pour afficher chaque élément de la liste
    
=== "Proposition de corrigé"
    ```python

    # Liste de fruits
    fruits = ["pomme", "banane", "cerise", "orange", "mangue"]

    # Utiliser une boucle for pour afficher chaque élément de la liste
    for fruit in fruits:
        print(fruit)
    ```
