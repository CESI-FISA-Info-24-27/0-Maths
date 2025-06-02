# Maths et Cryptographie

## Objectifs pédagogiques

À l’issue de cette séquence, vous serez capable de :

- Expliquer les théorèmes fondamentaux utilisés en cryptographie (Euler, Euclide, Fermat)
- Identifier des nombres premiers spéciaux (Mersenne, Fermat, Sophie Germain)
- Appliquer ces notions à des systèmes de chiffrement simples (RSA)
- Implémenter un mini-système RSA en Python

## Introduction à la cryptographie

### Qu’est-ce que la cryptographie ?

La cryptographie est une branche des mathématiques appliquées et de l'informatique qui s'intéresse aux techniques de **protection de l'information**. Son objectif est de transformer un message de manière à ce qu’il ne puisse être compris que par des personnes autorisées, même en présence d’un adversaire ayant accès aux données chiffrées.

Elle repose sur des concepts fondamentaux tels que la **théorie des nombres**, **l’arithmétique modulaire**, et les **algorithmes informatiques**, et elle constitue un pilier de la sécurité des systèmes d'information.

### Domaines d’application

- Sécurisation des communications (messageries, protocoles HTTPS, VPN)
- Authentification (signatures numériques, certificats X.509)
- Stockage sécurisé des données (bases de données, fichiers chiffrés)
- Transactions électroniques (paiement, blockchain)

### Objectifs de la cryptographie

1. **Confidentialité**
   Garantir que seuls les destinataires légitimes peuvent accéder au contenu du message. Cela repose principalement sur des techniques de chiffrement.

2. **Authenticité**
   Vérifier que le message a bien été envoyé par l’émetteur prétendu. Cela implique l’usage de mécanismes d’authentification, souvent via des clés cryptographiques ou des signatures numériques.

3. **Intégrité**
   Détecter toute modification (intentionnelle ou non) du message lors de son transport ou de son stockage. On utilise pour cela des fonctions de hachage et des codes d’authentification de message (MAC).

4. **Non-répudiation**
   Empêcher un utilisateur d’un système de nier avoir effectué une action (par exemple, l’envoi d’un message). Elle repose généralement sur les signatures numériques et les journaux horodatés.

## Théorèmes fondamentaux en cryptographie

La cryptographie moderne repose sur des fondements mathématiques solides, principalement issus de la **théorie des nombres**. Cette section présente trois résultats fondamentaux qui interviennent dans de nombreux algorithmes de chiffrement : l’algorithme d’Euclide, le petit théorème de Fermat, et la fonction indicatrice d’Euler.

### Algorithme d’Euclide – Calcul du PGCD

L'algorithme d’Euclide permet de calculer le **plus grand commun diviseur (PGCD)** de deux entiers. C’est un algorithme fondamental utilisé dans la génération des clés asymétriques, notamment pour :

- Vérifier que deux entiers sont **premiers entre eux**
- Calculer un **inverse modulaire**, ce qui est indispensable dans RSA

#### Principe

L'algorithme repose sur la propriété suivante :

> Soit `a` et `b` deux entiers naturels avec `a ≥ b > 0`, alors :
>
> `pgcd(a, b) = pgcd(b, a mod b)`

L’algorithme s’exécute en temps logarithmique (O(log min(a, b))), ce qui en fait un choix très efficace même pour de grands entiers.

#### Exemple

Calcul du PGCD de 252 et 105 :

```
252 = 2 × 105 + 42
105 = 2 × 42 + 21
42  = 2 × 21 + 0
=> PGCD(252, 105) = 21
```

### Petit théorème de Fermat

Le petit théorème de Fermat est un résultat central en **arithmétique modulaire**, et l’un des fondements mathématiques de nombreux algorithmes cryptographiques, notamment RSA. Il donne une propriété remarquable des puissances d’un entier modulo un nombre premier.

#### Énoncé

Soit `p` un nombre premier, et soit `a` un entier tel que `a` n’est pas divisible par `p` (c’est-à-dire `pgcd(a, p) = 1`). Alors :

```
a^(p−1) ≡ 1 mod p
```

Autrement dit, si `p` est premier et `a` est un entier non nul modulo `p`, alors `a` élevé à la puissance `p−1` est congru à 1 modulo `p`.

#### Justification mathématique

L'idée repose sur la structure **du groupe multiplicatif des inversibles modulo `p`**, noté `(ℤ/pℤ)⁎`. Ce groupe contient `p−1` éléments (les entiers de `1` à `p−1`) et est **cyclique** (il existe un générateur `g` tel que chaque élément est une puissance de `g`).

##### Méthode 1 : Justification par multiplication de classes

Soit l’ensemble des entiers `{1, 2, ..., p−1}`. Tous sont **inversibles modulo `p`**, car `p` est premier.

On considère alors l’application suivante :

```
∀x ∈ {1, ..., p−1}, f(x) = a·x mod p
```

Comme `a` est premier avec `p`, cette application est une **bijection** de l’ensemble `{1, ..., p−1}` vers lui-même (on peut démontrer que `f` est injective modulo `p`, donc bijective sur un ensemble fini).

Ainsi :

```
a × 1 × a × 2 × ... × a × (p−1) ≡ 1 × 2 × ... × (p−1) mod p
```

Ce qui donne :

```
a^(p−1) × (p−1)! ≡ (p−1)! mod p
```

Comme `(p−1)!` est non nul modulo `p` (et premier avec `p`), on peut simplifier :

```
a^(p−1) ≡ 1 mod p
```

##### Méthode 2 : Justification par théorie des groupes

On considère le groupe multiplicatif `(ℤ/pℤ)⁎` de cardinal `p−1`. Par le **théorème de Lagrange**, tout élément `a` de ce groupe satisfait :

```
a^{|G|} = a^{p−1} ≡ 1 mod p
```

Cela découle du fait que l’ordre de tout élément divise l’ordre du groupe, et que l’élévation à la puissance `p−1` donne l’élément neutre du groupe, soit 1.

Cette approche justifie pleinement le résultat du petit théorème de Fermat via la structure algébrique sous-jacente.

#### Applications

1. **Tests de primalité**
   Si `n` est un entier et `a` un entier < `n`, on peut tester :

   ```
   a^(n−1) ≡ 1 mod n ?
   ```

   Si l’égalité est fausse, alors `n` est **composé**.
   Si elle est vraie pour plusieurs `a`, `n` est **probablement premier** (attention aux pseudopremiers et nombres de Carmichael).

2. **RSA et calcul d’inverses**
   Le petit théorème de Fermat permet d’obtenir l’inverse de `a mod p` :

   ```
   a^(p−2) ≡ a⁻¹ mod p
   ```

   Cela évite d’utiliser l’algorithme d’Euclide étendu dans certains cas.

3. **Sécurité**
   Le théorème garantit que l’exponentiation dans un groupe fini ne sort pas du cadre modulaire, propriété essentielle pour les algorithmes de **chiffrement asymétrique**.

#### Exemple complet

Prenons `p = 7` (nombre premier) et `a = 3` (premier avec 7).

```
3^6 = 729
729 mod 7 = 1
```

En effet :

```
729 = 104 × 7 + 1 ⇒ 3^6 ≡ 1 mod 7
```

Ce qui confirme le théorème.

#### Lien avec le théorème d’Euler

Le petit théorème de Fermat est un **cas particulier** du théorème d’Euler :

```
a^φ(n) ≡ 1 mod n   (si pgcd(a, n) = 1)
```

Lorsque `n` est premier, alors `φ(n) = n−1`, et on retrouve le résultat de Fermat :

```
a^(p−1) ≡ 1 mod p
```

## Fonction indicatrice d’Euler (φ)

La **fonction indicatrice d’Euler**, notée φ(n), est une fonction arithmétique fondamentale en cryptographie. Elle intervient directement dans la construction du système RSA, et plus généralement dans tout contexte où l’on travaille avec les éléments inversibles modulo un entier.

### Définition

Pour un entier naturel `n ≥ 1`, la fonction φ(n) est définie comme le **nombre d'entiers `k` avec `1 ≤ k ≤ n` tels que `pgcd(k, n) = 1`**.

Autrement dit, φ(n) est le **nombre d’entiers strictement inférieurs à `n` qui sont premiers avec `n`** (ou encore : d’inversibles modulo `n`).

### Exemples

- φ(1) = 1
  (seul 1 est ≤ 1 et premier avec 1)

- φ(6) = 2
  Les entiers premiers avec 6 sont : 1, 5

- φ(7) = 6
  Puisque 7 est premier, tous les entiers de 1 à 6 sont premiers avec 7

### Propriétés fondamentales

#### 1. Si `p` est premier alors

```
φ(p) = p − 1
```

Car tout entier < `p` est premier avec `p`.

#### 2. Si `p` est premier et `k ≥ 1`

```
φ(p^k) = p^k − p^{k−1} = p^k (1 − 1/p)
```

#### 3. **Multiplicativité**

Si `m` et `n` sont **premiers entre eux**, alors :

```
φ(m × n) = φ(m) × φ(n)
```

C’est une propriété essentielle qui permet de calculer φ(n) à partir de la décomposition en facteurs premiers de `n`.

#### 4. Pour un entier `n = p₁^α₁ × p₂^α₂ × ... × p_k^α_k` (décomposition en facteurs premiers), alors :

```
φ(n) = n × ∏ (1 − 1/pᵢ)
```

Exemple avec `n = 60 = 2^2 × 3 × 5` :

```
φ(60) = 60 × (1 − 1/2) × (1 − 1/3) × (1 − 1/5)
       = 60 × 1/2 × 2/3 × 4/5
       = 60 × (1/2 × 2/3 × 4/5) = 60 × 4/15 = 16
```

### Rôle dans RSA

Dans le chiffrement RSA, on choisit deux nombres premiers `p` et `q`, et on définit `n = p × q`. Le produit `n` est utilisé comme **modulus** commun pour les clés publique et privée.

La sécurité du système repose sur le fait que :

- Le chiffrement se fait avec un exposant `e`, tel que `1 < e < φ(n)` et `pgcd(e, φ(n)) = 1`
- Le déchiffrement repose sur le calcul de l’inverse de `e` modulo `φ(n)`, noté `d`, tel que :

```
e × d ≡ 1 mod φ(n)
```

Cette étape est possible **uniquement** si φ(n) est connu, ce qui suppose de connaître les facteurs premiers de `n`. Cela garantit la sécurité du système RSA : tant que `n` est difficile à factoriser, φ(n) est inconnu, donc `d` est difficile à calculer.

### Exemple complet

Prenons `p = 11` et `q = 17` (nombres premiers)

- `n = p × q = 11 × 17 = 187`
- `φ(n) = (p − 1)(q − 1) = 10 × 16 = 160`

Soit `e = 7` (premier avec 160), alors on peut calculer `d`, l'inverse modulaire de 7 modulo 160, tel que :

```
7 × d ≡ 1 mod 160
```

Le chiffrement d’un message `m` (avec `m < n`) se fait par :

```
c = m^e mod n
```

Le déchiffrement par :

```
m = c^d mod n
```

### Justification théorique : le théorème d’Euler

Le lien avec la cryptographie est renforcé par le **théorème d’Euler**, qui généralise le petit théorème de Fermat :

> Si `a` est premier avec `n`, alors :

```
a^φ(n) ≡ 1 mod n
```

Ce résultat est utilisé pour garantir que l’exponentiation `a^e` suivie de `a^d` revient au message initial `a`, modulo `n`, si `e × d ≡ 1 mod φ(n)`.

## Nombres premiers spéciaux

Les **nombres premiers spéciaux** sont des classes particulières de nombres premiers qui présentent des propriétés algébriques intéressantes. En cryptographie, ils sont utilisés pour :

- Gagner en performance dans les algorithmes de génération de clés
- Optimiser certains tests de primalité
- Protéger contre certaines attaques en augmentant la robustesse des clefs

On s’intéressera ici à trois familles classiques : les nombres premiers de Mersenne, de Fermat et de Sophie Germain.

### Nombres premiers de Mersenne

Un **nombre de Mersenne** est un nombre de la forme :

```
M_p = 2^p − 1
```

où `p` est un entier **premier**.

#### Exemples :

| p   | M_p = 2^p − 1 | Premier ? |
| --- | ------------- | --------- |
| 2   | 3             | Oui       |
| 3   | 7             | Oui       |
| 5   | 31            | Oui       |
| 6   | 63            | Non       |
| 7   | 127           | Oui       |

Seuls certains `M_p` sont premiers. **Si `M_p` est premier, alors `p` doit être premier**, mais l'inverse n'est pas toujours vrai : `p = 11` donne `M₁₁ = 2047 = 23 × 89`, donc non premier.

#### Utilisation

- Génération de grands nombres premiers dans les systèmes à clefs longues (ex : RSA, Diffie-Hellman)
- Tests de primalité rapides (Lucas-Lehmer pour les Mersenne)

### Nombres premiers de Fermat

Les **nombres de Fermat** sont définis par :

```
F_n = 2^{2^n} + 1
```

#### Exemples

| n   | F_n = 2^{2^n} + 1 | Valeur        | Premier ?          |
| --- | ----------------- | ------------- | ------------------ |
| 0   | 2^1 + 1           | 3             | Oui                |
| 1   | 2^2 + 1           | 5             | Oui                |
| 2   | 2^4 + 1           | 17            | Oui                |
| 3   | 2^8 + 1           | 257           | Oui                |
| 4   | 2^16 + 1          | 65537         | Oui                |
| 5   | 2^32 + 1          | 4 294 967 297 | Non (div. par 641) |

À ce jour, seuls les 5 premiers `F_n` sont premiers. Aucun autre n’a été trouvé premier depuis.

#### Intérêt

- En théorie des nombres : construction de polygones réguliers (Gauss)
- En cryptographie, certains protocoles exploitent la simplicité binaire de ces nombres

### Nombres premiers de Sophie Germain

Un **nombre premier de Sophie Germain** est un entier `p` tel que `2p + 1` est également premier.

Dans ce cas, `2p + 1` est appelé un **nombre premier sûr** (_safe prime_).

#### Exemples

| p   | 2p + 1 | Premier ? |
| --- | ------ | --------- |
| 2   | 5      | Oui       |
| 3   | 7      | Oui       |
| 5   | 11     | Oui       |
| 11  | 23     | Oui       |
| 23  | 47     | Oui       |
| 29  | 59     | Oui       |
| 41  | 83     | Oui       |

#### Utilisation en cryptographie

- Clés RSA/Diffie-Hellman résistantes à certaines attaques
- Construction de **groupes cycliques sûrs**, utilisés notamment dans le protocole **DH (Diffie-Hellman)**, où la présence de sous-groupes de petit ordre peut compromettre la sécurité si les nombres premiers ne sont pas bien choisis

### Récapitulatif

| Type               | Formule                                | Usage principal                                              |
| ------------------ | -------------------------------------- | ------------------------------------------------------------ |
| **Mersenne**       | `2^p − 1`                              | Grands nombres premiers, tests de primalité                  |
| **Fermat**         | `2^{2^n} + 1`                          | Théorie des nombres, quelques usages cryptographiques        |
| **Sophie Germain** | `p` tel que `2p + 1` est aussi premier | Groupes sûrs, résistance aux attaques sur Diffie-Hellman/RSA |

## Application à la cryptographie asymétrique : RSA

RSA est un système de chiffrement asymétrique dont la sécurité repose sur des résultats fondamentaux en **arithmétique modulaire**, notamment le **théorème d’Euler** et l’**inexistence d’un algorithme efficace de factorisation** des grands entiers. Il est utilisé à grande échelle dans les systèmes sécurisés (protocoles SSL/TLS, PGP, signatures numériques, etc.).

### Objectif de RSA

RSA vise à permettre deux opérations fondamentales :

- **Chiffrer un message avec une clé publique** que tout le monde peut connaître
- **Déchiffrer ce message uniquement avec une clé privée**, conservée secrète

Ces opérations doivent satisfaire une propriété essentielle :

> Soit `m` un message, `e` l’exposant public, `d` l’exposant privé, et `n` le modulus :
>
> ```
> m^(e·d) ≡ m mod n
> ```

Autrement dit, `m` peut être retrouvé **sans perte d’information** après chiffrement puis déchiffrement. Cette propriété repose sur le **théorème d’Euler**, qui garantit que `m^φ(n) ≡ 1 mod n` si `pgcd(m, n) = 1`.

### Détail de la génération des clés

#### Étape 1 – Choix de deux grands nombres premiers

On choisit deux entiers premiers `p` et `q` suffisamment grands (typiquement de 1024 bits chacun).

```
n = p × q
```

Le nombre `n` est le **modulus** commun à la clé publique et à la clé privée. Il doit être rendu public.

#### Étape 2 – Calcul de φ(n)

Comme `p` et `q` sont premiers :

```
φ(n) = (p − 1)(q − 1)
```

Cette valeur est **secrète**, car elle dépend directement de la factorisation de `n`.

#### Étape 3 – Choix de l’exposant `e`

On choisit un entier `e` tel que :

- `1 < e < φ(n)`
- `pgcd(e, φ(n)) = 1` (e est premier avec φ(n))

Ce `e` constitue l’**exposant de chiffrement**, et fait partie de la **clé publique**. En pratique, des valeurs standards sont souvent utilisées pour `e`, comme `65537`, car elles permettent une exponentiation modulaire rapide avec un nombre réduit de bits à 1.

#### Étape 4 – Calcul de l’exposant `d`

On cherche l’inverse modulaire de `e` modulo `φ(n)`, c’est-à-dire `d` tel que :

```
e × d ≡ 1 mod φ(n)
```

Cela signifie que `d` est la **solution de l’équation de Bézout** : `e·d − φ(n)·k = 1` pour un certain entier `k`. On le calcule via **l’algorithme d’Euclide étendu**.

Ce `d` est **conservé secret** et constitue la **clé privée**.

### Résumé des clés

- Clé **publique** : paire (n, e)

  - utilisée pour chiffrer
  - rendue publique

- Clé **privée** : paire (n, d)

  - utilisée pour déchiffrer
  - conservée secrète

### Fonctionnement du chiffrement RSA

Soit `m` un message tel que `0 ≤ m < n`. On effectue :

#### Chiffrement

```
c = m^e mod n
```

#### Déchiffrement

```
m = c^d mod n = (m^e)^d mod n = m^{ed} mod n
```

#### Justification mathématique

- On a `ed ≡ 1 mod φ(n)`, donc il existe un entier `k` tel que `ed = 1 + k·φ(n)`

- On élève `m` à la puissance `ed` :

  ```
  m^{ed} = m^{1 + k·φ(n)} = m · (m^{φ(n)})^k
  ```

- Par le théorème d’Euler, si `pgcd(m, n) = 1`, alors `m^{φ(n)} ≡ 1 mod n`, donc :

  ```
  m^{ed} ≡ m · 1^k ≡ m mod n
  ```

Ce résultat garantit la **réversibilité** du chiffrement RSA pour tous `m` tels que `pgcd(m, n) = 1`. En pratique, cela est toujours vrai si `m < n` et `p`, `q` sont correctement choisis.

### Remarques techniques

- **Chiffrement de gros messages** :
  RSA ne chiffre pas des fichiers entiers. Il est utilisé pour chiffrer une **clé de session symétrique** (AES), qui elle-même servira à chiffrer les données. C’est le principe de l’**hybrid encryption**.

- **Padding** :
  Pour éviter des attaques déterministes, le message `m` est **préparé** avant chiffrement (ajout de bits aléatoires, normes comme **PKCS#1**, **OAEP**).

- **Attaques connues** :

  - Attaque par factorisation de `n`
  - Attaque par faible `e` si le padding est mal appliqué
  - Attaques de canal auxiliaire (side-channel : consommation, temps, rayonnement…)

## Implémentation Python (mini-RSA)

```python
def pgcd(a, b):
    while b != 0:
        a, b = b, a % b
    return a

def euclide_etendu(a, b):
    if b == 0:
        return (1, 0)
    x1, y1 = euclide_etendu(b, a % b)
    x, y = y1, x1 - (a // b) * y1
    return x, y

def modinv(e, phi):
    x, _ = euclide_etendu(e, phi)
    return x % phi

# Exemples avec p=11, q=17
p, q = 11, 17
n = p * q
phi = (p - 1) * (q - 1)
e = 7
d = modinv(e, phi)

# Chiffrement/déchiffrement
m = 8
c = pow(m, e, n)
m_dechiffre = pow(c, d, n)

print("Message initial :", m)
print("Chiffré :", c)
print("Déchiffré :", m_dechiffre)
```

---

## Ressources pédagogiques

### Chiffrement RSA

1. **Maths expertes – Les nombres premiers et le chiffrement RSA**
   Une vidéo claire qui explique comment les nombres premiers sont utilisés dans le chiffrement RSA.
   [Voir la vidéo](https://www.youtube.com/watch?v=azSL_wDuZO4)

2. **Cours Pasquet – Chiffrement RSA**
   Une explication détaillée du fonctionnement du chiffrement RSA, avec des exemples concrets.
   [Voir la vidéo](https://www.youtube.com/watch?v=jZiMkAOOUKs)

3. **Maths interne – Le système RSA "pour les nuls"**
   Une introduction simplifiée au système RSA, idéale pour les débutants.
   [Voir la vidéo](https://www.youtube.com/watch?v=1LGcAIyn2Gk)

### Petit théorème de Fermat

1. **Maths Khawarizmi – Théorème de Fermat + Démonstration**
   Une démonstration détaillée du petit théorème de Fermat, avec des explications pas à pas.
   [Voir la vidéo](https://www.youtube.com/watch?v=XC-VgIeEBCU)

2. **Francis Loret – Le dernier théorème de Fermat**
   Une présentation historique et mathématique du dernier théorème de Fermat.
   [Voir la vidéo](https://www.youtube.com/watch?v=Acr1HQz2mDU)

### Théorème d’Euler

1. **Ennaji Khalid Sciences – Théorème d'Euler : cours et démonstration**
   Une explication complète du théorème d'Euler, avec des exemples d'application.
   [Voir la vidéo](https://www.youtube.com/watch?v=9k316Fi-05g)

2. **Mathématiques 1 – Théorème d'Euler**
   Une présentation académique du théorème d'Euler, adaptée aux étudiants en mathématiques.
   [Voir la vidéo](https://www.youtube.com/watch?v=9yb14S7y0Vw)

### Ressources complémentaires

- **Lumni – La cryptographie et Alan Turing**
  Une vidéo qui explore l'histoire de la cryptographie et le rôle d'Alan Turing.
  [Voir la vidéo](https://www.lumni.fr/video/la-cryptographie-et-alan-turing)

- **Arte – Voyages au pays des maths**
  Une série documentaire qui vulgarise des concepts mathématiques complexes, y compris ceux liés à la cryptographie.
  [Voir la série](https://www.arte.tv/fr/videos/RC-021426/voyages-au-pays-des-maths/)
