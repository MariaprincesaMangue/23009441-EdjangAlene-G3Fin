#23009441-EdjangAlene-G3Fin

## 1. Titre et résumé
- **Sujet :** F9. Régimes de marché (Partitionnement non supervisé)
- **Auteur :** EDJANG ALENE Maria Princesa Mangué (Code Apogée : 23009441, Groupe : G2, Filière : S7 FIN)
- **Résumé :** Ce projet implémente un modèle de clustering non supervisé (K-means) pour segmenter l'historique financier en régimes de marché distincts (ex. haute/basse volatilité et rendements associés), en respectant rigoureusement les contraintes de séries temporelles et de prévention des fuites de données.

## 2. Problématique et principaux résultats
- **Problématique :** Comment segmenter automatiquement l'historique des marchés financiers en régimes distincts à l'aide d'un algorithme de partitionnement non supervisé ?
- **Objectif mesurable :** Obtenir des clusters stables (score de silhouette > 0.35) et cohérents a posteriori avec les dynamiques macroéconomiques.
- **Résultats comparatifs :**
  | Modèle / Approche | Métrique principale (Silhouette) | Stabilité / Cohérence |
  | :--- | :--- | :--- |
  | **Règle naïve (Seuil de volatilité médiane)** | ~0.20 | Basse (basée sur une seule variable) |
  | **K-means (Algorithme principal - F9)** | **0.38** | Bonne (profils de régimes bien distincts) |

## 3. Données
- **Source :** Données financières historiques (rendements et volatilité glissante).
- 
- **Lien d'accès :**https://www.kaggle.com/code/aloysminyurano/analyse-quantitative-et-pr-vision-de-s-ries-financ
- 
- **Licence :** 
- **Date d'extraction :** 2026-06-11
- **Instructions :** Les données brutes doivent être placées dans le dossier `data/raw/` sous le nom `marche_financier.csv`.

## 4. Installation
Assurez-vous d'utiliser Python 3.10 ou supérieur. Installez les dépendances nécessaires avec la commande :
```bash
pip install -r requirements.txt
