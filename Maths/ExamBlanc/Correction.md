# **Correction de l'examen blanc de Statistiques et Probabilités**

---

### **Exercice 1 : Probabilité simple (3 points)**  

1. **Probabilité de tirer une boule rouge :**  
   Total des boules : \( 5 + 4 + 3 = 12 \).  
   \( P(\text{rouge}) = \frac{5}{12} \).  

   **Réponse : \( \frac{5}{12} \) ou environ 0,4167 (41,67 %)**  

2. **Probabilité de ne pas tirer une boule verte :**  
   \( P(\text{pas verte}) = 1 - P(\text{verte}) = 1 - \frac{3}{12} = \frac{9}{12} = \frac{3}{4} \).  

   **Réponse : \( \frac{3}{4} \) ou 0,75 (75 %)**
   
3. **Probabilité que la première soit rouge et la seconde bleue :**  
   \( P(\text{rouge puis bleu}) = P(\text{rouge}) \times P(\text{bleu | rouge}) \).  
   \( P(\text{rouge}) = \frac{5}{12} \), \( P(\text{bleu | rouge}) = \frac{4}{11} \).  
   \( P(\text{rouge puis bleu}) = \frac{5}{12} \times \frac{4}{11} = \frac{20}{132} = \frac{5}{33} \).  

   **Réponse : \( \frac{5}{33} \) ou environ 0,1515 (15,15 %)**
   
---

### **Exercice 2 : Loi binomiale (4 points)**  

\( n = 5 \), \( p = 0,7 \). La variable suit une loi binomiale \( B(5, 0,7) \).  

1. **Probabilité de réussir exactement 3 coups :**  
   \( P(X = 3) = \binom{5}{3} \cdot (0,7)^3 \cdot (0,3)^2 \).  
   \( \binom{5}{3} = 10 \).  
   \( P(X = 3) = 10 \cdot 0,343 \cdot 0,09 = 0,3087 \).  

   **Réponse : \( 0,3087 \) (30,87 %)**
   
2. **Probabilité de réussir au moins 4 coups :**  
   \( P(X \geq 4) = P(X = 4) + P(X = 5) \).  
   \( P(X = 4) = \binom{5}{4} \cdot (0,7)^4 \cdot (0,3)^1 = 5 \cdot 0,2401 \cdot 0,3 = 0,36015 \).  
   \( P(X = 5) = \binom{5}{5} \cdot (0,7)^5 \cdot (0,3)^0 = 1 \cdot 0,16807 \cdot 1 = 0,16807 \).  
   \( P(X \geq 4) = 0,36015 + 0,16807 = 0,52822 \).  

   **Réponse : \( 0,5282 \) (52,82 %)**
   
---

### **Exercice 3 : Statistiques descriptives (5 points)**  

Scores : \( 12, 15, 20, 25, 30, 35, 50 \).  

1. **Moyenne, médiane et écart-type :**  
   - Moyenne :  
     \( \text{Moyenne} = \frac{12 + 15 + 20 + 25 + 30 + 35 + 50}{7} = \frac{187}{7} = 26,71 \).  

   - Médiane :  
     Les scores ordonnés sont déjà classés. La médiane est le score central : **25**.  

   - Écart-type :  
     \( \sigma = \sqrt{\frac{\sum (x_i - \bar{x})^2}{n}} \), avec \( \bar{x} = 26,71 \).  
     \( \sigma \approx 12,90 \).  

     **Réponse : Moyenne = \( 26,71 \), Médiane = \( 25 \), Écart-type = \( 12,90 \)**  

2. **Détection des outliers (méthode IQR) :**  
   - \( Q1 = 20 \), \( Q3 = 35 \), \( IQR = Q3 - Q1 = 15 \).  
   - Limites :  
     \( \text{Limite inférieure} = Q1 - 1,5 \cdot IQR = 20 - 22,5 = -2,5 \).  
     \( \text{Limite supérieure} = Q3 + 1,5 \cdot IQR = 35 + 22,5 = 57,5 \).  

   Aucun score ne dépasse ces limites. **Aucun outlier.**

---

### **Exercice 4 : Loi normale (4 points)**  

\( \mu = 75 \), \( \sigma = 10 \).  

1. **Probabilité qu’un score soit supérieur à 85 :**  
   \( Z = \frac{85 - 75}{10} = 1 \).  
   \( P(X > 85) = 1 - P(Z \leq 1) = 1 - 0,8413 = 0,1587 \).  

   **Réponse : \( 0,1587 \) (15,87 %)**
   
2. **Probabilité qu’un score soit entre 70 et 90 :**  
   \( Z_1 = \frac{70 - 75}{10} = -0,5 \), \( Z_2 = \frac{90 - 75}{10} = 1,5 \).  
   \( P(70 \leq X \leq 90) = P(Z \leq 1,5) - P(Z \leq -0,5) \).  
   \( P(Z \leq 1,5) = 0,9332 \), \( P(Z \leq -0,5) = 0,3085 \).  
   \( P(70 \leq X \leq 90) = 0,9332 - 0,3085 = 0,6247 \).  

   **Réponse : \( 0,6247 \) (62,47 %)**
   
---

### **Exercice 5 : Régression linéaire (4 points)**  

1. **Équation de la droite de régression :**  
   \( \bar{x} = \frac{1 + 2 + 3 + 4}{4} = 2,5 \), \( \bar{y} = \frac{12 + 15 + 19 + 25}{4} = 17,75 \).  
   \( S_{xy} = \sum (x_i - \bar{x})(y_i - \bar{y}) = 26,5 \), \( S_{xx} = \sum (x_i - \bar{x})^2 = 5 \).  
   \( a = \frac{S_{xy}}{S_{xx}} = \frac{26,5}{5} = 5,3 \).  
   \( b = \bar{y} - a \cdot \bar{x} = 17,75 - 5,3 \cdot 2,5 = 4 \).  
   **Équation : \( y = 5,3x + 4 \)**  

2. **Prédiction pour \( x = 5 \) :**  
   \( y = 5,3 \cdot 5 + 4 = 26,5 + 4 = 30,5 \).  

   **Réponse : \( y = 30,5 \)**  
