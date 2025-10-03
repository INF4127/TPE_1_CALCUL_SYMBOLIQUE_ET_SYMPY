# TPE_1_CALCUL_SYMBOLIQUE_ET_SYMPY
Ce projet vise à introduire le **calcul symbolique** et son implémentation avec la bibliothèque **Sympy** en Python.  
Il combine à la fois une présentation théorique, des fichiers de suivi et des applications pratiques en optimisation et en apprentissage automatique

## Description du projet

Ce projet comporte : 

- Une **présentation théorique** du calcul symbolique et de sympy : principes, avantages, limites.

- Un **notebook Jupyter** démontrant des cas pratiques avec Sympy.

- Des **fichiers README de suivi** représentant le travail réalisé par chaque membre dans le dossier doc.

- Une **application pratique (notebook Jupyter)** portant sur l’étude de la convexité des fonctions de perte utilisées en machine learning.

- Des **datasets** pour l'expérimentation sur des données réelles des fonctions de perte.


## Objectifs

1. **Compréhension du calcul symbolique** 
- Présenter le calcul symbolique, ressortir ses applications, avantages et limites.
- Comprendre les principes du calcul symbolique (dérivées, intégrales, simplifications, équations, etc.).
- Explorer l’utilisation de Sympy pour automatiser ces opérations.
- Illustrer l’application du calcul symbolique en optimisation mathématique.

2. **Applications pratiques en optimisation et en machine learning**  
   Pour chacune des fonctions de perte suivantes :  
   - Erreur Quadratique Moyenne (MSE)  
   - Entropie Croisée Binaire  
   - Entropie Croisée Catégorielle  
   - Perte de Huber  

   Nous avons utilisé Sympy pour :  
   - Fournir les expressions symboliques des **gradients**.  
   - Étudier leurs **propriétés de convexité**.  

3. **Expérimentation sur données réelles**  
   - Sélection ou Génération de deux jeux de données simples :  
     - Un jeu pour la **régression** (2 attributs explicatifs, < 100 observations).  
     - Un jeu pour la **classification** (2 attributs explicatifs, < 100 observations).  
   - Visualisation des courbes associées à ces fonctions de perte.  
   - Détermination de l’équation de la **tangente à l’ellipse** en un point donné, en utilisant le calcul symbolique.

## Résultats attendus

- Expressions analytiques et symboliques des gradients des fonctions de perte.  

- Étude formelle de la convexité.  

- Visualisation graphique des pertes sur des petits jeux de données.  

- Détermination symbolique de la tangente à l’ellipse en un point donné.

## Structure du projet

TPE_1_CALCUL_SYMBOLIQUE_ET_SYMPY/
  
  │── sympy___calcul_symbolique.pdf          
  │── sympy.ipynb
  │── fonction_perte.ipynb
  │── dataset_classification.csv
  │── dataset_regression.csv                            
  │── README.md    
  │── doc/
  
  │── 22W2147LETHYCIA-MELONG.md           
  │── 22W2164LEA-DASSI.md                     
  │── 22T2960ARSENE-BELL.md          

## Technologies utilisées

+ Python 3.10+

+ Jupyter Notebook (Ou google colab)

+ Sympy

+ **Matplotlib / Seaborn** : visualisation des courbes.


## Installation

### 1 - Cloner le dépôt :

git clone https://github.com/INF4127/TPE_1_CALCUL_SYMBOLIQUE_ET_SYMPY.git

cd TPE_1_CALCUL_SYMBOLIQUE_ET_SYMPY


### 2 - Installer les dépendances :

pip install sympy jupyter

## Utilisation

Lancer Jupyter Notebook : jupyter-notebook

Ouvrir le fichier **sympy.ipynb**.

Exécuter les cellules pour explorer les exemples :

- Simplifications d’expressions

- Résolution d’équations

- Dérivées et intégrales

- Matrice Hessienne et optimisation

Ouvrir le fichier **fonction_perte.ipynb**.

- Exécuter les cellules pour explorer les exemples liés aux fonctions de perte :

- Calcul symbolique des gradients pour différentes fonctions de perte (MSE, entropie croisée binaire et catégorielle, perte de Huber).

- Vérification des propriétés de convexité via les dérivées secondes (La Hessienne).

- Représentation graphique des fonctions sur des jeux de données simples (régression et classification).

- Détermination de l’équation de la tangente à une ellipse en un point donné.

## Contenu pédagogique

Partie 1 : Introduction au calcul symbolique

- Définition et historique

- Intérêt en optimisation et en apprentissage automatique

Partie 2 : Découverte de Sympy et ses modules utiles

- Manipulation symbolique (simplifications, dérivées, intégrales)

- Fonctions mathématiques avancées (gradients, Hessien, convexité)

Partie 3 : Fonctions de perte en apprentissage supervisé

- Erreur quadratique moyenne (MSE)

- Entropie croisée binaire

- Entropie croisée catégorielle

Perte de Huber

- Partie 4 : Études expérimentales

- Calcul des gradients symboliques

- Vérification de la convexité des fonctions

- Visualisation des courbes de perte avec des jeux de données réduits

- Exemple de tangente à une ellipse

## Auteurs

Projet réalisé dans le cadre du TPE N°1 par :

- BELL ARSENE KEVIN

- DASSI MANDJO LEA JUSTINE

- MELONG LETHYCIA
