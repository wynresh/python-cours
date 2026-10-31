# Python-cours

## REPL pyton

```bash
python3

>>> 10
10
>>> 10 + 10
20
```

## OPERATEURS ARITHMETIQUES


|Operation|Nom                  |Exemple     |
|---------|---------------------|------------|
|    +	  | Ajout	            | 2 + 2      |
|    –	  | Soustraction        | 3 – 1      |
|    *	  | Multiplication      | 5 * 3      |
|    /	  | Division	        | 5/2        |
|    %	  | Modulo	            | 5 % 2      |
|    //   |	Division des étages	| 9 // 2     |
|    **	  | Exponentiel	        | 2 ** 4     |

### Exemples

```python
>>> 2 + 3 * 3
11
>>> (2 + 3) * 3
15
>>> 1 + 2 ** 2
5
>>> 2 / 2 * 8
8.0
```

## LES VARIABLES

### Qu'est-ce qu'une variable Python ?

Commençons par définir plus formellement ce qu'est une variable :

#### Variable

Une variable sert à stocker des informations qui pourront être consultées ultérieurement.

Une variable sert à stocker le résultat d'un calcul. Autrement dit, on peut assigner ce résultat à une variable. 
On peut créer un nombre illimité de variables ; 
il suffit de leur donner des noms uniques.

### Déclarer une variable Python

```python
>>> result = 3 * 5
>>> result
15
```

### Nommage des variables

En règle générale, choisissez toujours un nom de variable qui décrit au mieux son contenu. Cette pratique rend votre code plus lisible et plus facile à comprendre. Si nous calculions ici, par exemple, le prix total d'un panier d'achat, un bon nom serait `shopping_cart_total`.

### Utilisation de variables dans les expressions

```python
>>> 4 * result
60
>>> result - result
0
>>> _
```

### Chaînes de caractères en Python : manipulation de texte

En termes plus simples, une chaîne de caractères est un fragment de texte. Les chaînes de caractères ne sont pas propres à Python ; c’est un terme courant en informatique et il a la même signification dans la plupart des autres langages. Maintenant que nous savons ce qu’est une chaîne de caractères, nous allons voir comment en créer une.

```python
>>> 'Hello, World'
'Hello, World'
>>> 'a' + 'b'
'ab'
>>> 'ab' * 4
'abababab'
>>> 'a' - 'b'
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: unsupported operand type(s) for -: 'str' and 'str'
>>> mystring = 'It\'s an escaped quote!'
>>> mystring
"It's an escaped quote!"
```

### Chaînes multilignes

```python
>>> """This is line 1,
... this is line 2,
... this is line 3."""
'This is line 1,\nthis is line 2,\nthis is line 3.'
```

| Séquence échappée	| Que fait-il ?
|-------------------|---------------
| \n	            | Un saut de ligne (les sauts de ligne sont générés avec la touche Entrée). Passe à la ligne suivante.
| \r	            | Retour chariot : vous ramène au début de la ligne, sans passer à la ligne suivante.
| \t	            | Un caractère de tabulation
| \\	            | Le caractère barre oblique lui-même : puisqu’il sert de point de départ aux séquences d’échappement, il faut également l’échapper. Python est assez tolérant si vous oubliez de l’échapper.

### Opérations sur les chaînes de caractères

```python
>>> mystring = "Hello world"
>>> mystring.
mystring.capitalize(    mystring.find(          mystring.isdecimal(     mystring.istitle(       mystring.partition(     mystring.rstrip(        mystring.translate(
mystring.casefold(      mystring.format(        mystring.isdigit(       mystring.isupper(       mystring.replace(       mystring.split(         mystring.upper(
mystring.center(        mystring.format_map(    mystring.isidentifier(  mystring.join(          mystring.rfind(         mystring.splitlines(    mystring.zfill(
mystring.count(         mystring.index(         mystring.islower(       mystring.ljust(         mystring.rindex(        mystring.startswith(
mystring.encode(        mystring.isalnum(       mystring.isnumeric(     mystring.lower(         mystring.rjust(         mystring.strip(
mystring.endswith(      mystring.isalpha(       mystring.isprintable(   mystring.lstrip(        mystring.rpartition(    mystring.swapcase(
mystring.expandtabs(    mystring.isascii(       mystring.isspace(       mystring.maketrans(     mystring.rsplit(        mystring.title(

>>> mystring.lower()
'hello world'
>>> mystring.upper()
'HELLO WORLD'

# Separation
>>> 'Hello \t\n there,\t\t\t stranger.'.split()
['Hello', 'there,', 'stranger.']
'Hello world'.split(' ')
['Hello', 'world']

# Remplacer 
'>>> 'Hello world'.replace('H', 'h')
'hello world'
>>> 'Hello world'.replace('l', '_')
'He__o wor_d'
>>> 'Hello world'.replace('world', 'readers')
'Hello readers'
>>> 'Hello world'.replace('H', 'h')
'hello world'
>>> 'Hello world'.replace('l', '_')
'He__o wor_d'
>>> 'Hello world'.replace('world', 'readers')
'Hello readers'

# découpage
>>> mystring = 'Hello world'
>>> mystring[2]
'l'
>>> mystring[0]
'H'

# slicing -mystring[start:stop:step_size]
>>> mystring = 'Hello world'
>>> mystring[::-1]
'dlrow olleH'
```

### Formatage de chaînes de caractères en Python avec les f-strings

```python
>>> my_age = 40
>>> f'My age is {my_age}'
My age is 40
>>> f'3 + 4 = {3+4}'
'3 + 4 = 7'
>>> my_age = 40
>>> f'My age is, unfortunately, not {my_age-8}'
'My age is, unfortunately, not 32'
```

### Qu'est-ce qu'une fonction ?

Pour l'instant, il suffit de savoir qu'une fonction est un objet que l'on peut appeler. Elle accomplit une tâche spécifique et son nom est souvent explicite. Les fonctions acceptent généralement des arguments, qu'elles utilisent pour réaliser leur tâche.

```python
print(1)
print('Some text')
print('A tab:\t and some text')
print()
print('This is my age:', 39)
```

### Programmation booléenne et conditionnelle en Python : if… else

#### Qu'est-ce qu'un booléen ?

Commençons par une définition :

Un booléen est le type de données le plus simple ; il est soit vrai,  True soit faux  False.
En informatique, les booléens sont très utilisés. Cela est lié au fonctionnement interne des ordinateurs. De nombreuses opérations informatiques se résument à un simple « vrai ou faux ». Il est important de noter qu'en Python, une valeur booléenne commence par une majuscule : `true`  True ou `false`  False. Ceci contraste avec la plupart des autres langages de programmation, où la norme est la minuscule.

```python
>>> door_is_locked = True
>>> if door_is_locked:
...     print("Mum, open the door!")
...
Mum, open the door!
>>>_
```
