# Projet-labyrinth

> Un jeu de labyrinthe interactif généré procéduralement avec l'algorithme DFS, développé en HTML/CSS/JavaScript pur.

---

## 📌 Description

**Maze Ultimate Pro** est une application web de jeu de labyrinthe où chaque partie génère un labyrinthe unique et aléatoire. Le joueur doit trouver le chemin de la case de départ (en haut à gauche) jusqu'à la sortie (en bas à droite) le plus rapidement possible. Un chronomètre mesure le temps de chaque partie et le meilleur score est sauvegardé localement.

---

## 🛠️ Technologies utilisées

| Technologie | Utilisation |
|-------------|-------------|
| **HTML5** | Structure de la page |
| **CSS3** | Mise en page, gradient, animations visuelles |
| **JavaScript (Vanilla)** | Logique du jeu, génération du labyrinthe, événements clavier |
| **Canvas API** | Rendu graphique du labyrinthe et du joueur |
| **LocalStorage** | Sauvegarde du meilleur score entre les sessions |

---

## ✨ Fonctionnalités principales

- 🔀 **Génération aléatoire** — chaque partie produit un labyrinthe différent grâce à l'algorithme DFS
- 🎮 **Contrôles clavier** — navigation avec les touches ↑ ↓ ← →
- ⏱️ **Chronomètre** — mesure le temps écoulé depuis le début de la partie
- 🏆 **Meilleur score** — sauvegarde automatique du record en secondes via localStorage
- 🔄 **Restart** — génère un nouveau labyrinthe à tout moment
- 🎨 **Interface soignée** — fond dégradé, canvas arrondi, ombres et boutons stylisés

---

## 🌐 Lien GitHub Pages

👉 [Voir le rendu final en ligne](https://aminrafrafi27-a11y.github.io/Rafrafi_Mohamed_Amine_Labyrinth/)

---

## 🚀 Nouveautés explorées

Durant ce projet, nous avons découvert et appris plusieurs concepts nouveaux :

- **L'algorithme DFS (Depth-First Search)** appliqué à la génération procédurale de labyrinthes — une utilisation concrète d'un algorithme de graphe vu en cours
- **L'API Canvas HTML5** pour dessiner des formes, des lignes et des arcs directement dans le navigateur sans bibliothèque externe
- **La gestion des murs par tableau de booléens** `[top, right, bottom, left]` pour représenter chaque cellule du labyrinthe
- **Le LocalStorage** pour persister des données entre les sessions sans base de données ni serveur
- **La logique de déplacement contraint** — vérifier les murs avant d'autoriser un mouvement du joueur

---

## ⚠️ Difficultés rencontrées

| # | Difficulté |
|---|------------|
| 1 | Comprendre le fonctionnement du backtracking dans l'algorithme DFS |
| 2 | Synchroniser correctement la suppression des murs entre deux cellules adjacentes (côtés miroirs) |
| 3 | Faire correspondre les coordonnées Canvas (pixels) avec les coordonnées de la grille (colonnes/lignes) |
| 4 | Empêcher le joueur de traverser les murs — gérer les 4 directions indépendamment |
| 5 | Le chronomètre continuait après la victoire si on ne gérait pas `clearInterval` correctement |

---

## ✅ Solutions apportées

| # | Solution |
|---|----------|
| 1 | Lecture de documentation sur les algorithmes de génération de labyrinthes + schémas sur papier pour visualiser le backtracking |
| 2 | Utilisation d'un système de coordonnées `dx/dy` pour détecter la direction entre deux cellules et supprimer les deux murs correspondants simultanément |
| 3 | Multiplication des indices de grille par `cellSize` pour obtenir les coordonnées pixel exactes |
| 4 | Vérification du tableau `walls[]` de la cellule courante avant chaque déplacement selon la direction demandée |
| 5 | Appel de `clearInterval(timer)` dès la détection de la condition de victoire, avant d'afficher le message |

---

## 👤 Auteur

- **Mohamed Amine Rafrafi**
- Projet réalisé dans le cadre d'un cours de développement web
