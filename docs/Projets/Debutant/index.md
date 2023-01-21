# Exercice Simple en pyhon


!!! Exercice N° 1

    === "Question"

        ``` markdown
        Afficher "Bonjour tout le monde!"
        ```

    === "Réponse"

        ``` markdown
        print("Bonjour, monde!")
        ```

!!! Exercice N° 2

    === "Question"

        ``` markdown
        Stocker votre nom dans une variable nom et afficher "Bonjour, [nom]"
        ```

    === "Réponse"

        ``` markdown
        nom = "Mbappe"
        print("Bonjour, " + nom)
        ```

!!! Exercice N° 3

    === "Question"

        ``` markdown
        Calculer la somme de deux nombres(5 et 3) et stocker le résultat dans une variable resultat.
        ```

    === "Réponse"

        ``` markdown
        x = 5
        y = 3
        resultat = x + y
        print(resultat)
        ```

!!! Exercice N° 4

    === "Question"

        ``` markdown
        Demander à l'utilisateur de saisir un nombre et afficher le résultat de la multiplication de ce nombre par 2
        ```

    === "Réponse"

        ``` markdown
        x = input("Saisissez un nombre: ")
        x = int(x)
        resultat = x * 2
        print(resultat)
        ```

!!! Exercice N° 5

    === "Question"

        ``` markdown
        Utiliser une boucle pour afficher les nombres de 1 à 10
        ```

    === "Réponse"

        ``` markdown
        for i in range(1, 11):
            print(i)
        ```

!!! Exercice N° 6

    === "Question"

        ``` markdown
        Utiliser une boucle pour afficher la somme des nombres de 1 à 10
        ```

    === "Réponse"

        ``` markdown
        somme = 0
        for i in range(1, 11):
            somme += i
        print(somme)
        ```

!!! Exercice N° 7

    === "Question"

        ``` markdown
        Utiliser une boucle pour afficher les nombres pairs de 1 à 10
        ```

    === "Réponse"

        ``` markdown
        for i in range(1, 11):
        if i % 2 == 0:
            print(i)
        ```

!!! Exercice N° 8

    === "Question"

        ``` markdown
        Créer une fonction qui prend un nombre en paramètre et renvoie son carré
        ```

    === "Réponse"

        ``` markdown
        def carre(x):
            return x * x

        resultat = carre(5)
        print(resultat)
        ```

!!! Exercice N° 9

    === "Question"

        ``` markdown
        Utiliser une liste pour stocker 3 noms de votre choix et utiliser une boucle pour les afficher
        ```

    === "Réponse"

        ``` markdown
        noms = ["Olivier", "Marie", "Karim"]
        for nom in noms:
            print(nom)
        ```

!!! Exercice N° 10

    === "Question"

        ``` markdown
        Utiliser un dictionnaire pour stocker des informations sur des étudiants (nom, âge, note) et utiliser une boucle pour afficher au moins 3 étudiants.
        ```

    === "Réponse"

        ``` markdown
        etudiants = [
        {"nom": "John", "age": 20, "note": 75},
        {"nom": "Marie", "age": 22, "note": 82},
        {"nom": "Robert", "age": 19, "note": 65}
        ]

        for etudiant in etudiants:
            nom = etudiant["nom"]
            age = etudiant["age"]
            note = etudiant["note"]
            print("Nom: " + nom + ",  Age: " + str(age) + ",  Note: " + str(note))
        ```
