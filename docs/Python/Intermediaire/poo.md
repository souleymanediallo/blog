# Programmation orientée objet

## Définition :
La programmation orientée objet (POO) est un paradigme de programmation basé sur le concept d' `objets`, qui peut contenir des données et du code qui manipulent ces données. En Python, vous pouvez utiliser des techniques POO pour créer des classes et des objets, ce qui peut vous aider à structurer votre code et à le rendre plus réutilisable et maintenable.

### Définir une classe
une classe est un modèle qui définit les attributs et les comportements d'un groupe d'objets. Vous pouvez définir une classe en Python en utilisant le mot clé `class`, suivi du nom de la classe et de deux-points `:`. La définition de classe doit inclure une métode `__init__` appelée lorsqu'un objet est créé à partir de la classe. Cette méthode peut être utilisée pour définir les valeurs initiales des attributs de l'objet.

Voici un exemple de définition de classe pour une simple classe `Person`:

```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age
```

### Créer un objet
Pour créer un objet à partir d'une classe, vous pouvez utiliser le nom de la classe suivi de parenthèses et transmettre tous les arguments requis à la méthode `__init__`. Cela créera un nouvel objet avec les valeurs d'attribut spécifiées.

Voici un exemple de création d'un objet à partir de la Personclasse :
``` 
p = Person("John", 30)
print(p.name)  # prints "John"
print(p.age)   # prints 30
```

### Définir des méthodes
Une méthode est une fonction définie dans une classe et utilisée pour effectuer une action spécifique sur les données de l'objet. Vous pouvez définir une méthode en utilisant le mot-clé `def`, suivi du nom de la méthode et des arguments requis.

Voici un exemple de définition d'une méthode `greet()` pour la classe `Person` :
```
class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def greet(self):
    print(f"Hello, my name is {self.name} and I am {self.age} years old.")
```

### Héritage
L'héritage est un moyen de créer une nouvelle classe qui est une version modifiée d'une classe existante. La nouvelle classe est appelée la sous-classe et la classe existante est la superclasse. La sous-classe peut hériter des attributs et des méthodes de la superclasse et peut également avoir ses propres attributs et méthodes.

Voici un exemple de définition d'une sous-classe qui hérite de la classe `Person`:
```
class Student(Person):
  def __init__(self, name, age, student_id):
    super().__init__(name, age)
    self.student_id = student_id
```
