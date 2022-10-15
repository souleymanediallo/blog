# Projet N°1

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    `mkdocs.yml    # The configuration file.`
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
    merci beauc

## Project Pas
    >>> the_world_is_flat = True
    >>> if the_world_is_flat:
    ...     print("Be careful not to fall off!")
    ...
    Be careful not to fall <off!></off!>

Merci d'ecire ce sont

    >>> 17 / 3  # classic division returns a float
    5.666666666666667
    >>>
    >>> 17 // 3  # floor division discards the fractional part
    5
    >>> 17 % 3  # the % operator returns the remainder of the division
    2
    >>> 5 * 3 + 2  # floored quotient * divisor + remainder
    17

Dans l'exemple précédent, nous avons stocké un nombre entier (int) dans la variable x, mais il est tout à fait possible de stocker des floats, des chaînes de caractères (string ou str) ou de nombreux autres types de variable que nous verrons par la suite :

    >>> y = 3.14
    >>> y
    3.14
    >>> a = "bonjour"
    >>> a
    'bonjour'
    >>> b = 'salut'
    >>> b
    'salut'
    >>> c = """girafe"""
    >>> c
    'girafe'
    >>> d = '''lion'''
    >>> d
    'lion'

### Hello
```console
$ python main.py

---> 100%

Processed 100 things.
```

## Typer `progressbar`

You can use `typer.progressbar()` with a `with` statement, as in:

```Python hl_lines="8"
{!../docs_src/progressbar/tutorial003.py!}
```

!!! tip

```py linenums="1"
users = ["Camila", "Rick", "Morty"]
with typer.progressbar(users) as progress:
    for user in progress:
        typer.echo(user)
```

Merci pour ce code

``` py linenums="1"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```
Ajouter ce code

```py hl_lines="2 3"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```