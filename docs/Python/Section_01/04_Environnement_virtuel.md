# 4. Environnement virtuel

En utilisant l'outil pycharm et créer un nouveau projet, notre environnement virutel a été crée automatiquement. Et c'est quoi un environnement virtuel ? 

**Définition :** Un environnement virtuel en Python est un espace isolé où vous pouvez installer des paquets Python spécifiques à un projet sans affecter les autres projets ou les paquets installés globalement sur votre système. Cela permet de gérer différentes versions de paquets et d’éviter les conflits de dépendances entre projets.

## Utilité d'un Environnement Virtuel

1. **Isolation des Dépendances :** Chaque projet peut avoir ses propres dépendances spécifiques. Un environnement virtuel empêche les conflits de version de paquets entre projets.
2. **Reproductibilité :** Facilite la reproduction de l’environnement de développement sur d’autres machines en utilisant des fichiers de configuration comme requirements.txt.
3. **Gestion de Versions :** Permet d’utiliser différentes versions d’un même paquet dans différents projets.

## Installation d'un Environnement Virtuel
Pour créer et utiliser un environnement virtuel en Python, vous pouvez utiliser le module `venv` (inclus dans Python 3.3 et versions ultérieures) ou `virtualenv` (disponible pour les versions antérieures et offrant plus de fonctionnalités).

### Utilisation de venv

1. **Installation :** venv est inclus par défaut dans Python 3.3 et versions ultérieures, donc aucune installation supplémentaire n’est nécessaire.

2. **Création d'un Environnement Virtuel :**
`python -m venv venv`

3. Activation de l’Environnement Virtuel :
    - Sur Windows :
    `.\venv\Scripts\activate`
    - Sur macOS et Linux :
    `source venv/bin/activate`

4. Désactivation de l’Environnement Virtuel :
   `deactivate`

### Utilisation de virtualenv
1. **Installation :** 
`pip install virtualenv`

2. **Création d'un Environnement Virtuel :**
`virtualenv venv`

1. Activation de l’Environnement Virtuel :
    - Sur Windows :
    `.\venv\Scripts\activate`
    - Sur macOS et Linux :
    `source venv/bin/activate`

2. Désactivation de l’Environnement Virtuel :
   `deactivate`

### Exemple Pratique
1. **Créer un Environnement Virtuel :** 
`python -m venv venv`

2. **Activer l’Environnement Virtuel :**
    - Sur Windows :
    `.\venv\Scripts\activate`
    - Sur macOS et Linux :
    `source venv/bin/activate`

3. Installer des Paquets :
   `pip install requests flask`

4. Générer un Fichier de Dépendances :
   `pip freeze > requirements.txt`

5. Désactiver l’Environnement Virtuel :
   `deactivate`

## En résumé
Ces étapes vous permettent de travailler dans un environnement Python isolé, ce qui améliore la gestion et la maintenance de vos projets Python.