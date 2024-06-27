# 2. Installation de python

L'installation et la configuration de Python peuvent varier légèrement selon le système d'exploitation. Dans ce cours, nous verrons toutes les étapes pour installer Python sur Windows, macOS et Linux, en s'assurant que vous disposez d'un environnement de développement Python fonctionnel et prêt à l'emploi.

## Installation sur Windows

1. **Téléchargement :**
    * Rendez-vous sur le site officiel de Python à [python.org :octicons-link-external-16:](https://python.org){:target="_blank"}.
    * Positionnez le curseur de la souris sur l'onglet Downloads en haut de l'écran.
    * Téléchargez la dernière version de Python recommandée pour Windows.

2. **Exécution de l'installateur :**
    * Lancez l'exécutable téléchargé.
    * Lorsque la fenêtre apparaît, cliquez sur l'option **Customize installation**.
    * Cliquez sur le bouton **Next**
    * Assurez-vous de cocher la case "Add Python 3.x to PATH" pour ajouter Python à votre variable d'environnement PATH.
    * Cliquez sur "Install Now".

3. **Vérification de l'installation:**
    * Ouvrez le Command Prompt (cmd) et tapez ```python --version``` pour confirmer que Python est correctement installé.

## Installation sur macOS
1. **Téléchargement :**
    * Rendez-vous sur le site officiel de Python à [python.org :octicons-link-external-16:](https://python.org){:target="_blank"}.
    * Positionnez le curseur de la souris sur l'onglet Downloads en haut de l'écran.
    * Téléchargez la dernière version de Python recommandée pour macOS.

2. **Exécution de l'installateur :**
    * Lancez l'exécutable téléchargé.
    * Lorsque la fenêtre apparaît, cliquez sur le bouton **Continuer**.
    * Cliquez sur le bouton **Accepter** pour poursuivre l'installation du logiciel, vous devez accepter les termes du contrat de licence du logiciel.
    * Cliquez sur le bouton **Installer**, parfois la saisie d'un mot de passe est nécessaire pour autoriser l'installation.

3. **Vérification de l'installation:**
    * Ouvrez le terminal et tapez ```python --version``` pour confirmer que Python est correctement installé.
  

## Installation sur Linux
1. Installation sur Ubuntu/Debian:
   - Ouvrez un terminal et mettez à jour votre gestionnaire de paquets : ```$sudo apt-get update && sudo apt upgrade```.
   - Installez Python avec : ```sudo apt-get install python3```.
   - Une fois python installer, tapez la commande ```exit()``` pour sortir de l'interpréteur.

2. Installation sur Fedora/Red Hat:
   - Ouvrez un terminal et tapez : sudo dnf install python3.

3. Vérification de l'installation:
   - Dans le terminal, tapez python3 --version pour confirmer l'installation.


