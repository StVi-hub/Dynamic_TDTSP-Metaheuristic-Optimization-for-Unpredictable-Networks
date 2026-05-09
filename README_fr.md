Dynamic-TDTSP : Optimisation Métaheuristique pour Réseaux Imprévisibles

Aperçu du Projet

Ce projet traite d'une variante spécialisée du Problème du Voyageur de Commerce : le Time-Dependent Traveling Salesman Problem (TDTSP) avec blocages de routes dynamiques. Dans la logistique réelle, les coûts de transport sont rarement constants ; ils fluctuent en fonction du trafic et des défaillances imprévues des infrastructures.

Ce dépôt fournit un cadre complet pour modéliser ces complexités et les résoudre à l'aide d'algorithmes métaheuristiques avancés, conçus pour la gestion résiliente de la chaîne d'approvisionnement et le routage autonome.

Caractéristiques Clés

Matrices de Coût Dépendantes du Temps : Les coûts de trajet évoluent dynamiquement selon l'heure de départ.

Blocages de Routes Stochastiques : Simulation de perturbations réelles (accidents, travaux) via l'indisponibilité dynamique des arcs.

Rigueur Mathématique : Formalisation complète de la fonction objectif et des contraintes selon les standards de la Programmation Linéaire (PL).

Métaheuristiques Hybrides : Implémentation et comparaison d'Algorithmes Génétiques (AG) et d'Optimisation par Colonies de Fourmis (ACO).

Analyse de Complexité : Preuve formelle de l'appartenance du problème à la classe NP-Difficile.

Formulation Mathématique

Le problème est modélisé comme un graphe $G = (V, A)$ où la fonction de coût $c_{i,j}(t)$ dépend de l'heure de départ $t$ du sommet $i$.

Fonction Objectif

Minimiser l'heure d'arrivée totale à la destination finale :


$$\min Z = \sum_{(i,j) \in A} \sum_{t \in T} c_{i,j}(t) \cdot x_{i,j,t}$$

Implémentation & Algorithmes

Le projet utilise Python et la bibliothèque PuLP pour la modélisation exacte, ainsi que des implémentations personnalisées de :

Algorithme Génétique (AG) :

Opérateurs de croisement spécifiques pour la préservation des permutations.

Taux de mutation adaptatifs pour éviter les optima locaux.

Optimisation par Colonies de Fourmis (ACO) :

Règles de mise à jour des phéromones modifiées pour les coûts dépendant du temps.

Désirabilité heuristique dépendant de l'état du réseau.

Évaluation des Performances

Analyse OFAT (One-Factor-At-a-Time) : Réglage systématique des hyperparamètres.

Calcul de Borne Inférieure : Comparaison avec les minima théoriques pour évaluer l'écart d'optimalité.

Stack Technique

Langage : Python 3.11.9

Modélisation : PuLP (Programmation Linéaire)

Analyse : NumPy, Matplotlib, Pandas