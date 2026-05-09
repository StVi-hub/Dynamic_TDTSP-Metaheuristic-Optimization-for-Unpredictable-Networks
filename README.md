[![English](https://img.shields.io/badge/lang-en-red)](#english)
[![Français](https://img.shields.io/badge/lang-fr-blue)](#-français)

<a name="english"></a>

# Dynamic-TDTSP: Metaheuristic Optimization for Unpredictable Networks
## Project Overview

This project addresses a specialized variant of the Traveling Salesman Problem: the Time-Dependent Traveling Salesman Problem (TDTSP) with Dynamic Road Blockages. In real-world logistics, travel costs are rarely constant; they fluctuate based on traffic patterns and unexpected infrastructure failures.

This repository provides a complete framework for modeling these complexities and solving them using advanced metaheuristic algorithms, specifically designed for resilient supply chain management and autonomous routing.

## Key Features

- Time-Dependent Cost Matrices: Travel costs evolve dynamically as the agent moves through the network.
- Stochastic Road Blockages: Simulates real-world disruptions (accidents, construction) via dynamic edge unavailability.
- Mathematical Rigor: Full formalization of the objective function and constraints using Linear Programming (LP) standards.
- Hybrid Metaheuristics: Implementation and comparison of Genetic Algorithms (GA) and Ant Colony Optimization (ACO).
- Complexity Analysis: Formal proof of the problem's membership in the NP-Hard class.

## Mathematical Formulation

The problem is modeled as a graph $G = (V, A)$ where the cost function $c_{i,j}(t)$ depends on the departure time $t$ from node $i$.

## Objective Function

Minimize the total arrival time at the final destination:

$$\min Z = \sum_{(i,j) \in A} \sum_{t \in T} c_{i,j}(t) \cdot x_{i,j,t}$$

## Implementation & Algorithms

The project utilizes Python and the PuLP library for exact modeling, alongside custom implementations of:

Genetic Algorithm (GA):

- Custom crossover operators for permutation preservation.
- Adaptive mutation rates to avoid local optima.

Ant Colony Optimization (ACO):

- Pheromone update rules modified for time-dependent costs.
- State-dependent heuristic desirability.

## Performance Evaluation

- OFAT (One-Factor-At-a-Time) Analysis: Systematic hyperparameter tuning.
- Lower Bound Calculation: Comparison against theoretical minima to assess the optimality gap.

## Tech Stack

- Language: Python 3.11.9
- Modeling: PuLP (Linear Programming)
- Analysis: NumPy, Matplotlib, Pandas



<details>
<summary><b>Cliquez ici pour lire en Français</b></summary>

[![Français](https://img.shields.io/badge/lang-fr-blue)](#-français)
[![English](https://img.shields.io/badge/lang-en-red)](#english)


# Dynamic-TDTSP : Optimisation Métaheuristique pour Réseaux Imprévisibles

## Aperçu du Projet

Ce projet traite d'une variante spécialisée du Problème du Voyageur de Commerce : le Time-Dependent Traveling Salesman Problem (TDTSP) avec blocages de routes dynamiques. Dans la logistique réelle, les coûts de transport sont rarement constants ; ils fluctuent en fonction du trafic et des défaillances imprévues des infrastructures.

Ce dépôt fournit un cadre complet pour modéliser ces complexités et les résoudre à l'aide d'algorithmes métaheuristiques avancés, conçus pour la gestion résiliente de la chaîne d'approvisionnement et le routage autonome.

## Caractéristiques Clés

Matrices de Coût Dépendantes du Temps : Les coûts de trajet évoluent dynamiquement selon l'heure de départ.

Blocages de Routes Stochastiques : Simulation de perturbations réelles (accidents, travaux) via l'indisponibilité dynamique des arcs.

Rigueur Mathématique : Formalisation complète de la fonction objectif et des contraintes selon les standards de la Programmation Linéaire (PL).

Métaheuristiques Hybrides : Implémentation et comparaison d'Algorithmes Génétiques (AG) et d'Optimisation par Colonies de Fourmis (ACO).

Analyse de Complexité : Preuve formelle de l'appartenance du problème à la classe NP-Difficile.

## Formulation Mathématique

Le problème est modélisé comme un graphe $G = (V, A)$ où la fonction de coût $c_{i,j}(t)$ dépend de l'heure de départ $t$ du sommet $i$.

## Fonction Objectif

Minimiser l'heure d'arrivée totale à la destination finale :

$$\min Z = \sum_{(i,j) \in A} \sum_{t \in T} c_{i,j}(t) \cdot x_{i,j,t}$$

## Implémentation & Algorithmes

Le projet utilise Python et la bibliothèque PuLP pour la modélisation exacte, ainsi que des implémentations personnalisées de :

Algorithme Génétique (AG) :

Opérateurs de croisement spécifiques pour la préservation des permutations.

Taux de mutation adaptatifs pour éviter les optima locaux.

Optimisation par Colonies de Fourmis (ACO) :

Règles de mise à jour des phéromones modifiées pour les coûts dépendant du temps.

Désirabilité heuristique dépendant de l'état du réseau.

## Évaluation des Performances

Analyse OFAT (One-Factor-At-a-Time) : Réglage systématique des hyperparamètres.

Calcul de Borne Inférieure : Comparaison avec les minima théoriques pour évaluer l'écart d'optimalité.

## Stack Technique

Langage : Python 3.11.9

Modélisation : PuLP (Programmation Linéaire)

Analyse : NumPy, Matplotlib, Pandas

</details>