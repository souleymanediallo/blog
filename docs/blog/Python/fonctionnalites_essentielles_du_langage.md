# Programmation Objet en Python

## Les fonctions
Pour couvrir les concepts des fonctions, des modules et des packages en Python, nous allons explorer chaque sujet un par un avec des exemples pratiques.

**Définition :** Une fonction est un bloc de code réutilisable qui effectue une tâche spécifique. Voici comment créer et appeler une fonction en Python.

```python 
def greet(name):
    return f"Hello, {name}!"

# Appel de la fonction
print(greet("Alice"))
```

Une fonction peut retourner plusieurs valeurs en utilisant des tuples.

```python
def get_name_and_age():
    name = "Alice"
    age = 30
    return name, age

# Appel de la fonction
name, age = get_name_and_age()
print(f"Name: {name}, Age: {age}")
```

Python permet de définir des fonctions qui acceptent plusieurs variables d'arguments.

```python
def sum_all(*numbers):
    return sum(numbers)

# Appel de la fonction
print(sum_all(1, 2, 3, 4))
```

Les fonctions peuvent avoir des paramètres par défaut et peuvent être appelées avec des arguments nommés.

```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

# Appel de la fonction
print(greet("Alice"))
print(greet("Bob", greeting="Hi"))
```

## Les modules

**Définition :** Un module est un fichier contenant du code Python que vous pouvez importer et réutiliser dans d'autres scripts.

Vous pouvez importer des modules en utilisant l'instruction **import**.
```python
import math

# Utilisation d'un module
print(math.sqrt(16))
```

Vous pouvez également importer des fonctions spécifiques à partir d'un module.
```python
from math import sqrt

# Utilisation d'une fonction importée
print(sqrt(25))
```

## Les packages
**Définition :** 
Un package est un répertoire contenant plusieurs modules et un fichier spécial **```__init__.py```**.

**Exemple de création de package**

1. Créez un répertoire nommé mypackage.
2. Ajoutez un fichier **```__init__.py```** dans mypackage.
3. Ajoutez un module mymodule.py dans mypackage.

Structure du package:
```markdown
mypackage/
    __init__.py
    mymodule.py
```

Contenu de **mymodule.py** 
```python 
def say_hello(name):
    return f"Hello, {name}!"
```

Utilisation du package:
```python
from mypackage.mymodule import say_hello

print(say_hello("Ousmane"))
```

## Programmation Orientée Objet

**Définition :** La programmation orientée objet (POO) est une façon de structurer le code en regroupant les données et les comportements connexes dans des objets. Voici les principaux concepts et techniques de la POO en Python.

**La conception de classe**

Une classe est un modèle pour créer des objets. Elle définit les attributs et les méthodes que les objets créés à partir de cette classe auront.
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        return f"Hello, my name is {self.name} and I am {self.age} years old."
```
Les attributs sont des variables qui appartiennent à une classe. Les méthodes sont des fonctions définies au sein d'une classe.

**Les constructeurs et les destructeurs**

Le constructeur ```__init__``` initialise les objets. Le destructeur ```__del__``` nettoie les objets avant qu'ils ne soient détruits.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age
        print(f"{self.name} is created.")

    def __del__(self):
        print(f"{self.name} is deleted.")
```

**L'encapsulation**

L'encapsulation cache les détails internes d'une classe. Les attributs sont généralement privés et accessibles via des méthodes publiques.

```python
class Person:
    def __init__(self, name, age):
        self._name = name
        self._age = age

    def get_name(self):
        return self._name

    def set_name(self, name):
        self._name = name

    def get_age(self):
        return self._age

    def set_age(self, age):
        if age < 0:
            raise ValueError("Age cannot be negative")
        self._age = age
```

Créer une instance de classe signifie créer un objet basé sur cette classe.

```python
person1 = Person("Ousmane", 30)
print(person1.greet())
```

Les variables de classe sont partagées par toutes les instances. Les méthodes de classe sont définies à l'aide du décorateur ```@classmethod```.

```python
class Person:
    population = 0

    def __init__(self, name, age):
        self.name = name
        self.age = age
        Person.population += 1

    @classmethod
    def get_population(cls):
        return cls.population
```

**L’héritage**

L'héritage permet à une classe de hériter les attributs et méthodes d'une autre classe.

```python
class Employee(Person):
    def __init__(self, name, age, employee_id):
        super().__init__(name, age)
        self.employee_id = employee_id

    def get_employee_id(self):
        return self.employee_id
```

**Le polymorphisme**

Le polymorphisme permet d'utiliser une interface commune pour différentes classes.

```python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow!"

def make_animal_speak(animal):
    return animal.speak()

dog = Dog()
cat = Cat()
print(make_animal_speak(dog))  # Output: Woof!
print(make_animal_speak(cat))  # Output: Meow!
```

**Les méthodes « magiques »**

Les méthodes magiques ou dunder methods sont des méthodes spéciales entourées de double underscores, comme ```__init__```, ```__str__```, etc.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def __str__(self):
        return f"{self.name}, {self.age}"

    def __eq__(self, other):
        return self.name == other.name and self.age == other.age
```

## Travaux Pratiques

### Système de Gestion de Bibliothèque

* Créez une classe Livre avec des attributs tels que titre, auteur, ISBN et disponibilité.
* Créez une classe Membre avec des attributs comme nom, identifiant de membre, et liste de livres empruntés.
* Implémentez une classe Bibliotheque qui permet d'ajouter des livres, d'enregistrer des membres, de prêter des livres et de retourner des livres.

### Système de Gestion d'École

* Créez une classe Personne avec des attributs comme nom et âge.
* Créez des classes Etudiant et Professeur qui héritent de Personne. Etudiant aura des attributs comme numéro d'étudiant et liste de cours inscrits, tandis que Professeur aura des attributs comme identifiant de professeur et liste de cours enseignés.
* Créez une classe Cours avec des attributs comme nom du cours et liste d'étudiants inscrits.
* Implémentez une classe Ecole qui permet de gérer l'inscription des étudiants aux cours, d'assigner des professeurs aux cours, etc.

### Gestion de Parc de Véhicules

- Créez une classe Vehicule avec des attributs tels que marque, modèle, année et disponibilité.
- Créez des sous-classes Voiture, Camion et Moto qui héritent de Vehicule, avec des attributs supplémentaires spécifiques à chaque type de véhicule.
- Implémentez une classe Parc qui permet d'ajouter des véhicules, de vérifier la disponibilité des véhicules et de louer des véhicules.

### Système de Réservation de Vols

- Créez une classe Vol avec des attributs comme numéro de vol, destination, date de départ, et nombre de sièges disponibles.
- Créez une classe Passager avec des attributs tels que nom, numéro de passeport, et liste de réservations.
- Implémentez une classe CompagnieAérienne qui permet d'ajouter des vols, d'enregistrer des passagers, de faire des réservations et d'annuler des réservations.

### Système de Gestion de Magasin

- Créez une classe Produit avec des attributs comme nom, prix, et quantité en stock.
- Créez une classe Client avec des attributs comme nom, identifiant de client, et historique des achats.
- Implémentez une classe Magasin qui permet d'ajouter des produits, de gérer les stocks, de traiter les achats et de maintenir l'historique des achats des clients.

### Système de Suivi de Projets

- Créez une classe Projet avec des attributs tels que nom du projet, date de début, date de fin, et liste des tâches.
- Créez une classe Tache avec des attributs comme description, date limite, et statut.
- Créez une classe Employe avec des attributs tels que nom, identifiant d'employé, et liste de tâches assignées.
- Implémentez une classe GestionnaireDeProjet qui permet de créer des projets, d'assigner des tâches aux employés, de mettre à jour le statut des tâches et de suivre l'avancement des projets.

### Exemple de Réalisation: Système de Gestion de Magasin

Classe Produit
```python
class Produit:
    def __init__(self, nom, prix, quantite):
        self.nom = nom
        self.prix = prix
        self.quantite = quantite

    def afficher_details(self):
        print(f"Produit: {self.nom}, Prix: {self.prix}, Quantité en stock: {self.quantite}")

    def ajuster_quantite(self, quantite):
        self.quantite += quantite

    def __str__(self):
        return f"{self.nom} - {self.prix}€ ({self.quantite} en stock)"
```

Classe Client
```python
class Client:
    def __init__(self, nom, identifiant):
        self.nom = nom
        self.identifiant = identifiant
        self.historique_achats = []

    def ajouter_achat(self, produit, quantite):
        self.historique_achats.append((produit, quantite))

    def afficher_historique(self):
        print(f"Historique d'achats de {self.nom}:")
        for produit, quantite in self.historique_achats:
            print(f"- {produit.nom}: {quantite} à {produit.prix}€ chacun")

    def __str__(self):
        return f"Client: {self.nom} (ID: {self.identifiant})"
```

Classe Magasin
```python
class Magasin:
    def __init__(self, nom):
        self.nom = nom
        self.produits = {}
        self.clients = {}

    def ajouter_produit(self, produit):
        if produit.nom in self.produits:
            self.produits[produit.nom].ajuster_quantite(produit.quantite)
        else:
            self.produits[produit.nom] = produit

    def enregistrer_client(self, client):
        self.clients[client.identifiant] = client

    def traiter_achat(self, identifiant_client, nom_produit, quantite):
        if identifiant_client in self.clients and nom_produit in self.produits:
            client = self.clients[identifiant_client]
            produit = self.produits[nom_produit]
            if produit.quantite >= quantite:
                produit.ajuster_quantite(-quantite)
                client.ajouter_achat(produit, quantite)
                print(f"Achat réussi : {quantite} x {produit.nom} pour {client.nom}")
            else:
                print("Quantité insuffisante en stock.")
        else:
            print("Client ou produit non trouvé.")

    def afficher_produits(self):
        print(f"Produits disponibles dans le magasin {self.nom}:")
        for produit in self.produits.values():
            produit.afficher_details()

    def __str__(self):
        return f"Magasin: {self.nom}"
```

Exemple d'utilisation
```python
# Création des produits
produit1 = Produit("Pain", 1.0, 50)
produit2 = Produit("Lait", 0.8, 30)

# Création du magasin
magasin = Magasin("Chez Nous")

# Ajout des produits au magasin
magasin.ajouter_produit(produit1)
magasin.ajouter_produit(produit2)

# Enregistrement d'un client
client1 = Client("Ousmane", "001")
magasin.enregistrer_client(client1)

# Achat d'un produit
magasin.traiter_achat("001", "Pain", 3)

# Affichage des détails
magasin.afficher_produits()
client1.afficher_historique()
```

Ces travaux pratiques vous permettront de mettre en œuvre les concepts de la programmation orientée objet tout en travaillant sur des projets réalistes. Vous pouvez ajuster et étendre ces exercices pour explorer davantage les capacités de Python.

