# Python

## - Variables

`nom_de_variable = valeur`

### Type

```python
int c = 0
float c = 1.3
str c = "salut"
boolean c = True or False
```

#### * Chaine de caracteres

**'text'**<br>
**"text"**<br>
**"""text"""** : Permet de ne pas echaper le texte + fait de vrai retour a la ligne<br>
**\** : caractere d'echapement

##### Propriete


```python
chaine2 = "salut"

chaine2[-1] == "t" # Dernier char de lq chaine
chaine2[2:5] == "lut" # Du char 2 au 5eme (commence a 0)
chaine2[2:] == "lut" # Du char 2 jusque fin
chaine2[:2] == "sa" # Du debut jusaue 2eme char
```

#### * Listes

```python
ma_liste = list()
ma_liste[0] = "str"
```

#### * Tuple

les tuple sont non modifiable apres creation

tuple = (1,)
tuple = (1, 2, 3, "Viva l'algerie")


#### * Dictionnaire
 = liste pouvant contenir des class avec clef/valeur


#### * Stocker une fonction

```python
# Creation de la fonction
def fonction(~param1 ~var):
  ~code

# Stoque la fonction dans la variable
variable = fonction

#Execution de la fonction
variable("test")
```

## Mots clefs python

<table>
<tbody>
<tr>
  <td>and</td>
  <td>del</td>
  <td>from</td>
  <td>none</td>
</tr><tr>
  <td>true</td>
  <td>as</td>
  <td>elif</td>
  <td>global</td>
</tr><tr>
  <td>nonlocal</td>
  <td>try</td>
  <td>assert</td>
  <td>else</td>
</tr><tr>
  <td>if</td>
  <td>not</td>
  <td>while</td>
  <td>break</td>
</tr><tr>
  <td>except</td>
  <td>import</td>
  <td>or</td>
  <td>with</td>
</tr><tr>
  <td>class</td>
  <td>false</td>
  <td>in</td>
  <td>pass</td>
</tr><tr>
  <td>yield</td>
  <td>continue</td>
  <td>finally</td>
  <td>is</td>
</tr><tr>
  <td>raise</td>
  <td>def</td>
  <td>for</td>
  <td>lamdba</td>
</tr><tr>
  <td>return</td>
</tr>
</table>

### Definition de mots clefs

#### with

**Permet de prevenir une exeption**, il prend l'objet et appelle son destructeur en cas d'exeption

** exemple ** :
Dans le cas d'une exeption le fichier sera quand meme ferme
```python
with open("test", "r") as variable
variable.read()
```

## Operateurs

### Operations

add: **+**<br>
sub: **-**<br>
equal: **=**<br>
mult: *** * *** <br>
div: **/**<br>
div_int: **//**<br>
modulo: **%**<br>

### Attribution

add_equal: **+=**<br>
sub_equal: **-=**<br>
mult_equal:** \*= **<br>
div_equal: ** /=** <br>

### Comparaison

inferior: **<**<br>
inferior or equal: **<=**<br>
superior: **\>**<br>
superior or equal: **>=**<br>
equal: **==**<br>
different: **!=**<br>
not: **!**/**not**<br>
Egalite des variable: **is**<br>

## Tests de valeur

### Conditions

```python
if (test and test or test)
   if (test):
      	    	~code
elif (not test):
	~code
else:
	~code
```

### Boucles

```python
while (test):
      ~code
```

```python
for ~value in ~tableau:
    ~code
```

```python
for ~key, ~value in ~tableau
    ~code
```

**break**: Casse la boucle<br>
**continue**: Retourne a la condition de la boucle

## Declaration

### Fonction

```python
def ~nom_fonction(~param1, ~param2 = ~default_value, ~param3 = ~default_value2):
    ~code
    return ~valeur


~valeur_retour = ~nomfonction(~param1, ~param3 = ~value)
```

Fonction a **param indeterminee** dans **tuple**

```python
def ~nom(*~param):
    # param sera alors un tuple
    type(~param[0])
```

Fonction a **param indeterminee** dans **dictionnaire**

```python
def ~nom(**~param):
    # param sera alors un dictionnaire
    type(~param["0"])
```

### Fonction lambda

Il faut **stocker** la fonction **dans une variable**

```python
~function_var = lambda ~param, ~param, ~param : ~return_value

~result = ~function_var(12, 12, 12)
```

### Class
```python
class ~nomDeClass:
      # Constructeur
      def __init__(self):
      	  ~code
          self.variable = "Variable publique"

      def ~fonction(self):
          self.~variable = "test"
```

## Modules

**Importation simple**
```python
import module

module.fonction()
```

**Importation avec renommage**
```python
import module2 as m

m.fonction()
```

**Importation d'une fonction specifique**
```python
from module import function

fonction()
```

## Configuration fichier

**Premiere ligne** d'un script python
```python
#!/Chemin/Vers/Interpreteur/Python
```

**Encodage** du script
```python
# -*-coding:ENCODAGE -*

# -*-coding:utf-8 -*
```

**Test execution du fichier principal**:

```python
if __name__ == __main__:
   	    True
else:
	    False
```

**Package**:

creer dans le dossier courant au package un fichier ** \__init__.py **
qui contient tous les imports


## Exeption

### Example

```python
try:
	~Test d'instruction(s)
except ~type_de_l_exception:
       ~Traitement en cas d'erreur
except ~type_de_l_exception:
       pass
       # Fait comme si il n'y avait pas eu d'erreur
finally:
	~Instruction(s) exécutée(s) qu'il y ait eu des erreurs ou non
else:
	~Instruction(s) si il n'y a pas d'erreur
```

### Assert

Comme un if sauf que **si le if n'est pas true, il lance une exeption**
```python
assert ~variable == 5
```


### Raise

**Lance une exeption**
```python
raise ~TypeDeLexeption("~Message")
```

## Sauvegarde et chargement de donnes

**Avant toute chose** il faut utiliser pickle
```python
import pickle
```

### Sauvegarde
```python
open(~nom_fichier)
~variable = pickle.Pickler(fichier)
~variable.dump(~valeur_a_sauvegarder)
```

### Chargement
```python
variable = pickle.Pickler(fichier)
variable.dump(valeur_a_sauvegarder)
```
