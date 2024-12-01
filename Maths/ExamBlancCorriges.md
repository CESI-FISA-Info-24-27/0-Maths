
## **Exercice 1 : Analyse combinatoire et probabilité conditionnelle**  
Dans une urne contenant 5 boules rouges, 4 boules bleues, et 3 boules vertes, un joueur tire successivement 3 boules sans remise. Quelle est la probabilité que les trois boules tirées soient de couleurs différentes ?  

<details>
<summary>Solution</summary>

### Étape 1 : Total des boules dans l’urne  
L’urne contient un total de \(5 + 4 + 3 = 12\) boules.

### Étape 2 : Probabilité de tirer des boules de couleurs différentes  
Pour que les trois boules tirées soient de couleurs différentes, nous devons analyser les probabilités successives :

1. La première boule peut être de n’importe quelle couleur.
2. La deuxième boule doit être d’une couleur différente de la première.
3. La troisième boule doit être d’une couleur différente des deux premières.

#### Première boule :  
La probabilité de tirer la première boule est \(1\), car tout tirage est valide.

#### Deuxième boule :  
Après avoir tiré une première boule, il reste \(12 - 1 = 11\) boules dans l’urne. Les boules restantes qui sont d’une couleur différente de la première représentent \(8\) boules sur les \(11\) restantes (si la première couleur compte \(4\) boules).

La probabilité de tirer une deuxième boule de couleur différente est donc :

$$
P(\text{2ème différente}) = \frac{8}{11}.
$$

#### Troisième boule :  
Après avoir tiré deux boules, il reste \(12 - 2 = 10\) boules dans l’urne. Les boules restantes qui sont d’une couleur différente des deux premières représentent \(6\) boules.

La probabilité de tirer une troisième boule de couleur différente est donc :

$$
P(\text{3ème différente}) = \frac{6}{10}.
$$

### Étape 3 : Calcul de la probabilité totale  
La probabilité totale est donnée par :

$$
P(\text{3 couleurs différentes}) = P(\text{1ère boule}) \cdot P(\text{2ème différente}) \cdot P(\text{3ème différente}).
$$

En remplaçant :

$$
P(\text{3 couleurs différentes}) = 1 \cdot \frac{8}{11} \cdot \frac{6}{10}.
$$

Simplifions :

$$
P(\text{3 couleurs différentes}) = \frac{8 \cdot 6}{11 \cdot 10} = \frac{48}{110} = \frac{24}{55}.
$$

### Résultat final :  
La probabilité que les trois boules tirées soient de couleurs différentes est :

$$
P = \frac{24}{55} \approx 0.436 \, (43,6\%).
$$
</details>

---

## **Exercice 2 : Loi normale avec approximation**  
Dans un tournoi, les scores des joueurs suivent une loi normale avec une moyenne de 60 et un écart-type de 12. Quelle est la probabilité qu’un joueur obtienne un score entre 50 et 75 ?

<details>
<summary>Solution</summary>

### Étape 1 : Transformation en \(Z\)-scores  
Pour transformer les bornes \(x = 50\) et \(x = 75\) en \(Z\)-scores, on utilise la formule :

$$
Z = \frac{x - \mu}{\sigma}.
$$

Pour \(x = 50\) :

$$
Z_1 = \frac{50 - 60}{12} = \frac{-10}{12} = -0.833.
$$

Pour \(x = 75\) :

$$
Z_2 = \frac{75 - 60}{12} = \frac{15}{12} = 1.25.
$$

### Étape 2 : Utilisation des tables de la loi normale  
À l’aide des tables de la loi normale :  
- \(P(Z \leq -0.833) \approx 0.2023\).  
- \(P(Z \leq 1.25) \approx 0.8944\).

La probabilité de se trouver entre \(50\) et \(75\) est donnée par :

$$
P(50 \leq X \leq 75) = P(Z \leq 1.25) - P(Z \leq -0.833).
$$

En remplaçant :

$$
P(50 \leq X \leq 75) = 0.8944 - 0.2023 = 0.6921.
$$

### Résultat final :  
La probabilité qu’un joueur obtienne un score entre \(50\) et \(75\) est :

$$
P \approx 0.6921 \, (69,21\%).
$$
</details>

---

## **Exercice 3 : Régression linéaire et coefficient de corrélation**  
Les heures d’entraînement (\(x\)) et les scores obtenus (\(y\)) pour 5 joueurs sont données ci-dessous :  
| \(x\) | 1 | 2 | 3 | 4 | 5 |  
|------|---|---|---|---|---|  
| \(y\) | 10 | 12 | 15 | 20 | 25 |  

1. Déterminez l’équation de la droite de régression.  
2. Calculez le coefficient de corrélation \(r\).

<details>
<summary>Solution</summary>

### Étape 1 : Calcul des moyennes  
Pour \(x\) :

$$
\bar{x} = \frac{1 + 2 + 3 + 4 + 5}{5} = 3.
$$

Pour \(y\) :

$$
\bar{y} = \frac{10 + 12 + 15 + 20 + 25}{5} = 16.4.
$$

### Étape 2 : Calcul de la pente (\(a\))  
La pente est donnée par :

$$
a = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}.
$$

Pour le numérateur (\(\sum (x_i - \bar{x})(y_i - \bar{y})\)) :

$$
\sum (x_i - \bar{x})(y_i - \bar{y}) = (1-3)(10-16.4) + (2-3)(12-16.4) + \dots + (5-3)(25-16.4).
$$

$$
= 2 \cdot 6.4 + 1 \cdot 4.4 + 0 \cdot 0 + 1 \cdot 3.6 + 2 \cdot 8.6 = 42.8.
$$

Pour le dénominateur (\(\sum (x_i - \bar{x})^2\)) :

$$
\sum (x_i - \bar{x})^2 = (1-3)^2 + (2-3)^2 + (3-3)^2 + (4-3)^2 + (5-3)^2.
$$

$$
= 4 + 1 + 0 + 1 + 4 = 10.
$$

Donc :

$$
a = \frac{42.8}{10} = 4.28.
$$

### Étape 3 : Calcul de l’ordonnée à l’origine (\(b\))  
L’ordonnée est donnée par :

$$
b = \bar{y} - a\bar{x}.
$$

$$
b = 16.4 - 4.28 \cdot 3 = 3.56.
$$

L’équation de la droite de régression est donc :

$$
y = 4.28x + 3.56.
$$

### Étape 4 : Calcul du coefficient de corrélation (\(r\))  
La formule de \(r\) est :

$$
r = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 \cdot \sum (y_i - \bar{y})^2}}.
$$

Pour \(\sum (y_i - \bar{y})^2\) :

$$
\sum (y_i - \bar{y})^2 = (10-16.4)^2 + (12-16.4)^2 + \dots + (25-16.4)^2.
$$

$$
= 40.96 + 19.36 + 1.96 + 12.96 + 73.96 = 149.2.
$$

Donc :

$$
r = \frac{42.8}{\sqrt{10 \cdot 149.2}} = \frac{42.8}{38.65} = 0.90.
$$

### Résultat final :  
1. L’équation de la droite est \(y = 4.28x + 3.56\).  
2. Le coefficient de corrélation est \(r = 0.90\), indiquant une forte corrélation positive.


</details>

---

### **Exercice 4 : Loi normale (4 points)**  
Dans un tournoi, les scores des joueurs suivent une loi normale avec une moyenne de \( \mu = 75 \) et un écart-type de \( \sigma = 10 \).

1. Quelle est la probabilité qu’un joueur obtienne un score supérieur à \(85\) ?  
2. Quelle est la probabilité qu’un joueur obtienne un score entre \(70\) et \(90\) ?  

---

<details>
<summary>Solution</summary>

### Question 1 : Probabilité \(P(X > 85)\)

#### Étape 1 : Transformation en \(Z\)-score  
Pour transformer \(X = 85\) en un \(Z\)-score, nous utilisons la formule :  

$$
Z = \frac{X - \mu}{\sigma}.
$$

Pour \(X = 85\) :

$$
Z = \frac{85 - 75}{10} = \frac{10}{10} = 1.
$$

#### Étape 2 : Utilisation des tables de la loi normale  
À l’aide des tables de la loi normale, nous trouvons :

$$
P(Z \leq 1) \approx 0.8413.
$$

La probabilité que \(X > 85\) est le complémentaire :

$$
P(X > 85) = 1 - P(Z \leq 1) = 1 - 0.8413 = 0.1587.
$$

**Réponse 1 :** \(P(X > 85) \approx 15.87 \%.\)

---

### Question 2 : Probabilité \(P(70 \leq X \leq 90)\)

#### Étape 1 : Transformation en \(Z\)-scores  
Pour \(X = 70\) :

$$
Z_1 = \frac{70 - 75}{10} = \frac{-5}{10} = -0.5.
$$

Pour \(X = 90\) :

$$
Z_2 = \frac{90 - 75}{10} = \frac{15}{10} = 1.5.
$$

#### Étape 2 : Utilisation des tables de la loi normale  
D’après les tables de la loi normale :  
- \(P(Z \leq -0.5) \approx 0.3085\).  
- \(P(Z \leq 1.5) \approx 0.9332\).

La probabilité cherchée est la différence :

$$
P(70 \leq X \leq 90) = P(Z \leq 1.5) - P(Z \leq -0.5).
$$

En remplaçant :

$$
P(70 \leq X \leq 90) = 0.9332 - 0.3085 = 0.6247.
$$

**Réponse 2 :** \(P(70 \leq X \leq 90) \approx 62.47 \%.\)

</details>

---

### **Exercice 5 : Régression linéaire (4 points)**  
Les données suivantes représentent les heures d’entraînement (\(x\)) et les scores obtenus (\(y\)) pour 4 joueurs :  
| \(x\) | 1 | 2 | 3 | 4 |  
|------|---|---|---|---|  
| \(y\) | 12 | 15 | 19 | 25 |  

1. Déterminez l’équation de la droite de régression \(y = ax + b\).  
2. Prédisez le score pour un joueur qui s’entraîne 5 heures.

---

<details>
<summary>Solution</summary>

### Étape 1 : Calcul des moyennes

Pour \(x\) :

$$
\bar{x} = \frac{1 + 2 + 3 + 4}{4} = 2.5.
$$

Pour \(y\) :

$$
\bar{y} = \frac{12 + 15 + 19 + 25}{4} = 17.75.
$$

---

### Étape 2 : Calcul de la pente (\(a\))  

La pente \(a\) est donnée par la formule :

$$
a = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}.
$$

#### Numérateur (\(\sum (x_i - \bar{x})(y_i - \bar{y})\)) :  

$$
\sum (x_i - \bar{x})(y_i - \bar{y}) = (1-2.5)(12-17.75) + (2-2.5)(15-17.75) + \dots + (4-2.5)(25-17.75).
$$

Développons :

- Pour \(x_1 = 1\), \(y_1 = 12\) :

$$
(1-2.5)(12-17.75) = (-1.5)(-5.75) = 8.625.
$$

- Pour \(x_2 = 2\), \(y_2 = 15\) :

$$
(2-2.5)(15-17.75) = (-0.5)(-2.75) = 1.375.
$$

- Pour \(x_3 = 3\), \(y_3 = 19\) :

$$
(3-2.5)(19-17.75) = (0.5)(1.25) = 0.625.
$$

- Pour \(x_4 = 4\), \(y_4 = 25\) :

$$
(4-2.5)(25-17.75) = (1.5)(7.25) = 10.875.
$$

La somme est :

$$
\sum (x_i - \bar{x})(y_i - \bar{y}) = 8.625 + 1.375 + 0.625 + 10.875 = 21.5.
$$

#### Dénominateur (\(\sum (x_i - \bar{x})^2\)) :  

$$
\sum (x_i - \bar{x})^2 = (1-2.5)^2 + (2-2.5)^2 + \dots + (4-2.5)^2.
$$

Développons :

- Pour \(x_1 = 1\) :

$$
(1-2.5)^2 = (-1.5)^2 = 2.25.
$$

- Pour \(x_2 = 2\) :

$$
(2-2.5)^2 = (-0.5)^2 = 0.25.
$$

- Pour \(x_3 = 3\) :

$$
(3-2.5)^2 = (0.5)^2 = 0.25.
$$

- Pour \(x_4 = 4\) :

$$
(4-2.5)^2 = (1.5)^2 = 2.25.
$$

La somme est :

$$
\sum (x_i - \bar{x})^2 = 2.25 + 0.25 + 0.25 + 2.25 = 5.
$$

#### Calcul de \(a\) :  

$$
a = \frac{21.5}{5} = 4.3.
$$

---

### Étape 3 : Calcul de l’ordonnée à l’origine (\(b\))  

L’ordonnée \(b\) est donnée par :

$$
b = \bar{y} - a\bar{x}.
$$

En remplaçant :

$$
b = 17.75 - 4.3 \cdot 2.5 = 17.75 - 10.75 = 7.
$$

L’équation de la droite de régression est donc :

$$
y = 4.3x + 7.
$$

---

### Étape 4 : Prédiction pour \(x = 5\)  

En remplaçant \(x = 5\) dans l’équation :

$$
y = 4.3 \cdot 5 + 7 = 21.5 + 7 = 28.5.
$$

**Réponse finale :**  
1. L’équation de la droite est \(y = 4.3x + 7\).  
2. Pour 5 heures d’entraînement, le score prédit est \(28.5\).

</details>

---
