# Exercices Corrigés de Statistiques et Probabilités

## **Thème : Probabilités**

### **Exercice 1 : Probabilité simple**  
Un joueur lance un dé à 6 faces. Quelle est la probabilité d’obtenir un nombre supérieur ou égal à 4 ?

<details>
<summary>Solution</summary>
Les nombres supérieurs ou égaux à 4 sont {4, 5, 6}. Cela représente 3 cas favorables parmi les 6 cas possibles.

La probabilité est :

$$
P = \frac{\text{Nombre de cas favorables}}{\text{Nombre de cas possibles}} = \frac{3}{6} = 0.5
$$

**Réponse :** 50 %.
</details>

---

### **Exercice 2 : Probabilité d’événements indépendants**  
Un joueur lance deux dés. Quelle est la probabilité que l’un des dés affiche un 3 et l’autre un 5 ?

<details>
<summary>Solution</summary>
Les deux événements sont indépendants. La probabilité est donnée par :

$$
P(A \cap B) = P(A) \cdot P(B)
$$

Chaque dé ayant 6 faces :

$$
P(A) = \frac{1}{6}, \quad P(B) = \frac{1}{6}
$$

Donc :

$$
P(A \cap B) = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}
$$

**Réponse :** $ \approx 2,78 \% $.
</details>

---

### **Exercice 3 : Événement complémentaire**  
Un joueur tire une carte d’un jeu de 52 cartes. Quelle est la probabilité que la carte ne soit pas une figure (roi, dame ou valet) ?

<details>
<summary>Solution</summary>
Les figures représentent $3 \cdot 4 = 12$ cartes sur les 52 cartes.  
La probabilité de tirer une figure est :

$$
P(\text{Figure}) = \frac{12}{52} = \frac{3}{13}
$$

La probabilité de ne pas tirer une figure est le complémentaire :

$$
P(\text{Non-Figure}) = 1 - P(\text{Figure}) = 1 - \frac{3}{13} = \frac{10}{13}
$$

**Réponse :** $ \approx 76,92 \% $.
</details>

---

### **Exercice 4 : Probabilité conditionnelle**  
Dans un jeu de cartes, un joueur tire deux cartes successivement sans remise. Quelle est la probabilité que la première soit un cœur et la deuxième un as ?

<details>
<summary>Solution</summary>
Événement $A$ : La première carte est un cœur.  
Événement $B$ : La deuxième carte est un as.  

La probabilité conditionnelle est donnée par :

$$
P(A \cap B) = P(A) \cdot P(B|A)
$$

- $P(A) = \frac{13}{52} = \frac{1}{4}$ (13 cœurs dans un jeu de 52 cartes).  
- Si la première carte est un cœur, il reste 51 cartes dont 4 as :  
$P(B|A) = \frac{4}{51}$.  

Donc :

$$
P(A \cap B) = \frac{1}{4} \cdot \frac{4}{51} = \frac{1}{51} \approx 0.0196
$$

**Réponse :** $ \approx 1,96 \% $.
</details>

---

### **Exercice 5 : Probabilité combinatoire**  
Dans un tirage aléatoire de 5 cartes d’un jeu de 52 cartes, quelle est la probabilité d’obtenir exactement 2 as ?

<details>
<summary>Solution</summary>
On utilise les combinaisons :

$$
P = \frac{\binom{4}{2} \cdot \binom{48}{3}}{\binom{52}{5}}
$$

- $\binom{4}{2}$ : Nombre de façons de choisir 2 as parmi 4.

$$
\binom{4}{2} = \frac{4!}{2! \cdot (4-2)!} = 6
$$

- $\binom{48}{3}$ : Nombre de façons de choisir 3 autres cartes parmi les 48 restantes.

$$
\binom{48}{3} = \frac{48 \cdot 47 \cdot 46}{3 \cdot 2 \cdot 1} = 17296
$$

- $\binom{52}{5}$ : Nombre total de combinaisons possibles de 5 cartes.

$$
\binom{52}{5} = \frac{52 \cdot 51 \cdot 50 \cdot 49 \cdot 48}{5 \cdot 4 \cdot 3 \cdot 2 \cdot 1} = 2598960
$$

En remplaçant :

$$
P = \frac{6 \cdot 17296}{2598960} \approx 0.0397
$$

**Réponse :** $ \approx 3,97 \% $.
</details>

---

Voici la suite des exercices corrigés avec des équations entourées de sauts de ligne pour un affichage clair.

---

## **Thème : Lois de distribution discrètes**

### **Exercice 6 : Loi binomiale**  
Un joueur a 75 % de chances de réussir une attaque. Si le joueur tente 4 attaques, quelle est la probabilité de réussir exactement 2 fois ?

<details>
<summary>Solution</summary>
On applique la loi binomiale :

$$
P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}
$$

Ici :  
- $n = 4$, $k = 2$, $p = 0.75$, $1-p = 0.25$.  

Le coefficient binomial est :

$$
\binom{4}{2} = \frac{4!}{2! \cdot (4-2)!} = 6
$$

La probabilité est :

$$
P(X = 2) = 6 \cdot (0.75)^2 \cdot (0.25)^2
$$

$$
P(X = 2) = 6 \cdot 0.5625 \cdot 0.0625 = 0.2109375
$$

**Réponse :** $ \approx 21,09 \% $.
</details>

---

### **Exercice 7 : Loi binomiale cumulée**  
Un joueur a 60 % de chances de réussir un coup. Si le joueur tente 5 coups, quelle est la probabilité de réussir au moins 3 fois ?

<details>
<summary>Solution</summary>
La probabilité d’au moins 3 succès est :

$$
P(X \geq 3) = P(X = 3) + P(X = 4) + P(X = 5)
$$

Pour $P(X = k)$ :

$$
P(X = k) = \binom{5}{k} (0.6)^k (0.4)^{5-k}
$$

- $P(X = 3)$ :

$$
\binom{5}{3} = 10, \quad P(X = 3) = 10 \cdot (0.6)^3 \cdot (0.4)^2 = 0.3456
$$

- $P(X = 4)$ :

$$
\binom{5}{4} = 5, \quad P(X = 4) = 5 \cdot (0.6)^4 \cdot (0.4)^1 = 0.2592
$$

- $P(X = 5)$ :

$$
\binom{5}{5} = 1, \quad P(X = 5) = 1 \cdot (0.6)^5 \cdot (0.4)^0 = 0.07776
$$

Donc :

$$
P(X \geq 3) = 0.3456 + 0.2592 + 0.07776 = 0.68256
$$

**Réponse :** $ \approx 68,26 \% $.
</details>

---

### **Exercice 8 : Loi de Poisson**  
Un joueur subit en moyenne 2 attaques critiques par partie. Quelle est la probabilité qu’il subisse exactement 0 attaque critique lors d’une partie ?

<details>
<summary>Solution</summary>
On utilise la loi de Poisson :

$$
P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}
$$

Ici :  
- $\lambda = 2$, $k = 0$.  

La probabilité est :

$$
P(X = 0) = \frac{2^0 e^{-2}}{0!} = e^{-2} \approx 0.1353
$$

**Réponse :** $ \approx 13,53 \% $.
</details>

---

## **Thème : Statistiques descriptives**

### **Exercice 9 : Moyenne et médiane**  
Les scores de 7 joueurs sont : 10, 12, 15, 18, 20, 25, 30. Calculez la moyenne et la médiane.

<details>
<summary>Solution</summary>
1. **Moyenne** :  

$$
\bar{x} = \frac{\sum x_i}{n} = \frac{10 + 12 + 15 + 18 + 20 + 25 + 30}{7} = \frac{130}{7} \approx 18.57
$$

2. **Médiane** :  
Les données triées sont : {10, 12, 15, 18, 20, 25, 30}.  
Le nombre total de données est impair ($n = 7$), donc la médiane est la valeur centrale :

**Médiane :** $18$.

**Réponse :** Moyenne $ \approx 18,57 $, Médiane $18$.
</details>

---

### **Exercice 10 : Variance et écart-type**  
Les scores de 5 joueurs sont : 10, 20, 25, 30, 50. Calculez la variance et l’écart-type.

<details>
<summary>Solution</summary>
1. **Moyenne** :  

$$
\bar{x} = \frac{\sum x_i}{n} = \frac{10 + 20 + 25 + 30 + 50}{5} = \frac{135}{5} = 27
$$

2. **Variance** :  
La variance est :

$$
\text{Variance} = \frac{\sum (x_i - \bar{x})^2}{n}
$$

$$
\text{Variance} = \frac{(10-27)^2 + (20-27)^2 + (25-27)^2 + (30-27)^2 + (50-27)^2}{5}
$$

$$
\text{Variance} = \frac{289 + 49 + 4 + 9 + 529}{5} = \frac{880}{5} = 176
$$

3. **Écart-type** :

$$
\sigma = \sqrt{\text{Variance}} = \sqrt{176} \approx 13.27
$$

**Réponse :** Variance $ 176 $, Écart-type $ \approx 13.27 $.
</details>

---

### **Exercice 11 : Détection des outliers avec $IQR$**  
Les scores sont : 10, 15, 20, 25, 30, 35, 100. Identifiez les éventuels outliers à l’aide de la méthode de l’écart interquartile ($IQR$).

<details>
<summary>Solution</summary>
1. **Quartiles** :  
Les données triées sont : {10, 15, 20, 25, 30, 35, 100}.  
- $Q1$ (1er quartile) = 15 (25 % des données).  
- $Q3$ (3e quartile) = 35 (75 % des données).  

2. **IQR** :

$$
IQR = Q3 - Q1 = 35 - 15 = 20
$$

3. **Limites pour les outliers** :  
- Limite inférieure :

$$
Q1 - 1.5 \cdot IQR = 15 - 1.5 \cdot 20 = -15
$$

- Limite supérieure :

$$
Q3 + 1.5 \cdot IQR = 35 + 1.5 \cdot 20 = 65
$$

4. **Vérification** :  
Le score $100$ est supérieur à la limite $65$, donc c’est un **outlier**.

**Réponse :** L’outlier est $100$.
</details>

---

Voici la suite des exercices pour le **thème : Régression linéaire** avec les équations entourées de sauts de ligne pour un rendu clair.

---

## **Thème : Régression linéaire**

### **Exercice 12 : Équation de régression**  
Les données suivantes représentent les heures d’entraînement ($x$) et les scores obtenus ($y$) :  
| $x$ | 1 | 2 | 3 | 4 |  
|------|---|---|---|---|  
| $y$ | 10 | 15 | 20 | 25 |  

Déterminez l’équation de la droite de régression $y = ax + b$.

<details>
<summary>Solution</summary>
1. **Moyennes** :

$$
\bar{x} = \frac{1 + 2 + 3 + 4}{4} = 2.5
$$

$$
\bar{y} = \frac{10 + 15 + 20 + 25}{4} = 17.5
$$

2. **Pente ($a$)** :  

$$
a = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}
$$

$$
a = \frac{(1-2.5)(10-17.5) + (2-2.5)(15-17.5) + \dots}{(1-2.5)^2 + (2-2.5)^2 + \dots}
$$

$$
a = 5
$$

3. **Ordonnée à l’origine ($b$)** :

$$
b = \bar{y} - a\bar{x} = 17.5 - 5 \cdot 2.5 = 5
$$

L’équation de la droite de régression est donc :

$$
y = 5x + 5
$$

**Réponse :** $y = 5x + 5$.
</details>

---

### **Exercice 13 : Prédiction avec régression**  
Avec l’équation $y = 4x + 10$, prévoyez le score pour un joueur qui s’entraîne 6 heures.

<details>
<summary>Solution</summary>
Remplacez $x = 6$ dans l’équation :

$$
y = 4 \cdot 6 + 10
$$

$$
y = 24 + 10 = 34
$$

**Réponse :** Le score prévu est $34$.
</details>

---

### **Exercice 14 : Résidu de régression**  
Pour l’équation $y = 3x + 15$, un joueur s’entraîne 4 heures et obtient un score de 30. Calculez le résidu.

<details>
<summary>Solution</summary>
1. **Score prédit ($\hat{y}$)** :  
Pour $x = 4$ :

$$
\hat{y} = 3 \cdot 4 + 15 = 27
$$

2. **Résidu** :  
Le résidu est la différence entre le score observé ($y$) et le score prédit ($\hat{y}$) :

$$
\text{Résidu} = y - \hat{y} = 30 - 27 = 3
$$

**Réponse :** Résidu $= 3$.
</details>

---

### **Exercice 15 : Calcul de la somme des erreurs quadratiques (SSE)**  
Les données suivantes représentent les scores observés ($y_i$) et les scores prévus $\hat{y}_i$ pour 4 joueurs :  

| $y_i$  | 10  | 15  | 20  | 25  |  
| $\hat{y}_i$ | 12  | 14  | 22  | 24  |  

Calculez la somme des erreurs quadratiques ($SSE$).

<details>
<summary>Solution</summary>
1. **Erreur pour chaque joueur ($e_i$)** :  

$$
e_i = y_i - \hat{y}_i
$$

- Pour le premier joueur :

$$
e_1 = 10 - 12 = -2
$$

- Pour le deuxième joueur :

$$
e_2 = 15 - 14 = 1
$$

- Pour le troisième joueur :

$$
e_3 = 20 - 22 = -2
$$

- Pour le quatrième joueur :

$$
e_4 = 25 - 24 = 1
$$

2. **Erreur quadratique pour chaque joueur ($e_i^2$)** :  

$$
e_1^2 = (-2)^2 = 4, \quad e_2^2 = 1^2 = 1, \quad e_3^2 = (-2)^2 = 4, \quad e_4^2 = 1^2 = 1
$$

3. **Somme des erreurs quadratiques ($SSE$)** :

$$
SSE = e_1^2 + e_2^2 + e_3^2 + e_4^2 = 4 + 1 + 4 + 1 = 10
$$

**Réponse :** $SSE = 10$.
</details>

---

### **Exercice 16 : Calcul de $R^2$ (coefficient de détermination)**  
Les données suivantes représentent les scores observés ($y_i$) et les scores prévus ($\hat{y}_i$) :  
| $y_i$  | 10  | 15  | 20  | 25  |  
| $\hat{y}_i$ | 12  | 14  | 22  | 24  |  

La moyenne des scores observés est $\bar{y} = 17.5$. Calculez $R^2$.

<details>
<summary>Solution</summary>
1. **Calcul de la somme totale des carrés ($SST$)** :  

$$
SST = \sum (y_i - \bar{y})^2
$$

- Pour le premier joueur :

$$
(y_1 - \bar{y})^2 = (10 - 17.5)^2 = 56.25
$$

- Pour le deuxième joueur :

$$
(y_2 - \bar{y})^2 = (15 - 17.5)^2 = 6.25
$$

- Pour le troisième joueur :

$$
(y_3 - \bar{y})^2 = (20 - 17.5)^2 = 6.25
$$

- Pour le quatrième joueur :

$$
(y_4 - \bar{y})^2 = (25 - 17.5)^2 = 56.25
$$

Donc :

$$
SST = 56.25 + 6.25 + 6.25 + 56.25 = 125
$$

2. **Calcul de la somme des erreurs quadratiques ($SSE$)** :  

Déjà calculé dans l’exercice précédent :

$$
SSE = 10
$$

3. **Calcul de $R^2$** :  

$$
R^2 = 1 - \frac{SSE}{SST}
$$

$$
R^2 = 1 - \frac{10}{125} = 1 - 0.08 = 0.92
$$

**Réponse :** $R^2 = 0.92$, soit 92 % de la variance expliquée.
</details>

---

