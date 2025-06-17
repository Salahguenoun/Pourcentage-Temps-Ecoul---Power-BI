# Power BI – Pourcentage de Temps Écoulé (hors week-ends et jours fériés)

Ce projet Power BI permet de calculer dynamiquement, pour chaque période de l’année 2025 (mois, trimestre, année), le pourcentage de temps écoulé **hors week-ends et jours fériés**.

## Objectif

Créer une mesure dans Power BI qui calcule :

- Le % de jours ouvrés écoulés depuis le début d'une période (mois, trimestre, année)
- En excluant automatiquement les week-ends et jours fériés
- En considérant un jour commencé comme écoulé

## Composants

- **Tables DAX**
  - `Jours_Fériés` : jours fériés en 2025, incluant les 24 et 28 février.
  - `Périodes` : année, trimestres, mois 2025 avec début/fin de chaque période.
  - `Périodes_Filtrées` : version nettoyée de la table précédente.

- **Mesure DAX**
  - `Pourcentage_Temps_Ecoule` : mesure principale qui adapte le calcul selon le niveau de hiérarchie affiché.

## Aperçu technique

Les scripts DAX sont disponibles dans le dossier `DAX/`.

Un rapport Power BI interactif est fourni dans le dossier `PBIX/`.

Le rapport écrit expliquant toute la démarche est disponible dans `Rapport/`.

## Limitations & pistes d'amélioration

- Le projet est limité à l’année 2025.
- Jours fériés saisis manuellement.
- Pistes futures :
  - Automatisation sur plusieurs années
  - Importation dynamique des jours fériés via API ou fichier externe

## Fichiers

- `Rapport Pourcentage du temps écoulé Power BI.pdf` : description complète du raisonnement
- `Pourcentage du temps écoulé.pbix` : fichier Power BI
