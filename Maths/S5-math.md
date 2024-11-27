# S5 TOMIC - Mathématiques

 <!-- TOC -->

- [S5 TOMIC - Mathématiques](#s5-tomic---math%C3%A9matiques)
    - [Déterminer des probabilités dans les jeux de stratégie](#d%C3%A9terminer-des-probabilit%C3%A9s-dans-les-jeux-de-strat%C3%A9gie)
        - [**Probabilité**](#probabilit%C3%A9)
        - [**Indépendance des événements**](#ind%C3%A9pendance-des-%C3%A9v%C3%A9nements)
        - [**Événement complémentaire**](#%C3%A9v%C3%A9nement-compl%C3%A9mentaire)
    - [Appliquer les lois de distribution discrètes à l'analyse de risque dans des jeux](#appliquer-les-lois-de-distribution-discr%C3%A8tes-%C3%A0-lanalyse-de-risque-dans-des-jeux)
        - [**Loi binomiale**](#loi-binomiale)
        - [**Loi de Poisson**](#loi-de-poisson)
        - [**Espérance mathématique**](#esp%C3%A9rance-math%C3%A9matique)
    - [Expliquer les concepts de base de statistiques descriptives](#expliquer-les-concepts-de-base-de-statistiques-descriptives)
        - [**Moyenne**](#moyenne)
        - [**Médiane**](#m%C3%A9diane)
        - [**Écart-type**](#%C3%A9cart-type)
        - [**Loi normale**](#loi-normale)
    - [Expliquer les concepts de base de statistiques descriptives](#expliquer-les-concepts-de-base-de-statistiques-descriptives)
        - [**Moyenne**](#moyenne)
        - [**Médiane**](#m%C3%A9diane)
        - [**Écart-type**](#%C3%A9cart-type)
        - [**Loi normale**](#loi-normale)
    - [Produire une analyse statistique bivariée](#produire-une-analyse-statistique-bivari%C3%A9e)
        - [**Covariance**](#covariance)
        - [**Coefficient de corrélation**](#coefficient-de-corr%C3%A9lation)
        - [**Régression linéaire**](#r%C3%A9gression-lin%C3%A9aire)
    - [Appliquer la méthode des moindres carrés ajustement de données](#appliquer-la-m%C3%A9thode-des-moindres-carr%C3%A9s-ajustement-de-donn%C3%A9es)
        - [**Formule des moindres carrés**](#formule-des-moindres-carr%C3%A9s)
            - [**Pente** :](#pente-)
            - [**Ordonnée à l’origine** :](#ordonn%C3%A9e-%C3%A0-lorigine-)
        - [**Erreur quadratique moyenne MSE**](#erreur-quadratique-moyenne-mse)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Estimer une erreur](#estimer-une-erreur)
        - [**Erreur standard**](#erreur-standard)
        - [**Intervalle de confiance niveau 95%**](#intervalle-de-confiance-niveau-95%25)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Construire un test statistique](#construire-un-test-statistique)
        - [**Hypothèses**](#hypoth%C3%A8ses)
            - [**Hypothèse nulle \ H_0 \** :](#hypoth%C3%A8se-nulle-%5C-h_0-%5C-)
            - [**Hypothèse alternative \ H_1 \** :](#hypoth%C3%A8se-alternative-%5C-h_1-%5C-)
        - [**Statistique du test**](#statistique-du-test)
        - [**P-valeur**](#p-valeur)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Interpréter des tableaux de données](#interpr%C3%A9ter-des-tableaux-de-donn%C3%A9es)
        - [**Tableau de contingence**](#tableau-de-contingence)
        - [**Test du \ \chi^2 \**](#test-du-%5C-%5Cchi%5E2-%5C)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Établir un intervalle de confiance](#%C3%A9tablir-un-intervalle-de-confiance)
        - [**Formule générale**](#formule-g%C3%A9n%C3%A9rale)
        - [**Interprétation**](#interpr%C3%A9tation)
            - [**Largeur de l’intervalle** :](#largeur-de-lintervalle-)
            - [**Signification** :](#signification-)
        - [**Applications dans les jeux**](#applications-dans-les-jeux)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Analyser les résultats des statistiques descriptives](#analyser-les-r%C3%A9sultats-des-statistiques-descriptives)
        - [**Comparaison des tendances centrales**](#comparaison-des-tendances-centrales)
            - [**Tendances centrales** :](#tendances-centrales-)
        - [**Analyse des écarts-types pour la dispersion**](#analyse-des-%C3%A9carts-types-pour-la-dispersion)
            - [**Écart-type \ \sigma \** :](#%C3%A9cart-type-%5C-%5Csigma-%5C-)
        - [**Détection des outliers via les boxplots ou \ Z \-scores**](#d%C3%A9tection-des-outliers-via-les-boxplots-ou-%5C-z-%5C-scores)
            - [**Boxplots**](#boxplots)
            - [**\ Z \-scores**](#%5C-z-%5C-scores)
        - [**Applications globales dans les jeux**](#applications-globales-dans-les-jeux)
    - [Analyser et évaluer les méthodes de détection des anomalies dans les données de séries temporelles](#analyser-et-%C3%A9valuer-les-m%C3%A9thodes-de-d%C3%A9tection-des-anomalies-dans-les-donn%C3%A9es-de-s%C3%A9ries-temporelles)
        - [**\ Z \-score**](#%5C-z-%5C-score)
        - [**Interquartile Range IQR**](#interquartile-range-iqr)
        - [**Pourcentage du maximum**](#pourcentage-du-maximum)
        - [**Statistiques robustes**](#statistiques-robustes)
            - [**Formule du MAD** :](#formule-du-mad-)

<!-- /TOC -->

---

## Déterminer des probabilités dans les jeux de stratégie

Dans les jeux de stratégie, la probabilité permet de modéliser et de comprendre les chances de succès d'une action ou d'un événement. Cela aide à la prise de décisions en tenant compte des incertitudes. Voici une explication détaillée des concepts et formules associés.

---

### **Probabilité**

**Formule** :  
$$P(A) = \frac{\text{Nombre de cas favorables}}{\text{Nombre de cas possibles}}$$

**Explication** :  
La probabilité d'un événement $ A $ correspond à la proportion des cas favorables parmi tous les cas possibles. Par exemple, dans un lancer de dé équilibré, la probabilité d'obtenir un 6 est :

$$P(6) = \frac{1}{6}$$

car il y a un seul cas favorable (le 6) sur les six résultats possibles (1, 2, 3, 4, 5, 6).

**Application dans les jeux de stratégie** :  
Cette formule peut être utilisée pour calculer les chances de réussite d'un coup ou d'une tactique. Par exemple, si un joueur de cartes veut tirer un atout dans un jeu de 52 cartes où il reste 13 atouts, la probabilité est :$P(\text{Atout}) = \frac{13}{52} = \frac{1}{4}$
---

### **Indépendance des événements**

**Formule** :  
$$P(A \cap B) = P(A) \cdot P(B)$$

**Explication** : 
Deux événements $ A $ et $ B $ sont dits indépendants si la probabilité qu'ils se produisent ensemble est égale au produit de leurs probabilités individuelles. Cela signifie que l'occurrence de l'un n'affecte pas l'autre.

**Exemple** :  
Dans un jeu de stratégie impliquant des dés, si vous lancez deux dés, la probabilité d'obtenir un 6 sur le premier dé ($ A $) et un 5 sur le second dé ($ B $) est :$P(A \cap B) = P(A) \cdot P(B) = \frac{1}{6} \cdot \frac{1}{6} = \frac{1}{36}$
**Attention** :  
Si les événements sont dépendants, comme tirer deux cartes consécutives d’un jeu sans remise, la formule ci-dessus ne s’applique pas. Les probabilités doivent être ajustées en tenant compte de la dépendance.

**Utilité dans les jeux de stratégie** :  
L'indépendance aide à modéliser des actions simultanées ou successives, comme calculer les chances de succès pour plusieurs actions différentes.

---

### **Événement complémentaire**

**Formule** :  
$$P(A^c) = 1 - P(A)$$

**Explication** :  
La probabilité du complémentaire $ A^c $ d'un événement $ A $ correspond à la probabilité que $ A $ ne se produise pas. Cela repose sur le fait que la somme des probabilités de tous les résultats possibles d'une situation est égale à 1.

**Exemple** :  
Dans un lancer de dé, la probabilité de ne pas obtenir un 6 est :$P(\text{Pas 6}) = 1 - P(6) = 1 - \frac{1}{6} = \frac{5}{6}$
**Utilisation dans les jeux de stratégie** :  
Cela permet de déterminer les chances d'échec d'une action. Par exemple, si un joueur estime qu'il a 70 % de chances de réussir une attaque ($ P(\text{Réussite}) = 0.7 $), alors ses chances d’échouer sont :$P(\text{Échec}) = 1 - 0.7 = 0.3$
---

## Appliquer les lois de distribution discrètes à l'analyse de risque dans des jeux

Dans les jeux, notamment ceux impliquant des choix stratégiques, l’utilisation des lois de distribution discrètes permet de modéliser des événements aléatoires et de quantifier les risques associés. Ces outils aident à évaluer les chances de succès ou d’échec de stratégies, ainsi que les scénarios improbables mais critiques.

---

### **Loi binomiale**

**Formule** :  $P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$
- $ n $ : Nombre total d’essais (ou actions).
- $ k $ : Nombre de succès souhaités.
- $ p $ : Probabilité de succès pour un essai donné.
- $ \binom{n}{k} $ : Nombre de combinaisons possibles, donné par $ \binom{n}{k} = \frac{n!}{k! \cdot (n-k)!} $.

**Explication** :  
La loi binomiale s'applique lorsque nous avons une séquence de $ n $ essais indépendants, chaque essai ayant deux issues possibles : succès ou échec. La probabilité $ P(X = k) $ indique la probabilité d'obtenir exactement $ k $ succès.

**Exemple** :  
Dans un jeu où un joueur a 60 % de chances ($ p = 0.6 $) de réussir une action, et où il tente 5 actions ($ n = 5 $), la probabilité de réussir exactement 3 fois ($ k = 3 $) est donnée par :$P(X = 3) = \binom{5}{3} (0.6)^3 (0.4)^2 = 10 \cdot 0.216 \cdot 0.16 = 0.3456$
**Application dans les jeux** :  
Cette loi est utile pour évaluer les stratégies reposant sur des actions répétées, comme le nombre d’attaques réussies ou la probabilité de remporter un certain nombre de manches.

---

### **Loi de Poisson**

**Formule** :  $P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$
- $ \lambda $ : Moyenne ou intensité du phénomène (nombre moyen d’événements dans un intervalle donné).
- $ k $ : Nombre d’occurrences.

**Explication** :  
La loi de Poisson s'applique aux événements rares sur un intervalle de temps ou d’espace. Elle modélise la probabilité d'observer exactement $ k $ occurrences lorsque la moyenne des occurrences est $ \lambda $.

**Exemple** :  
Dans un jeu de stratégie, supposons qu’un joueur subisse en moyenne 2 attaques par tour ($ \lambda = 2 $). La probabilité qu’il subisse exactement 3 attaques lors d’un tour est :$P(X = 3) = \frac{2^3 e^{-2}}{3!} = \frac{8 \cdot 0.1353}{6} = 0.1804$
**Application dans les jeux** :  
La loi de Poisson aide à évaluer les risques d’événements rares, comme des attaques critiques, ou des scénarios inhabituels mais potentiellement dangereux.

---

### **Espérance mathématique**

**Formule** :  $E(X) = \sum\_{x} x \cdot P(X = x)$
**Explication** :  
L'espérance mathématique est la moyenne pondérée des résultats possibles, où chaque résultat est multiplié par sa probabilité. Elle représente la valeur moyenne attendue d'une variable aléatoire après de nombreuses répétitions.

**Exemple** :  
Dans un jeu, un joueur tire au hasard une carte parmi trois cartes marquées $ 1, 2, 5 $. Si chaque carte a une probabilité égale ($ P(X=x) = \frac{1}{3} $), l’espérance des gains est :$E(X) = 1 \cdot \frac{1}{3} + 2 \cdot \frac{1}{3} + 5 \cdot \frac{1}{3} = \frac{1 + 2 + 5}{3} = 2.67$
**Application dans les jeux** :  
L'espérance permet d'évaluer la rentabilité ou le risque moyen d’une stratégie, comme les gains espérés dans une série de paris.

---

## Expliquer les concepts de base de statistiques descriptives

Les statistiques descriptives permettent de résumer, analyser et interpréter un ensemble de données en identifiant des mesures clés. Ces outils sont essentiels pour comprendre la structure des données et prendre des décisions éclairées. Voici une explication des principaux concepts.

---

### **Moyenne**

**Formule** :  $\bar{x} = \frac{1}{n} \sum\_{i=1}^n x_i$
- $ \bar{x} $ : Moyenne des données.
- $ n $ : Nombre total de données.
- $ x_i $ : Valeurs individuelles dans l’ensemble des données.

**Explication** :  
La moyenne représente la valeur centrale ou typique d’un ensemble de données. Elle est obtenue en additionnant toutes les valeurs puis en divisant par le nombre total d’observations.

**Exemple** :  
Dans un jeu où les scores des joueurs sont $ 10, 15, 20, 25, 30 $, la moyenne des scores est :$\bar{x} = \frac{10 + 15 + 20 + 25 + 30}{5} = 20$
**Application dans les jeux** :  
La moyenne peut être utilisée pour estimer la performance moyenne des joueurs ou pour évaluer le score attendu dans des conditions similaires.

---

### **Médiane**

**Définition** :  
La médiane est la valeur centrale d’un ensemble de données triées (par ordre croissant ou décroissant). Si le nombre de données est impair, c’est la valeur du milieu. Si le nombre est pair, la médiane est la moyenne des deux valeurs centrales.

**Explication** :  
La médiane est une mesure de tendance centrale robuste, moins sensible aux valeurs extrêmes (outliers) que la moyenne.

**Exemple** :  
Pour les scores $ 10, 15, 20, 25, 100 $, la médiane est $ 20 $ (valeur centrale après tri). Si les scores étaient $ 10, 15, 20, 25 $, la médiane serait :$\text{Médiane} = \frac{15 + 20}{2} = 17.5$
**Application dans les jeux** :  
La médiane est utile pour identifier une "performance typique" lorsqu'il y a des scores aberrants, par exemple des joueurs exceptionnellement mauvais ou bons.

---

### **Écart-type**

**Formule** :  $\sigma = \sqrt{\frac{1}{n} \sum\_{i=1}^n (x_i - \bar{x})^2}$
- $ \sigma $ : Écart-type (mesure de dispersion).
- $ \bar{x} $ : Moyenne des données.
- $ x_i $ : Valeurs individuelles.
- $ n $ : Nombre total de données.

**Explication** :  
L’écart-type mesure la dispersion ou la variabilité des données autour de la moyenne. Un écart-type faible indique que les données sont regroupées près de la moyenne, tandis qu’un écart-type élevé signale une grande variation.

**Exemple** :  
Pour les scores $ 10, 15, 20, 25, 30 $, où $ \bar{x} = 20 $ :$\sigma = \sqrt{\frac{(10-20)^2 + (15-20)^2 + (20-20)^2 + (25-20)^2 + (30-20)^2}{5}}
= \sqrt{\frac{100 + 25 + 0 + 25 + 100}{5}} = 7.07$
**Application dans les jeux** :  
L’écart-type aide à évaluer la stabilité des performances. Par exemple, dans un jeu compétitif, un joueur avec un faible écart-type est plus régulier.

---

### **Loi normale**

**Formule** :  $f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$
- $ \mu $ : Moyenne.
- $ \sigma $ : Écart-type.
- $ x $ : Valeur d’intérêt.

**Explication** :  
La loi normale, ou distribution gaussienne, est une courbe en cloche symétrique centrée sur la moyenne $ \mu $. Elle est caractérisée par deux paramètres : $ \mu $ (moyenne) et $ \sigma $ (écart-type). Environ 68 % des données se trouvent dans l’intervalle $ [\mu - \sigma, \mu + \sigma] $, et 95 % dans $ [\mu - 2\sigma, \mu + 2\sigma] $.

**Exemple** :  
Dans un jeu, si les scores suivent une distribution normale avec $ \mu = 50 $ et $ \sigma = 10 $, environ 68 % des scores se situent entre $ 40 $ et $ 60 $.

**Application dans les jeux** :  
La loi normale est souvent utilisée pour modéliser des performances ou des résultats lorsqu’ils suivent un comportement naturel. Par exemple, les temps de réaction ou les scores globaux peuvent être approximés par une loi normale.

---

## Expliquer les concepts de base de statistiques descriptives

Les statistiques descriptives permettent de résumer, analyser et interpréter un ensemble de données en identifiant des mesures clés. Ces outils sont essentiels pour comprendre la structure des données et prendre des décisions éclairées. Voici une explication des principaux concepts.

---

### **Moyenne**

**Formule** :  $\bar{x} = \frac{1}{n} \sum\_{i=1}^n x_i$
- $ \bar{x} $ : Moyenne des données.
- $ n $ : Nombre total de données.
- $ x_i $ : Valeurs individuelles dans l’ensemble des données.

**Explication** :  
La moyenne représente la valeur centrale ou typique d’un ensemble de données. Elle est obtenue en additionnant toutes les valeurs puis en divisant par le nombre total d’observations.

**Exemple** :  
Dans un jeu où les scores des joueurs sont $ 10, 15, 20, 25, 30 $, la moyenne des scores est :$\bar{x} = \frac{10 + 15 + 20 + 25 + 30}{5} = 20$
**Application dans les jeux** :  
La moyenne peut être utilisée pour estimer la performance moyenne des joueurs ou pour évaluer le score attendu dans des conditions similaires.

---

### **Médiane**

**Définition** :  
La médiane est la valeur centrale d’un ensemble de données triées (par ordre croissant ou décroissant). Si le nombre de données est impair, c’est la valeur du milieu. Si le nombre est pair, la médiane est la moyenne des deux valeurs centrales.

**Explication** :  
La médiane est une mesure de tendance centrale robuste, moins sensible aux valeurs extrêmes (outliers) que la moyenne.

**Exemple** :  
Pour les scores $ 10, 15, 20, 25, 100 $, la médiane est $ 20 $ (valeur centrale après tri). Si les scores étaient $ 10, 15, 20, 25 $, la médiane serait :$\text{Médiane} = \frac{15 + 20}{2} = 17.5$
**Application dans les jeux** :  
La médiane est utile pour identifier une "performance typique" lorsqu'il y a des scores aberrants, par exemple des joueurs exceptionnellement mauvais ou bons.

---

### **Écart-type**

**Formule** :  $\sigma = \sqrt{\frac{1}{n} \sum\_{i=1}^n (x_i - \bar{x})^2}$
- $ \sigma $ : Écart-type (mesure de dispersion).
- $ \bar{x} $ : Moyenne des données.
- $ x_i $ : Valeurs individuelles.
- $ n $ : Nombre total de données.

**Explication** :  
L’écart-type mesure la dispersion ou la variabilité des données autour de la moyenne. Un écart-type faible indique que les données sont regroupées près de la moyenne, tandis qu’un écart-type élevé signale une grande variation.

**Exemple** :  
Pour les scores $ 10, 15, 20, 25, 30 $, où $ \bar{x} = 20 $ :$\sigma = \sqrt{\frac{(10-20)^2 + (15-20)^2 + (20-20)^2 + (25-20)^2 + (30-20)^2}{5}}
= \sqrt{\frac{100 + 25 + 0 + 25 + 100}{5}} = 7.07$
**Application dans les jeux** :  
L’écart-type aide à évaluer la stabilité des performances. Par exemple, dans un jeu compétitif, un joueur avec un faible écart-type est plus régulier.

---

### **Loi normale**

**Formule** :  $f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2}\left(\frac{x-\mu}{\sigma}\right)^2}$
- $ \mu $ : Moyenne.
- $ \sigma $ : Écart-type.
- $ x $ : Valeur d’intérêt.

**Explication** :  
La loi normale, ou distribution gaussienne, est une courbe en cloche symétrique centrée sur la moyenne $ \mu $. Elle est caractérisée par deux paramètres : $ \mu $ (moyenne) et $ \sigma $ (écart-type). Environ 68 % des données se trouvent dans l’intervalle $ [\mu - \sigma, \mu + \sigma] $, et 95 % dans $ [\mu - 2\sigma, \mu + 2\sigma] $.

**Exemple** :  
Dans un jeu, si les scores suivent une distribution normale avec $ \mu = 50 $ et $ \sigma = 10 $, environ 68 % des scores se situent entre $ 40 $ et $ 60 $.

**Application dans les jeux** :  
La loi normale est souvent utilisée pour modéliser des performances ou des résultats lorsqu’ils suivent un comportement naturel. Par exemple, les temps de réaction ou les scores globaux peuvent être approximés par une loi normale.

---

## Produire une analyse statistique bivariée

L'analyse statistique bivariée permet d'examiner la relation entre deux variables. Elle est essentielle pour comprendre si des variables influencent l'une l'autre et comment elles interagissent. Voici les concepts clés et leurs explications.

---

### **Covariance**

**Formule** :  $\text{Cov}(X, Y) = \frac{1}{n} \sum\_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})$
- $ \text{Cov}(X, Y) $ : Covariance entre les variables $ X $ et $ Y $.
- $ x_i, y_i $ : Valeurs individuelles des variables $ X $ et $ Y $.
- $ \bar{x}, \bar{y} $ : Moyennes des variables $ X $ et $ Y $.

**Explication** :  
La covariance mesure dans quelle mesure deux variables varient ensemble. Si la covariance est positive, $ X $ et $ Y $ tendent à évoluer dans le même sens. Si elle est négative, elles varient dans des sens opposés. Une covariance proche de zéro indique une absence de relation linéaire.

**Exemple** :  
Dans un jeu, $ X $ représente le nombre d'attaques réussies et $ Y $ le score total. Une covariance positive indique qu'un plus grand nombre d'attaques réussies est associé à un score plus élevé.

**Application dans les jeux** :  
Analyser la covariance peut aider à comprendre comment deux aspects d'un jeu sont liés, par exemple, si une meilleure précision augmente la probabilité de victoire.

---

### **Coefficient de corrélation**

**Formule** :  $r = \frac{\text{Cov}(X, Y)}{\sigma_X \sigma_Y}$
- $ r $ : Coefficient de corrélation (entre -1 et 1).
- $ \text{Cov}(X, Y) $ : Covariance entre $ X $ et $ Y $.
- $ \sigma_X, \sigma_Y $ : Écart-types des variables $ X $ et $ Y $.

**Explication** :  
Le coefficient de corrélation mesure l'intensité et la direction de la relation linéaire entre deux variables.

- $ r > 0 $ : Relation positive (les variables augmentent ensemble).
- $ r < 0 $ : Relation négative (une variable augmente pendant que l’autre diminue).
- $ r = 0 $ : Absence de relation linéaire.  
  Plus $ r $ est proche de -1 ou 1, plus la relation est forte.

**Exemple** :  
Dans un jeu, si $ X $ est le temps de réaction d’un joueur et $ Y $ le nombre de coups réussis, un $ r $ négatif indiquerait qu’un temps de réaction plus faible est associé à un meilleur score.

**Application dans les jeux** :  
Le coefficient de corrélation est utile pour quantifier la relation entre les variables et évaluer si l'amélioration d'une variable (par exemple, la précision) peut influencer une autre (le score).

---

### **Régression linéaire**

**Formule** :  $y = ax + b$
- $ y $ : Variable dépendante.
- $ x $ : Variable indépendante.
- $ a $ : Pente de la droite (indique l’effet de $ x $ sur $ y $).
- $ b $ : Ordonnée à l'origine (valeur de $ y $ lorsque $ x = 0 $).

**Explication** :  
La régression linéaire modélise la relation entre deux variables en ajustant une droite de tendance. Elle est utilisée pour prédire les valeurs de $ y $ en fonction de $ x $ ou pour quantifier l’impact de $ x $ sur $ y $.

**Exemple** :  
Dans un jeu, $ x $ représente l’entraînement d’un joueur en heures, et $ y $ son score moyen. Une équation $ y = 5x + 20 $ suggère que chaque heure d'entraînement augmente le score moyen de 5 points, avec un score initial de 20 sans entraînement.

**Application dans les jeux** :  
La régression linéaire est utilisée pour :

- Prédire les performances futures des joueurs.
- Identifier les facteurs clés influençant les scores ou les résultats.

---

## Appliquer la méthode des moindres carrés (ajustement de données)

La méthode des moindres carrés est une technique fondamentale pour ajuster une droite linéaire aux données expérimentales. Elle est utilisée pour modéliser une relation entre deux variables, minimiser les erreurs entre les valeurs observées et prédites, et effectuer des prévisions.

---

### **Formule des moindres carrés**

#### **Pente** :
$a = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sum (x_i - \bar{x})^2}$
- $ a $ : Pente de la droite d’ajustement.
- $ x_i, y_i $ : Valeurs des observations pour les variables $ X $ et $ Y $.
- $ \bar{x}, \bar{y} $ : Moyennes des variables $ X $ et $ Y $.

#### **Ordonnée à l’origine** :
$b = \bar{y} - a \bar{x}$
- $ b $ : Ordonnée à l’origine, c’est-à-dire la valeur de $ y $ lorsque $ x = 0 $.

**Explication** :  
La pente ($ a $) indique le taux de variation de la variable $ y $ par rapport à $ x $. Si $ a > 0 $, $ y $ augmente avec $ x $ ; si $ a < 0 $, $ y $ diminue avec $ x $. L’ordonnée à l’origine ($ b $) représente la valeur de départ de $ y $ lorsque $ x $ est nul.

**Exemple** :  
Dans un jeu, $ x $ représente le nombre de sessions d’entraînement et $ y $ le score moyen obtenu. Si $ a = 3 $ et $ b = 50 $, la relation est donnée par :$y = 3x + 50$Cela signifie que chaque session d'entraînement supplémentaire augmente le score moyen de 3 points, avec un score initial de 50 sans entraînement.

**Application dans les jeux** :  
La formule est utilisée pour :

- Identifier des relations linéaires entre des variables (ex. sessions d’entraînement et score).
- Prédire les résultats futurs basés sur les performances passées.

---

### **Erreur quadratique moyenne (MSE)**

**Formule** :  $MSE = \frac{1}{n} \sum\_{i=1}^n (y_i - \hat{y}\_i)^2$
- $ MSE $ : Erreur quadratique moyenne.
- $ y_i $ : Valeurs observées (réelles).
- $ \hat{y}\_i $ : Valeurs prédites par le modèle.
- $ n $ : Nombre total de points de données.

**Explication** :  
Le $ MSE $ mesure l’erreur globale entre les valeurs prédites ($ \hat{y}\_i $) et les valeurs observées ($ y_i $). Plus le $ MSE $ est faible, meilleur est l’ajustement de la droite aux données.

**Exemple** :  
Pour les valeurs observées $ y = [20, 25, 30] $ et les valeurs prédites $ \hat{y} = [22, 24, 29] $, l’erreur quadratique moyenne est calculée comme suit :$MSE = \frac{(20-22)^2 + (25-24)^2 + (30-29)^2}{3} = \frac{4 + 1 + 1}{3} = 2$
**Application dans les jeux** :  
Le $ MSE $ est utile pour :

- Mesurer la précision du modèle d’ajustement.
- Comparer différents modèles et choisir celui qui minimise l’erreur.

### **Applications globales dans les jeux**

1. **Ajustement des performances** : Comprendre comment une variable (ex. temps de jeu) influence une autre (score).
2. **Prédictions** : Prévoir les scores futurs en fonction des efforts investis.
3. **Optimisation des stratégies** : Identifier les facteurs ayant un impact significatif pour ajuster la stratégie en jeu.
4. **Évaluation des modèles** : Utiliser le $ MSE $ pour évaluer si l’ajustement est fiable et précis.

---

## Estimer une erreur

L’estimation des erreurs est essentielle en statistique pour mesurer la fiabilité des résultats et comprendre l’incertitude associée aux observations. Ces outils permettent de quantifier la précision d’une estimation ou d’une prédiction.

---

### **Erreur standard**

**Formule** :  $SE = \frac{\sigma}{\sqrt{n}}$
- $ SE $ : Erreur standard.
- $ \sigma $ : Écart-type de l’échantillon.
- $ n $ : Taille de l’échantillon.

**Explication** :  
L’erreur standard mesure la variabilité de la moyenne d’un échantillon par rapport à la moyenne réelle de la population. Plus l’échantillon est grand ($ n $ élevé), plus l’erreur standard est faible, ce qui signifie que la moyenne estimée est plus proche de la vraie moyenne.

**Exemple** :  
Supposons que dans un jeu, les scores moyens des joueurs ($ \bar{x} $) ont un écart-type $ \sigma = 10 $, et que l'échantillon comprend $ n = 25 $ joueurs. L’erreur standard est :$SE = \frac{10}{\sqrt{25}} = \frac{10}{5} = 2$Cela signifie que la moyenne calculée à partir de cet échantillon a une incertitude de ±2 points.

**Application dans les jeux** :  
L’erreur standard est utilisée pour :

- Évaluer la précision des moyennes calculées, comme le score moyen des joueurs.
- Comparer différentes performances ou stratégies en tenant compte de la variabilité.

---

### **Intervalle de confiance (niveau 95%)**

**Formule** :  $\text{IC} = \bar{x} \pm 1.96 \cdot SE$
- $ \bar{x} $ : Moyenne de l’échantillon.
- $ 1.96 $ : Coefficient pour un intervalle de confiance à 95 % (provenant de la loi normale).
- $ SE $ : Erreur standard.

**Explication** :  
L’intervalle de confiance (IC) donne une plage dans laquelle on estime que la vraie moyenne de la population se trouve avec une certaine probabilité (95 % dans cet exemple). Plus $ SE $ est faible, plus l’intervalle est étroit, indiquant une estimation précise.

**Exemple** :  
Si la moyenne des scores des joueurs est $ \bar{x} = 50 $ avec un $ SE = 2 $, l’intervalle de confiance à 95 % est :$\text{IC} = 50 \pm 1.96 \cdot 2 = [46.08, 53.92]$Cela signifie qu’il y a 95 % de chances que la vraie moyenne des scores des joueurs se trouve entre 46.08 et 53.92.

**Application dans les jeux** :

- **Évaluation des scores** : Déterminer une plage probable pour les performances moyennes des joueurs.
- **Prise de décision** : Évaluer si les résultats observés sont fiables ou dus au hasard.
- **Comparaison de stratégies** : S'assurer qu’une stratégie est significativement meilleure que les autres.

### **Applications globales dans les jeux**

1. **Évaluer la précision des estimations** : L’erreur standard aide à comprendre dans quelle mesure une moyenne ou une prédiction est fiable.
2. **Analyser les performances** : Les intervalles de confiance permettent de comparer les performances des joueurs ou des stratégies avec une certaine assurance.
3. **Réduire l’incertitude** : En augmentant la taille des échantillons ($ n $), on réduit l’erreur standard et affine les prédictions.

---

## Construire un test statistique

Un test statistique est une méthode permettant de vérifier une hypothèse sur une population à partir d’un échantillon. Il aide à déterminer si un résultat observé est significatif ou simplement dû au hasard.

---

### **Hypothèses**

#### **Hypothèse nulle ($ H_0 $)** :

$ H_0 $ représente l’absence d’effet ou de différence. C’est l’hypothèse par défaut que l’on cherche à rejeter.

#### **Hypothèse alternative ($ H_1 $)** :

$ H_1 $ est l’hypothèse opposée à $ H_0 $. Elle suggère qu’il existe un effet ou une différence significative.

**Explication** :  
Le test statistique consiste à déterminer si les données soutiennent $ H_0 $ ou si elles sont suffisamment éloignées de cette hypothèse pour accepter $ H_1 $.

**Exemple** :  
Dans un jeu, on teste si une nouvelle stratégie améliore le score moyen.

- $ H_0 $ : La stratégie n’a aucun effet ($ \mu = 50 $, où $ 50 $ est le score moyen actuel).
- $ H_1 $ : La stratégie améliore le score ($ \mu > 50 $).

---

### **Statistique du test**

**Formule** :  $Z = \frac{\bar{x} - \mu}{SE}$
- $ Z $ : Statistique du test (nombre d’écarts-types entre la moyenne observée et la moyenne sous $ H_0 $).
- $ \bar{x} $ : Moyenne observée dans l’échantillon.
- $ \mu $ : Moyenne attendue sous $ H_0 $.
- $ SE $ : Erreur standard.

**Explication** :  
La statistique $ Z $ mesure la distance entre la moyenne observée ($ \bar{x} $) et la moyenne attendue ($ \mu $), normalisée par l’erreur standard ($ SE $). Une valeur $ Z $ élevée indique que $ \bar{x} $ est loin de $ \mu $, ce qui soutient $ H_1 $.

**Exemple** :  
Si $ \bar{x} = 55 $, $ \mu = 50 $, et $ SE = 2 $, alors :$Z = \frac{55 - 50}{2} = 2.5$Un $ Z $ de 2.5 indique que la moyenne observée est à 2.5 écarts-types de la moyenne attendue.

---

### **P-valeur**

**Définition** :  
La **p-valeur** est la probabilité d’obtenir un résultat aussi extrême (ou plus extrême) que celui observé, sous l’hypothèse $ H_0 $.

- Si $ p $-valeur < niveau de significativité ($ \alpha $, souvent fixé à 0.05), on rejette $ H_0 $.
- Si $ p $-valeur ≥ $ \alpha $, on ne rejette pas $ H_0 $.

**Explication** :  
La $ p $-valeur quantifie la plausibilité de $ H_0 $. Plus elle est faible, moins les données sont compatibles avec $ H_0 $, et plus il est raisonnable d’accepter $ H_1 $.

**Exemple** :  
Si $ Z = 2.5 $, la $ p $-valeur (à partir des tables de la loi normale) est environ 0.012. Avec un seuil $ \alpha = 0.05 $, on rejette $ H_0 $ et accepte $ H_1 $, concluant que la nouvelle stratégie améliore le score.

### **Applications globales dans les jeux**

1. **Évaluation des stratégies** : Tester si une nouvelle stratégie améliore significativement les scores des joueurs.
2. **Comparaison des performances** : Déterminer si deux groupes de joueurs diffèrent significativement dans leurs performances.
3. **Optimisation des mécanismes de jeu** : Identifier des effets significatifs dans les changements de règles ou d’outils.
4. **Analyse des résultats expérimentaux** : Vérifier la robustesse des conclusions tirées de tests en jeu.

---

## Interpréter des tableaux de données

L’interprétation des tableaux de données est essentielle pour extraire des informations significatives et identifier des relations ou des tendances. Les outils comme les tableaux de contingence et le test $ \chi^2 $ permettent d’analyser les relations entre variables, en particulier lorsqu’elles sont catégoriques.

---

### **Tableau de contingence**

**Définition** :  
Un tableau de contingence est une table de fréquences qui résume les relations entre deux variables catégoriques. Les lignes représentent les catégories d’une variable, et les colonnes celles de l’autre. Chaque cellule montre le nombre d’observations correspondant à une combinaison spécifique des deux variables.

**Explication** :  
Ce tableau permet d’explorer les interactions entre les variables et de détecter d’éventuelles dépendances ou corrélations.

**Exemple** :  
Dans un jeu, un tableau de contingence peut comparer les préférences des joueurs pour deux types d’armes en fonction de leur expérience.

| **Expérience** | **Arme A** | **Arme B** | **Total** |
| -------------- | ---------- | ---------- | --------- |
| Débutant       | 30         | 50         | 80        |
| Avancé         | 70         | 50         | 120       |
| **Total**      | 100        | 100        | 200       |

Ce tableau montre que les joueurs avancés préfèrent davantage l’arme A par rapport aux débutants.

**Application dans les jeux** :

- Analyser les préférences des joueurs en fonction de caractéristiques (ex. choix d’armes, modes de jeu).
- Comprendre les relations entre différents comportements des joueurs.

---

### **Test du $ \chi^2 $**

**Formule** :  $\chi^2 = \sum \frac{(O - E)^2}{E}$
- $ \chi^2 $ : Statistique du test.
- $ O $ : Valeur observée dans chaque cellule.
- $ E $ : Valeur attendue (si les deux variables étaient indépendantes).

**Calcul des valeurs attendues** :  
Les valeurs $ E $ sont calculées comme :$E = \frac{\text{Total ligne} \times \text{Total colonne}}{\text{Total général}}$
**Explication** :  
Le test $ \chi^2 $ vérifie si deux variables catégoriques sont indépendantes. Une valeur $ \chi^2 $ élevée indique une dépendance entre les variables, tandis qu’une valeur faible suggère une indépendance.

**Exemple** :  
Dans le tableau précédent, pour la cellule "Débutant, Arme A", l’attendu $ E $ est calculé comme :$E = \frac{\text{Total ligne Débutant} \times \text{Total colonne Arme A}}{\text{Total général}} = \frac{80 \times 100}{200} = 40$La contribution à $ \chi^2 $ pour cette cellule est :$\frac{(O - E)^2}{E} = \frac{(30 - 40)^2}{40} = \frac{100}{40} = 2.5$
Le test $ \chi^2 $ total additionne ces contributions pour toutes les cellules et compare la valeur obtenue à une table critique pour évaluer l’indépendance des variables.

**Application dans les jeux** :

- Tester si des choix stratégiques (ex. armes, personnages) sont liés à des niveaux d’expérience ou d’autres variables.
- Vérifier si les résultats observés diffèrent significativement de ce qui serait attendu par hasard.

### **Applications globales dans les jeux**

1. **Analyser les relations catégoriques** : Identifier si des préférences ou comportements sont influencés par des facteurs comme l’expérience, les modes de jeu ou le niveau.
2. **Valider des hypothèses** : Vérifier si les distributions observées dans un tableau correspondent à des distributions attendues.
3. **Optimiser l’expérience utilisateur** : Identifier des préférences spécifiques à des segments de joueurs pour personnaliser les mécanismes de jeu.
4. **Détection de biais** : Repérer des tendances ou des déséquilibres dans les choix ou performances des joueurs.

---

## Établir un intervalle de confiance

Un intervalle de confiance (IC) est une plage de valeurs qui estime avec une certaine probabilité la vraie valeur d’un paramètre inconnu, comme une moyenne ou une proportion. Il permet d’exprimer l’incertitude associée à une estimation.

---

### **Formule générale**
$\text{IC} = \bar{x} \pm z \cdot SE$
- $ \bar{x} $ : Moyenne de l’échantillon.
- $ z $ : Coefficient correspondant au niveau de confiance (par exemple, $ z = 1.96 $ pour un IC de 95 %).
- $ SE $ : Erreur standard, donnée par $ SE = \frac{\sigma}{\sqrt{n}} $, où $ \sigma $ est l’écart-type et $ n $, la taille de l’échantillon.

**Explication** :  
L’intervalle de confiance fournit une plage probable pour la valeur réelle d’un paramètre dans une population, en tenant compte de la variabilité des données. Le niveau de confiance indique la probabilité que cet intervalle contienne la vraie valeur.

**Exemple** :  
Dans un jeu, la moyenne des scores des joueurs est $ \bar{x} = 70 $ avec un $ SE = 2 $. Pour un niveau de confiance de 95 % ($ z = 1.96 $), l’intervalle de confiance est :$\text{IC} = 70 \pm 1.96 \cdot 2 = [66.08, 73.92]$Cela signifie qu’il y a 95 % de chances que la vraie moyenne des scores se trouve entre 66.08 et 73.92.

---

### **Interprétation**

#### **Largeur de l’intervalle** :

La largeur de l’intervalle dépend de :

1. **Erreur standard ($ SE $)** : Une variabilité plus faible ($ \sigma $) ou un échantillon plus grand ($ n $) réduit l’intervalle.
2. **Niveau de confiance ($ z $)** : Un niveau de confiance plus élevé (par exemple, 99 %, avec $ z = 2.576 $) élargit l’intervalle.

#### **Signification** :

Un IC à 95 % ne signifie pas que la probabilité que la vraie moyenne soit dans l’intervalle est 95 %. Cela signifie que, sur de multiples échantillons, 95 % des intervalles construits contiendraient la vraie valeur.

---

### **Applications dans les jeux**

1. **Analyse des scores** :  
   Utiliser les IC pour estimer une plage probable pour la moyenne des performances des joueurs. Par exemple, comparer les scores moyens de différents groupes (débutants vs avancés).

2. **Validation des stratégies** :  
   Si une nouvelle stratégie produit un IC de scores plus élevé que l’ancienne, cela peut indiquer son efficacité.

3. **Prise de décision** :  
   Dans des jeux compétitifs, estimer les performances attendues pour déterminer la viabilité d’une stratégie ou d’une mécanique de jeu.

4. **Test de robustesse** :  
   Les IC peuvent être utilisés pour tester si une performance observée est significativement différente de la moyenne attendue.

### **Applications globales dans les jeux**

- **Évaluer la précision des estimations** : Fournir une plage probable pour les moyennes et proportions, en tenant compte de la variabilité des données.
- **Prédire les performances futures** : Identifier les performances probables d’un joueur ou d’une équipe sur la base des données actuelles.
- **Comparer des groupes** : Évaluer si deux groupes diffèrent significativement en comparant leurs IC respectifs.

---

## Analyser les résultats des statistiques descriptives

L’analyse des résultats des statistiques descriptives permet de résumer un ensemble de données pour en extraire les caractéristiques principales. Ces outils sont essentiels pour comprendre la structure des données, identifier des tendances et repérer des anomalies.

---

### **Comparaison des tendances centrales**

#### **Tendances centrales** :

- **Moyenne ($ \bar{x} $)** : Représente la valeur moyenne des données.
- **Médiane** : Point central des données triées, moins sensible aux valeurs extrêmes que la moyenne.

**Explication** :  
Comparer la moyenne et la médiane permet de détecter la symétrie ou l’asymétrie d’un jeu de données :

- Si $ \text{moyenne} = \text{médiane} $, les données sont généralement symétriques.
- Si $ \text{moyenne} > \text{médiane} $, les données sont asymétriques à droite (queue longue vers les grandes valeurs).
- Si $ \text{moyenne} < \text{médiane} $, les données sont asymétriques à gauche (queue longue vers les petites valeurs).

**Exemple** :  
Dans un jeu, les scores des joueurs sont $ [10, 15, 20, 25, 100] $ :

- Moyenne : $ \bar{x} = \frac{10 + 15 + 20 + 25 + 100}{5} = 34 $.
- Médiane : $ \text{médiane} = 20 $ (valeur centrale après tri).  
  La moyenne est nettement plus élevée que la médiane, suggérant un outlier à 100.

**Applications dans les jeux** :

- Identifier les performances typiques des joueurs.
- Comparer les stratégies basées sur les moyennes ou les médianes pour choisir les plus adaptées.

---

### **Analyse des écarts-types pour la dispersion**

#### **Écart-type ($ \sigma $)** :
$\sigma = \sqrt{\frac{1}{n} \sum\_{i=1}^n (x_i - \bar{x})^2}$
**Explication** :  
L’écart-type mesure la dispersion des données autour de la moyenne :

- Faible ($ \sigma $ bas) : Les valeurs sont regroupées près de la moyenne.
- Élevé ($ \sigma $ haut) : Les données sont dispersées.

**Exemple** :  
Dans un jeu, si deux groupes de joueurs ont les scores suivants :

- Groupe A : $ [18, 19, 20, 21, 22] $ ($ \sigma \approx 1.41 $).
- Groupe B : $ [10, 15, 20, 25, 30] $ ($ \sigma \approx 7.07 $).

Le groupe B a des performances plus variées, tandis que le groupe A est plus homogène.

**Applications dans les jeux** :

- Évaluer la régularité des performances des joueurs.
- Comparer la stabilité de différentes stratégies.

---

### **Détection des outliers via les boxplots ou $ Z $-scores**

#### **Boxplots**

Un boxplot visualise la répartition des données en montrant les quartiles, la médiane et les éventuels outliers. Un point est considéré comme un outlier s’il se trouve en dehors de l’intervalle :$[Q1 - 1.5 \cdot IQR, Q3 + 1.5 \cdot IQR]$où $ IQR = Q3 - Q1 $ est l’écart interquartile.

#### **$ Z $-scores**
$Z = \frac{x - \bar{x}}{\sigma}$
Un $ Z $-score mesure combien de fois une valeur s’écarte de la moyenne. Une valeur est souvent considérée comme un outlier si $ |Z| > 3 $.

**Exemple** :  
Dans un jeu, les scores $ [10, 15, 20, 25, 100] $ présentent un outlier à 100, détectable par :

- **Boxplot** : La valeur 100 se trouve bien au-dessus de $ Q3 + 1.5 \cdot IQR $.
- **$ Z $-score** : Pour $ \bar{x} = 34 $ et $ \sigma = 36 $,$  Z = \frac{100 - 34}{36} = 1.83 \ (\text{pas un outlier strict selon la règle } |Z| > 3).$
**Applications dans les jeux** :

- Repérer les performances anormalement élevées ou faibles.
- Identifier les valeurs qui pourraient biaiser les analyses.

---

### **Applications globales dans les jeux**

1. **Évaluer la performance des joueurs** :  
   Les tendances centrales (moyenne, médiane) fournissent un aperçu des résultats typiques et permettent de comparer différents groupes de joueurs.

2. **Analyser la variabilité** :  
   L’écart-type et la dispersion aident à identifier si une stratégie ou un joueur est fiable et constant.

3. **Repérer des anomalies** :  
   La détection des outliers via les boxplots ou $ Z $-scores permet de corriger ou d'expliquer des résultats inhabituels, comme une victoire écrasante ou un score exceptionnellement bas.

4. **Optimiser l’équilibrage** :  
   Comprendre la répartition des scores aide à équilibrer les mécanismes de jeu et à ajuster la difficulté.

---

## Analyser et évaluer les méthodes de détection des anomalies dans les données de séries temporelles

Les anomalies dans les séries temporelles représentent des valeurs inattendues qui s’écartent du comportement habituel. Leur détection est cruciale dans divers contextes, tels que la surveillance, l’analyse des performances, ou encore la détection de comportements inhabituels. Voici un aperçu des méthodes principales pour identifier ces anomalies.

---

### **$ Z $-score**

**Formule** :  $Z = \frac{x - \mu}{\sigma}$
- $ x $ : Valeur observée.
- $ \mu $ : Moyenne des données.
- $ \sigma $ : Écart-type.

**Critère** : Une valeur est considérée comme une anomalie si $ |Z| > 3 $, c’est-à-dire qu’elle est à plus de 3 écarts-types de la moyenne.

**Explication** :  
Le $ Z $-score exprime combien de fois une valeur s’écarte de la moyenne en termes d’écarts-types. Cela permet d’identifier les points qui diffèrent significativement du comportement général.

**Exemple** :  
Pour une série temporelle avec une moyenne $ \mu = 50 $ et un écart-type $ \sigma = 10 $, une valeur $ x = 85 $ donne :$Z = \frac{85 - 50}{10} = 3.5$Puisque $ |Z| > 3 $, $ x = 85 $ est une anomalie.

**Applications** :

- Détection de pics ou chutes soudains dans les performances des joueurs.
- Identification des défaillances inhabituelles dans un système de jeu.

---

### **Interquartile Range (IQR)**

**Formule** :  $IQR = Q3 - Q1$
- $ Q1 $ : Premier quartile (25e percentile).
- $ Q3 $ : Troisième quartile (75e percentile).

**Critère** : Une valeur est considérée comme une anomalie si :$x < Q1 - 1.5 \cdot IQR \quad \text{ou} \quad x > Q3 + 1.5 \cdot IQR$
**Explication** :  
L’IQR mesure la dispersion centrale des données. Toute valeur en dehors de $ [Q1 - 1.5 \cdot IQR, Q3 + 1.5 \cdot IQR] $ est considérée comme extrême. Contrairement au $ Z $-score, cette méthode ne repose pas sur l’hypothèse que les données suivent une distribution normale.

**Exemple** :  
Si $ Q1 = 30 $ et $ Q3 = 70 $, alors $ IQR = 40 $. Une valeur $ x = 10 $ est une anomalie car :$10 < Q1 - 1.5 \cdot IQR = 30 - 60 = -30$
**Applications** :

- Identifier les comportements extrêmes des joueurs (par exemple, un temps de réaction exceptionnellement court ou long).
- Détection des anomalies dans des distributions asymétriques ou non gaussiennes.

---

### **Pourcentage du maximum**

**Définition** :  
Cette méthode compare chaque valeur à un seuil basé sur un pourcentage du maximum observé dans les données.

**Critère** : Une valeur est considérée comme une anomalie si elle dépasse un seuil prédéfini, souvent 90 % ou 95 % du maximum.

**Explication** :  
Cette méthode est simple et adaptée lorsque les données ont une limite supérieure naturelle ou attendue.

**Exemple** :  
Dans une série temporelle avec un maximum observé de $ 100 $, toute valeur supérieure à $ 90 $ (90 % du maximum) pourrait être marquée comme une anomalie si le seuil est fixé à 90 %.

**Applications** :

- Surveillance des pics de charge serveur ou de consommation de ressources.
- Identification des scores exceptionnellement élevés dans un contexte compétitif.

---

### **Statistiques robustes**

**Définition** :  
Les statistiques robustes, comme la médiane et la médiane absolue des écarts (MAD), sont utilisées pour détecter les anomalies sans être influencées par les valeurs extrêmes existantes.

#### **Formule du MAD** :

$MAD = \text{médiane}(|x_i - \text{médiane}(x)|)$

**Critère** : Une valeur est une anomalie si $ |x - \text{médiane}| > k \cdot MAD $, où $ k $ est un facteur (souvent $ k = 3 $).

**Explication** :  
Contrairement au $ Z $-score, les statistiques robustes ne sont pas sensibles aux outliers déjà présents, ce qui en fait un outil idéal pour les données asymétriques ou fortement bruitées.

**Exemple** :  
Dans une série temporelle où la médiane est $ 50 $ et $ MAD = 5 $, une valeur $ x = 70 $ est une anomalie car :$|70 - 50| = 20 > 3 \cdot 5 = 15$
**Applications** :

- Détection des comportements anormaux dans des environnements de jeu où les données sont asymétriques.
- Identification des anomalies dans les données fortement bruitées (par exemple, les clics par seconde ou les réponses des joueurs).
