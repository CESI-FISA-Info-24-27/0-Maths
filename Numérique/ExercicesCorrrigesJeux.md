# Exercices corrigés de théorie des jeux

### **Exercice 1 : Identification d'un équilibre de Nash simple**  
Deux joueurs choisissent simultanément entre deux stratégies : **A** et **B**. La matrice de gains est la suivante :  

|                | **A (Joueur 2)** | **B (Joueur 2)** |
|----------------|------------------|------------------|
| **A (Joueur 1)** | \( (3, 3) \)      | \( (1, 4) \)      |
| **B (Joueur 1)** | \( (4, 1) \)      | \( (2, 2) \)      |

1. Déterminez l’équilibre de Nash de ce jeu.
2. Justifiez si une stratégie dominante existe pour l’un ou les deux joueurs.

<details>
<summary>Solution</summary>

#### **Rappel de cours : Équilibre de Nash**
Un équilibre de Nash est atteint lorsque chaque joueur adopte une stratégie optimale donnée la stratégie de l'autre, et qu'aucun joueur ne peut améliorer son gain en changeant unilatéralement de stratégie.

---

#### **Étape 1 : Analyser les stratégies des joueurs**
- Si le **Joueur 2** choisit **A** :  
  Le **Joueur 1** compare \(3\) (s’il joue \(A\)) et \(4\) (s’il joue \(B\)). Il choisit donc \(B\).  

- Si le **Joueur 2** choisit **B** :  
  Le **Joueur 1** compare \(1\) (s’il joue \(A\)) et \(2\) (s’il joue \(B\)). Il choisit donc \(B\).

- Si le **Joueur 1** choisit **A** :  
  Le **Joueur 2** compare \(3\) (s’il joue \(A\)) et \(4\) (s’il joue \(B\)). Il choisit donc \(B\).

- Si le **Joueur 1** choisit **B** :  
  Le **Joueur 2** compare \(1\) (s’il joue \(A\)) et \(2\) (s’il joue \(B\)). Il choisit donc \(B\).

---

#### **Étape 2 : Identifier les points stables**
- Lorsque \(J1 = B\) et \(J2 = B\), aucun joueur n’a intérêt à dévier :  
  - Si \(J1\) change à \(A\), son gain passe de \(2\) à \(1\).  
  - Si \(J2\) change à \(A\), son gain passe de \(2\) à \(1\).  
  **Conclusion :** \( (B, B) \) est un équilibre de Nash avec un gain de \( (2, 2) \).

---

#### **Étape 3 : Vérifier les stratégies dominantes**
Une stratégie est dominante si elle donne un meilleur résultat que toutes les autres stratégies, quel que soit le choix de l’autre joueur.  
- **Pour \(Joueur 1\)** :  
  - \(B\) domine \(A\) car \(4 > 3\) et \(2 > 1\).  
- **Pour \(Joueur 2\)** :  
  - \(B\) domine \(A\) car \(4 > 3\) et \(2 > 1\).

**Conclusion :** Chaque joueur a une stratégie dominante, et elle correspond à \(B\).
</details>

---

### **Exercice 2 : Suppression des stratégies dominées**  
La matrice de gains suivante représente un jeu simultané entre deux joueurs :

|                | **A (Joueur 2)** | **B (Joueur 2)** | **C (Joueur 2)** |
|----------------|------------------|------------------|------------------|
| **A (Joueur 1)** | \( (4, 4) \)      | \( (1, 5) \)      | \( (0, 3) \)      |
| **B (Joueur 1)** | \( (2, 1) \)      | \( (3, 3) \)      | \( (1, 2) \)      |
| **C (Joueur 1)** | \( (5, 0) \)      | \( (0, 1) \)      | \( (3, 4) \)      |

1. Supprimez les stratégies strictement dominées.
2. Identifiez tous les équilibres de Nash.

<details>
<summary>Solution</summary>

#### **Rappel de cours : Stratégies dominées**
Une stratégie est strictement dominée si, quel que soit le choix des autres joueurs, il existe une autre stratégie qui offre un gain strictement supérieur.

---

#### **Étape 1 : Identifier les stratégies dominées pour le joueur 1**
- Comparons les gains des stratégies \(A\), \(B\), et \(C\) pour le joueur 1 :
  - \(A\) donne de meilleurs gains que \(B\) dans toutes les situations :  
    \(4 > 2\), \(1 > 0\), et \(0 > 1\).  
    **Conclusion :** \(B\) est strictement dominée et peut être éliminée.

---

#### **Étape 2 : Identifier les stratégies dominées pour le joueur 2**
- Comparons les gains des stratégies \(A\), \(B\), et \(C\) pour le joueur 2 :  
  - \(A\) donne de meilleurs gains que \(C\) dans toutes les situations :  
    \(4 > 0\), \(5 > 3\), et \(3 > 2\).  
    **Conclusion :** \(C\) est strictement dominée et peut être éliminée.

---

#### **Étape 3 : Simplifier la matrice**
Après suppression des stratégies dominées, la matrice devient :  

|                | **A (Joueur 2)** | **B (Joueur 2)** |
|----------------|------------------|------------------|
| **A (Joueur 1)** | \( (4, 4) \)      | \( (1, 5) \)      |
| **C (Joueur 1)** | \( (5, 0) \)      | \( (0, 1) \)      |

---

#### **Étape 4 : Identifier les équilibres de Nash**
- Pour \(J2 = A\), \(J1\) choisit \(C\) (gain \(5 > 4\)).  
- Pour \(J2 = B\), \(J1\) choisit \(A\) (gain \(1 > 0\)).  
- Pour \(J1 = A\), \(J2\) choisit \(B\) (gain \(5 > 4\)).  
- Pour \(J1 = C\), \(J2\) choisit \(A\) (gain \(0 > 1\)).

**Équilibres de Nash :**  
1. \( (A, A) \) avec un gain \( (4, 4) \).  
2. \( (C, B) \) avec un gain \( (0, 1) \).
</details>

---

### **Exercice 3 : Jeu séquentiel avec arbre de décision**  
Deux entreprises décident séquentiellement d’investir ou non dans un nouveau marché. L’arbre de décision est le suivant :

1. Entreprise A choisit d’investir ou non.  
2. Si A investit, entreprise B choisit de réagir ou non.  

Les gains sont les suivants :  
- Si A investit et B réagit : \( (3, 2) \).  
- Si A investit et B ignore : \( (5, 0) \).  
- Si A n’investit pas : \( (1, 1) \).  

Trouvez l’équilibre parfait en sous-jeux.

<details>
<summary>Solution</summary>

#### **Rappel de cours : Jeu séquentiel et équilibre parfait en sous-jeux**
- Un jeu séquentiel se joue en plusieurs étapes, chaque joueur observant les décisions précédentes.  
- L’équilibre parfait en sous-jeux (EPS) est une extension de l’équilibre de Nash applicable à chaque sous-jeu.

---

#### **Étape 1 : Identifier les sous-jeux**
- Si \(A\) investit, \(B\) a deux choix :  
  - Réagir (gain \(3, 2\)).  
  - Ignorer (gain \(5, 0\)).  

#### **Étape 2 : Optimiser le choix de \(B\)**
- \(B\) maximise son gain en **réagissant** (\(2 > 0\)).  
  **Conclusion pour \(B\)** : Si \(A\) investit, \(B\) réagit.

---

#### **Étape 3 : Optimiser le choix de \(A\)**
- \(A\) anticipe la réponse optimale de \(B\) :  
  - Si \(A\) investit : Gain \(3\).  
  - Si \(A\) n’investit pas : Gain \(1\).  
  **Conclusion pour \(A\)** : \(A\) investit.

---

#### **Étape 4 : Équilibre parfait en sous-jeux**
- Stratégie optimale : \(A\) investit, \(B\) réagit.

  
- **Gain final : \( (3, 2) \)**.
</details>

---

### **Exercice 4 : Jeu coopératif et coalition**  
Trois joueurs \(A\), \(B\), et \(C\) peuvent former des coalitions pour maximiser leurs gains. Les gains potentiels sont :  
- \(v(\{A, B\}) = 5\), \(v(\{A, C\}) = 4\), \(v(\{B, C\}) = 6\), \(v(\{A, B, C\}) = 8\).  

1. Trouvez la coalition optimale.  
2. Répartissez les gains selon le noyau.

<details>
<summary>Solution</summary>

#### **Rappel de cours : Jeux coopératifs et coalition**
- Une coalition est un groupe de joueurs qui coopèrent pour maximiser leur utilité.  
- Le noyau est un ensemble de répartitions des gains où aucun sous-groupe n’a intérêt à dévier.

---

#### **Étape 1 : Coalition optimale**
- La valeur maximale est obtenue avec \( \{A, B, C\} \), gain \(8\).

---

#### **Étape 2 : Répartition selon le noyau**
- Une répartition \( (x_A, x_B, x_C) \) est dans le noyau si :  
  - \(x_A + x_B + x_C = 8\).  
  - \(x_A + x_B \geq 5\), \(x_A + x_C \geq 4\), \(x_B + x_C \geq 6\).  

- \(x_A = 2\), \(x_B = 3\), \(x_C = 3\) satisfait toutes les conditions.  

**Répartition finale : \( (2, 3, 3) \)**.
</details>

---