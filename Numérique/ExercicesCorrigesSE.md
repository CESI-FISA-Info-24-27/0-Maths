# Exercices corrigés - Systemes d'exploitation

## **Partie 1 : Fonctionnement des ordinateurs**

### **Exercice 1 : Le rôle du processeur et de la mémoire**
Expliquez le rôle du processeur (CPU) et de la mémoire vive (RAM) dans l'exécution d'un programme. Illustrez avec un exemple simple de calcul d’une somme de deux nombres.

<details>
<summary>Solution</summary>

1. **Processeur (CPU)** :
   - Le processeur exécute les instructions du programme, comme les calculs, les comparaisons et le transfert de données.
   - Exemple : Pour $ a + b $, le CPU lit les valeurs de $a$ et $b$, exécute l'instruction "addition", et stocke le résultat.

2. **Mémoire vive (RAM)** :
   - La RAM stocke temporairement les données et instructions nécessaires à l'exécution du programme.
   - Exemple : Les valeurs de $a$ et $b$ sont chargées depuis le disque dans la RAM, puis le CPU y accède pour effectuer l'opération.

**Étapes de fonctionnement** :
1. Le programme est chargé en mémoire.
2. Le CPU lit l'instruction d'addition.
3. Le CPU récupère les valeurs depuis la RAM.
4. Le CPU calcule la somme et la stocke en RAM ou dans un registre temporaire.

**Illustration :**
Pour $ a = 3 $, $ b = 4 $, le CPU :
1. Charge $a$ et $b$ en RAM.
2. Exécute l'instruction : $ 3 + 4 = 7 $.
3. Renvoie $7$ au programme ou le stocke pour un usage futur.
</details>

---

### **Exercice 2 : Les différents types de mémoires**
Classez les mémoires suivantes en fonction de leur vitesse et expliquez leur rôle : Cache L1, Disque dur, RAM.

<details>
<summary>Solution</summary>

1. **Classification** par vitesse (du plus rapide au plus lent) :
   - **Cache L1** : Mémoire ultra-rapide intégrée au processeur.
   - **RAM** : Mémoire vive rapide, mais plus lente que le cache.
   - **Disque dur** : Stockage permanent, beaucoup plus lent.

2. **Rôles** :
   - **Cache L1** : Stocke les données les plus fréquemment utilisées par le CPU. Accès en quelques nanosecondes.
   - **RAM** : Stocke les données temporaires et les programmes en cours d'exécution. Accès en dizaines de nanosecondes.
   - **Disque dur** : Stocke les données à long terme. Accès en millisecondes.

**Exemple :**
Lors de l'exécution d'un programme :
1. Les instructions sont d'abord chargées depuis le disque dur vers la RAM.
2. Les instructions courantes sont copiées dans le cache L1 pour un accès rapide.
</details>

---

### **Exercice 3 : Le cycle d’instruction**
Décrivez les étapes du cycle d’instruction d’un processeur (fetch, decode, execute) et appliquez-le à une instruction "charger 5 dans le registre A".

<details>
<summary>Solution</summary>

1. **Fetch** (Récupération) :
   - Le CPU lit l'instruction "charger 5 dans le registre A" depuis la mémoire RAM.

2. **Decode** (Décodage) :
   - L'unité de contrôle du CPU interprète l'instruction pour déterminer :
     - L’opération : Charger une valeur.
     - Les opérandes : La valeur $5$ et le registre $A$.

3. **Execute** (Exécution) :
   - Le CPU exécute l'instruction :
     - Il place la valeur $5$ dans le registre $A$.

**Illustration :**
- Instruction en RAM : `LOAD A, 5`.
- Après exécution :
  - Registre $A = 5$.
</details>

---

Voici des exercices supplémentaires pour la **Partie 1 : Fonctionnement des ordinateurs**.

---

### **Exercice 4 : Ordonnancement des processus**
Un système d’exploitation utilise l’algorithme **Round Robin** avec un quantum de temps de 4 ms. Trois processus $P_1$, $P_2$, et $P_3$ arrivent respectivement à 0 ms, 1 ms, et 2 ms, avec des temps d’exécution nécessaires de 6 ms, 8 ms, et 12 ms. Quel est l’ordre d’exécution et le temps d’attente moyen des processus ?

<details>
<summary>Solution</summary>

1. **Algorithme Round Robin** :
   - Chaque processus obtient un temps de CPU égal au quantum, puis revient à la file si du temps est encore requis.

2. **Temps d’exécution** :
   - $P_1$ : 6 ms
   - $P_2$ : 8 ms
   - $P_3$ : 12 ms

3. **Exécution** :
   - Temps $t = 0$: $P_1$ (4 ms, reste 2 ms)
   - Temps $t = 4$: $P_2$ (4 ms, reste 4 ms)
   - Temps $t = 8$: $P_3$ (4 ms, reste 8 ms)
   - Temps $t = 12$: $P_1$ (2 ms, terminé)
   - Temps $t = 14$: $P_2$ (4 ms, terminé)
   - Temps $t = 18$: $P_3$ (8 ms, terminé)

4. **Temps d’attente** :
   - $P_1$ : $12 - 6 = 6$ ms.
   - $P_2$ : $18 - 8 = 10$ ms.
   - $P_3$ : $26 - 12 = 14$ ms.

5. **Temps moyen d’attente** :
   \[
   \text{Moyenne} = \frac{6 + 10 + 14}{3} = 10 \, \text{ms}.
   \]

**Réponse** :
- Ordre d’exécution : $P_1, P_2, P_3, P_1, P_2, P_3$.
- Temps d’attente moyen : $10 \, \text{ms}$.
</details>

---

### **Exercice 5 : Cycle de machine**
Un processeur fonctionne avec une fréquence de 2 GHz. Combien de cycles seront exécutés en une seconde ? Si une instruction prend en moyenne 4 cycles d’horloge, combien d’instructions sont exécutées par seconde ?

<details>
<summary>Solution</summary>

1. **Calcul des cycles** :
   - Fréquence = 2 GHz = $2 \times 10^9$ Hz.
   - Chaque cycle correspond à un battement d’horloge :
     \[
     \text{Cycles par seconde} = 2 \times 10^9 \, \text{cycles}.
     \]

2. **Calcul des instructions** :
   - Chaque instruction prend 4 cycles d’horloge.
   - Nombre d’instructions par seconde :
     \[
     \text{Instructions par seconde} = \frac{\text{Cycles par seconde}}{\text{Cycles par instruction}} = \frac{2 \times 10^9}{4} = 0.5 \times 10^9 = 500 \, \text{millions}.
     \]

**Réponse** :
- Cycles par seconde : $2 \times 10^9$.
- Instructions par seconde : $500 \, \text{millions}$.
</details>

---

### **Exercice 6 : Fragmentation mémoire**
Un système utilise une mémoire segmentée. Trois segments de mémoire contigus sont disponibles : $100$ KB, $300$ KB, et $200$ KB. Trois processus $P_1$, $P_2$, et $P_3$ demandent respectivement $90$ KB, $250$ KB, et $150$ KB. Attribuez les segments selon les stratégies **first-fit** et **best-fit**, et calculez la fragmentation externe dans chaque cas.

<details>
<summary>Solution</summary>

1. **First-fit** (première case suffisante) :
   - $P_1 (90 \, \text{KB})$ : Alloué à $100 \, \text{KB}$, reste $10 \, \text{KB}$.
   - $P_2 (250 \, \text{KB})$ : Alloué à $300 \, \text{KB}$, reste $50 \, \text{KB}$.
   - $P_3 (150 \, \text{KB})$ : Alloué à $200 \, \text{KB}$, reste $50 \, \text{KB}$.

   **Fragmentation externe** :
   - Fragments inutilisés : $10 + 50 + 50 = 110 \, \text{KB}$.

2. **Best-fit** (meilleure adaptation) :
   - $P_1 (90 \, \text{KB})$ : Alloué à $100 \, \text{KB}$, reste $10 \, \text{KB}$.
   - $P_2 (250 \, \text{KB})$ : Alloué à $300 \, \text{KB}$, reste $50 \, \text{KB}$.
   - $P_3 (150 \, \text{KB})$ : Alloué à $200 \, \text{KB}$, reste $50 \, \text{KB}$.

   **Fragmentation externe** :
   - Fragments inutilisés : $10 + 50 + 50 = 110 \, \text{KB}$.

**Réponse** :
- Stratégies first-fit et best-fit attribuent la mémoire de manière identique.
- Fragmentation externe totale : $110 \, \text{KB}$.
</details>

---

### **Exercice 7 : Mémoire virtuelle**
Un système d’exploitation utilise une mémoire virtuelle avec une taille de page de 4 KB. Un programme demande 20 KB de mémoire. Combien de pages seront allouées ? Si la table des pages stocke une entrée par page, combien d’entrées sont nécessaires ?

<details>
<summary>Solution</summary>

1. **Nombre de pages nécessaires** :
   - Taille totale demandée : $20 \, \text{KB}$.
   - Taille d’une page : $4 \, \text{KB}$.
   - Nombre de pages :
     \[
     \text{Pages} = \frac{\text{Taille totale}}{\text{Taille de page}} = \frac{20}{4} = 5 \, \text{pages}.
     \]

2. **Entrées de la table des pages** :
   - Chaque page nécessite une entrée.
   - Total : $5 \, \text{entrées}$.

**Réponse** :
- Pages nécessaires : $5$.
- Entrées dans la table des pages : $5$.
</details>

---

### **Exercice 8 : Cache L1 et L2**
Un processeur a deux niveaux de cache : L1 avec une latence de 2 cycles et L2 avec une latence de 10 cycles. Le taux de hit est de $90\%$ pour L1 et $70\%$ pour L2 (en cas de miss dans L1). Quelle est la latence moyenne d'accès au cache ?

<details>
<summary>Solution</summary>

1. **Latence moyenne** :
   - Hit dans L1 ($90\%$) : $2 \, \text{cycles}$.
   - Miss dans L1, mais hit dans L2 ($10\% \times 70\%$) : $10 \, \text{cycles}$.
   - Miss dans L2 ($10\% \times 30\%$) : Ignoré pour simplification.

   Latence moyenne :
   \[
   \text{Latence} = (0.9 \times 2) + (0.1 \times 0.7 \times 10) = 1.8 + 0.7 = 2.5 \, \text{cycles}.
   \]

**Réponse** :
- Latence moyenne : $2.5 \, \text{cycles}$.
</details>

---


## **Partie 2 : Paradigmes de programmation**

### **Exercice 1 : Paradigmes impératif et déclaratif**
Expliquez la différence entre les paradigmes **impératif** et **déclaratif** à l’aide d’un exemple de calcul de la somme des nombres d’une liste.

<details>
<summary>Solution</summary>

1. **Impératif** :
   - Le programme décrit **comment** effectuer le calcul en détaillant chaque étape.
   - Exemple (Python) :
     ```python
     liste = [1, 2, 3, 4]
     somme = 0
     for nombre in liste:
         somme += nombre
     print(somme)  # Résultat : 10
     ```

2. **Déclaratif** :
   - Le programme décrit **quoi** faire, sans détailler les étapes.
   - Exemple (SQL) :
     ```sql
     SELECT SUM(nombre) FROM table_nombres;
     ```
   - En Python, une approche déclarative :
     ```python
     liste = [1, 2, 3, 4]
     somme = sum(liste)
     print(somme)  # Résultat : 10
     ```

**Résumé** :
- **Impératif** : Spécifie chaque étape du calcul.
- **Déclaratif** : Exprime le résultat souhaité sans détailler la procédure.
</details>

---

### **Exercice 2 : Programmation orientée objet (POO)**
Créez une classe `Rectangle` en Python avec des méthodes pour calculer l’aire et le périmètre. Instanciez un rectangle de dimensions $5 \times 3$ et affichez ses propriétés.

<details>
<summary>Solution</summary>

**Code en Python** :
```python
class Rectangle:
    def __init__(self, largeur, hauteur):
        self.largeur = largeur
        self.hauteur = hauteur

    def aire(self):
        return self.largeur * self.hauteur

    def perimetre(self):
        return 2 * (self.largeur + self.hauteur)

# Instanciation
rect = Rectangle(5, 3)

# Calculs
print(f"Aire : {rect.aire()}")         # Aire : 15
print(f"Périmètre : {rect.perimetre()}")  # Périmètre : 16
```

1. **Instanciation** :
   - L’objet `rect` est une instance de la classe `Rectangle`.
   - $ \text{largeur} = 5 $, $ \text{hauteur} = 3 $.

2. **Méthodes** :
   - `aire` calcule $5 \times 3 = 15$.
   - `perimetre` calcule $2 \times (5 + 3) = 16$.

**Explication** :
La POO permet de regrouper les propriétés (largeur, hauteur) et les comportements (aire, périmètre) dans une structure réutilisable.
</details>

---

### **Exercice 3 : Programmation fonctionnelle**
Écrivez une fonction Python utilisant un paradigme fonctionnel pour filtrer les nombres pairs d’une liste et les élever au carré.

<details>
<summary>Solution</summary>

**Code en Python** :
```python
# Liste initiale
liste = [1, 2, 3, 4, 5, 6]

# Filtrage et transformation
resultat = list(map(lambda x: x**2, filter(lambda x: x % 2 == 0, liste)))

print(resultat)  # Résultat : [4, 16, 36]
```

1. **Filtrage** :
   - La fonction `filter` sélectionne les nombres pairs :
     ```python
     filter(lambda x: x % 2 == 0, liste)
     ```

2. **Transformation** :
   - La fonction `map` élève chaque nombre pair au carré :
     ```python
     map(lambda x: x**2, ...)
     ```

3. **Résultat** :
   - Les nombres pairs ($2, 4, 6$) sont transformés en $ [4, 16, 36] $.

**Explication** :
- Le paradigme fonctionnel évite les boucles explicites en utilisant des fonctions comme `map` et `filter`.
</details>

---

### **Exercice 4 : Comparaison entre paradigmes**
Comparez l’approche orientée objet et fonctionnelle pour gérer une liste de rectangles (calcul des aires).

<details>
<summary>Solution</summary>

1. **Approche orientée objet** :
   ```python
   class Rectangle:
       def __init__(self, largeur, hauteur):
           self.largeur = largeur
           self.hauteur = hauteur

       def aire(self):
           return self.largeur * self.hauteur

   # Liste de rectangles
   rectangles = [Rectangle(5, 3), Rectangle(2, 4), Rectangle(3, 3)]
   aires = [rect.aire() for rect in rectangles]

   print(aires)  # Résultat : [15, 8, 9]
   ```

2. **Approche fonctionnelle** :
   ```python
   rectangles = [(5, 3), (2, 4), (3, 3)]
   aires = list(map(lambda dims: dims[0] * dims[1], rectangles))

   print(aires)  # Résultat : [15, 8, 9]
   ```

**Comparaison** :
- **POO** :
  - Modélise les rectangles avec des objets.
  - Utilise des méthodes associées à chaque objet.
  - Avantages : Clarté pour des structures complexes, extensibilité.
- **Fonctionnelle** :
  - Utilise des tuples simples pour représenter les dimensions.
  - Avantages : Code plus concis pour des tâches simples.

**Conclusion** :
- La POO est préférable pour des applications complexes.
- Le fonctionnel est idéal pour des tâches courtes et répétitives.
</details>