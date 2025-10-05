# Cahier de Suivi Personnel - MELONG LETHYCIA

# TPE N°1 : CALCUL SYMBOLIQUE ET SYMPY

##  Informations


- **Nom** : MELONG LETHYCIA
- **Projet** : TPE N°1 : CALCUL SYMBOLIQUE ET SYMPY
- **Encadrant** : Pr. MELATAGIA Paulin 
- **Période** : 25/09/2025 - 02/10/2025


---

##  Objectifs du Projet

Explorer et maîtriser la bibliothèque **SymPy** pour le calcul symbolique en Python, en mettant l'accent sur :

- Manipulation d'expressions mathématiques symboliques
- Calcul de dérivées et intégrales
- Résolution d'équations algébriques et différentielles
- Simplification et transformation d'expressions
- Applications pratiques en mathématiques et sciences

---

##  Travail Réalisé

### 1. Prise en Main de SymPy



- Installation et importation de la bibliothèque
- Création de symboles et variables symboliques
- Opérations arithmétiques de base sur expressions symboliques


**Concepts maîtrisés** :
```python
from sympy import symbols, simplify, expand, factor
x, y, z = symbols('x y z')
```

### 2. Calcul Différentiel



- Calcul de dérivées premières : `diff(expr, x)`
- Dérivées partielles pour fonctions multivariées
- Dérivées d'ordre supérieur
- Calcul de gradients et matrices hessiennes

**Exemples traités** :
- Dérivée de polynômes, exponentielles, logarithmes
- Gradient de fonctions à plusieurs variables


### 3. Calcul Intégral


- Intégrales indéfinies : `integrate(expr, x)`
- Intégrales définies avec bornes
- Intégrales multiples
- Calcul d'aires et volumes

### 3. Résolution d'Équations



- Équations algébriques : `solve(equation, variable)`
- Systèmes d'équations linéaires et non-linéaires
- Équations différentielles ordinaires (EDO) : `dsolve()`
- Équations polynomiales de degré supérieur

**Cas d'usage** :
- Trouver les points critiques d'une fonction
- Résoudre des systèmes d'équations en optimisation



### 4. Algèbre Linéaire Symbolique

**Fichier** : `algebre_lineaire.py`

- Matrices symboliques : `Matrix()`
- Opérations matricielles (multiplication, inversion, transposée)
- Calcul de déterminant, trace, valeurs propres
- Résolution de systèmes linéaires

**Exemple** :
```python
A = Matrix([[a, b], [c, d]])
det_A = A.det()  # ad - bc
```


---

##  Difficultés Rencontrées et Solutions


### 1. Notation et affichage
**Problème** : Difficulté à obtenir un affichage clair et lisible
**Solution** : 
- Utilisation de `pprint()` pour l'affichage console
- `latex()` pour générer du code LaTeX
- `init_printing()` pour l'affichage automatique amélioré

### 2. Hypothèses sur les variables
**Problème** : SymPy ne fait pas toujours les bonnes hypothèses (réel, positif, etc.)
**Solution** :
```python
x = symbols('x', real=True, positive=True)
```

### 3. Intégration et simplification automatique
**Problème** : Les résultats ne sont pas toujours sous la forme la plus simple
**Solution** : 
- Application successive de `simplify()`, `trigsimp()`, `expand()`
- Parfois manuel avec `collect()`, `factor()`

---

##  Compétences Développées

### Techniques
- ✅ Maîtrise complète de la bibliothèque SymPy
- ✅ Calcul différentiel et intégral symbolique
- ✅ Résolution d'équations complexes
- ✅ Algèbre linéaire symbolique
- ✅ Optimisation mathématique

### Transversales
- ✅ Pensée analytique et rigoureuse
- ✅ Documentation technique claire
- ✅ Visualisation de concepts mathématiques
- ✅ Bridge entre mathématiques et programmation



---




## 📝 Réflexions Personnelles

### Ce que j'ai appris

SymPy est un outil puissant qui transforme Python en système de calcul formel comparable à Mathematica ou Maple. La capacité de manipuler des expressions mathématiques de manière programmatique ouvre des possibilités énormes pour :

- **L'enseignement** : Vérification automatique de calculs
- **La recherche** : Dérivation de formules complexes
- **L'ingénierie** : Modélisation et simulation symbolique

### Défis intéressants

Le passage du calcul numérique au calcul symbolique demande un changement de paradigme. Il faut penser en termes de **manipulations formelles** plutôt que de **valeurs approximatives**.


---

**Dernière mise à jour** : 02/10/2025

---

<br>
<br>
<br>
<br>
<br>


# TP1: Fonctions de Perte

## Informations

- **Nom** : MELONG LETHYCIA
- **Projet** : TP N°1 : FONCTIONS DE PERTE
- **Encadrant** : Pr. MELATAGIA Paulin 
- **Rôle dans le projet** : Analyse de la fonction de perte d'entropie croisée catégorielle
- **Période** : 02/10/2025 - 02/10/2025

---



##  Objectifs Assignés

Dans le cadre de ce projet en groupe sur les fonctions de perte en apprentissage automatique, j'ai été chargée de :

- Étudier et implémenter la fonction de perte **entropie croisée catégorielle**
- Analyser ses propriétés mathématiques (gradient, convexité)
- Créer des visualisations pour illustrer son comportement
- Comparer avec d'autres fonctions de perte (notamment MSE)

---

##  Travail Réalisé

### 1. Introduction Théorique



- Définition mathématique de l'entropie croisée catégorielle
- Formule : $L = -\sum_{i=0}^{K-1} y_i \log(\hat{y}_i)$
- Interprétation intuitive de la fonction de perte
- Explication du gradient et de sa simplification avec softmax

### 2. Calcul Symbolique du Gradient



- Utilisation de SymPy pour le calcul symbolique
- Dérivation automatique de la fonction de perte
- Affichage des gradients : $\frac{\partial L}{\partial \hat{y}_i} = -\frac{y_i}{\hat{y}_i}$
- Démonstration de la simplification avec softmax : $\frac{\partial L}{\partial z_i} = \hat{y}_i - y_i$

### 3. Analyse de Convexité



- Calcul de la matrice Hessienne (dérivées secondes)
- Analyse des propriétés de convexité
- Démonstration que la fonction est strictement convexe
- Interprétation des implications pratiques pour l'optimisation

**Résultats clés** :
- Hessienne diagonale : $H_{ii} = \frac{y_i}{\hat{y}_i^2}$
- Éléments hors diagonale nuls : $H_{ij} = 0$ pour $i \neq j$
- Fonction strictement convexe (pas de minima locaux)

### 4. Visualisations


- Adaptation du code de visualisation MSE pour l'entropie croisée
- Deux figures principales :
  - **Régression** : Courbe prédite et scatter plot avec binary cross-entropy
  - **Classification** : Frontière de décision et courbe de perte
- Comparaison visuelle avec MSE

### 5. Analyse Symbolique Complète



- Équation de régression logistique avec coefficients réels
- Gradient symbolique complet
- Calcul de l'équation de la tangente en un point spécifique
- Forme développée des équations

---

## 🔍 Difficultés Rencontrées

1. **Normalisation pour la régression** : L'entropie croisée est naturellement conçue pour des probabilités. Pour l'appliquer à la régression, j'ai dû normaliser les valeurs entre 0 et 1.

2. **Gestion du log(0)** : Ajout d'un epsilon (1e-15) pour éviter les valeurs infinies lors du calcul de $-\log(0)$.

3. **Notation mathématique** : Harmonisation de la notation ($\hat{y}_i$ vs $p_i$) dans tous les documents.

---

##  Compétences Développées

- Maîtrise du calcul symbolique avec SymPy
- Analyse mathématique avancée (gradient, Hessienne)
- Visualisation de données avec Matplotlib
- Compréhension approfondie des fonctions de perte en ML
- Documentation technique avec Markdown et LaTeX

---




## Liens avec le Projet Global

Mon travail sur l'entropie croisée catégorielle s'intègre dans le projet global qui compare différentes fonctions de perte :

- **MSE** : Travaillé par DASSI MANDJO LEA JUSTINE  
- **Entropie Croisée Catégorielle** : Ma contribution
- **Entropie Croisée binaire** : Travaillé par BELL ARSENE
- **perte de Huber** : Travaillé par DASSI MANDJO LEA JUSTINE  

---





##  Notes Personnelles

- L'entropie croisée catégorielle est particulièrement élégante en classification multi-classes
- La propriété de convexité garantit une optimisation stable
- La simplification du gradient avec softmax ($\hat{y}_i - y_i$) est remarquablement simple
- Cette fonction de perte est un choix standard pour la classification, ce qui justifie son étude approfondie

---



**Dernière mise à jour** : 05/10/2025