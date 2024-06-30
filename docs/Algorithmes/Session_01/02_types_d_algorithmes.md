# 2. Types d'algorithmes

Les quatre principaux types d'algorithmes sont : la recherche, le tri, le calcul et la collecte.

## 2.1 Principaux types d'algorithmes

### 1. Algorithmes de recherche :

- **Recherche linéaire :** Parcourt chaque élément de la liste jusqu'à trouver l'élément recherché.
- **Recherche binaire :** Recherche un élément dans une liste triée en divisant la liste en deux à chaque étape.

### 2. Algorithmes de tri :

- **Tri à bulles (Bubble Sort) :** Compare et échange les éléments adjacents pour les placer dans l'ordre.
- **Tri par insertion (Insertion Sort) :** Insère chaque élément dans sa position correcte par rapport aux éléments déjà triés.
- **Tri rapide (Quick Sort) :** Utilise la méthode de partition pour diviser et trier les sous-listes.
- **Tri fusion (Merge Sort) :** Divise la liste en sous-listes, les trie et les fusionne.

### 3. Algorithmes de calcul :

Ces algorithmes effectuent des opérations mathématiques complexes. Par exemple, trouver la moyenne, la médiane, ou l'écart-type d'une liste de nombres.

### 4. Algorithmes de collecte :

Ces algorithmes collectent et agrègent des données selon des critères spécifiques. Par exemple, regrouper les contacts par ville ou par domaine professionnel.

## 2.2 Utilisation pour organiser une liste de contacts

**Exemple de liste de contacts**
```
contacts = [
    {"nom": "Dupont", "prenom": "Jean", "telephone": "1234567890"},
    {"nom": "Martin", "prenom": "Sophie", "telephone": "0987654321"},
    {"nom": "Durand", "prenom": "Luc", "telephone": "1122334455"}
]
```

**Algorithmes de tri**

Pour trier les contacts par nom de famille :
```
def tri_par_nom(contact):
    return contact['nom']

contacts_trie = sorted(contacts, key=tri_par_nom)
print(contacts_trie)
```

**Algorithmes de recherche**

Pour rechercher un contact par nom :
```
def recherche_par_nom(nom, contacts):
    for contact in contacts:
        if contact['nom'] == nom:
            return contact
    return None

contact = recherche_par_nom("Martin", contacts)
print(contact)
```

Pour une recherche binaire (requiert que la liste soit triée) :
```
def recherche_binaire(nom, contacts):
    contacts_trie = sorted(contacts, key=lambda x: x['nom'])
    gauche, droite = 0, len(contacts_trie) - 1
    while gauche <= droite:
        milieu = (gauche + droite) // 2
        if contacts_trie[milieu]['nom'] == nom:
            return contacts_trie[milieu]
        elif contacts_trie[milieu]['nom'] < nom:
            gauche = milieu + 1
        else:
            droite = milieu - 1
    return None

contact = recherche_binaire("Martin", contacts)
print(contact)
```

**Algorithmes de calcul**

Pour calculer la longueur moyenne des prénoms des contacts :
```
def moyenne_longueur_prenom(contacts):
    total_longueur = sum(len(contact['prenom']) for contact in contacts)
    return total_longueur / len(contacts)

moyenne = moyenne_longueur_prenom(contacts)
print(moyenne)
```

**Algorithmes de collecte**

Pour regrouper les contacts par la première lettre de leur nom :

```
from collections import defaultdict

def regrouper_par_premiere_lettre(contacts):
    groupe = defaultdict(list)
    for contact in contacts:
        premiere_lettre = contact['nom'][0].upper()
        groupe[premiere_lettre].append(contact)
    return groupe

groupe_contacts = regrouper_par_premiere_lettre(contacts)
for lettre, groupe in groupe_contacts.items():
    print(f"{lettre}: {groupe}")
```

Ces exemples montrent comment différents types d'algorithmes peuvent être utilisés pour organiser, rechercher, trier et analyser une liste de contacts, rendant les données plus utilisables et accessibles.