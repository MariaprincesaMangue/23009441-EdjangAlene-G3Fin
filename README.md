# Projet F25 : Taux directeur et pente de la courbe

- **Auteur :** Edjang Alene — **Code Apogée :** `23009441` — **Groupe :** `G3Fin` — **Filière :** S7 FIN
- **Résumé :** Étude empirique de la relation entre le taux directeur de Bank Al-Maghrib et la pente de la courbe des taux des Bons du Trésor marocains (10 ans − 2 ans) sur la période 2018–2026 par régression linéaire.

---

## Problématique et principaux résultats

- **Problématique :** Dans quelle mesure le niveau du taux directeur de Bank Al-Maghrib permet-il d'expliquer et de prévoir la pente de la courbe des taux souverains marocains (écart $\text{Taux}_{10\text{ ans}} - \text{Taux}_{2\text{ ans}}$) ?
- **Objectif mesurable :** Prévoir la pente mensuelle sur les 14 derniers mois (août 2024 à mars 2026) avec une erreur absolue moyenne (MAE) inférieure d'au moins 10 % à celle d'une référence naïve (moyenne historique de l'apprentissage).

| Modèle | MAE Train (pts) | MAE CV (5 plis) | MAE Test (pts) | RMSE Test (pts) | $R^2$ Test |
| :--- | :---: | :---: | :---: | :---: | :---: |
| Référence naïve (moyenne train) | 0,0923 | 0,1112 ± 0,0800 | **0,1002** | 0,1253 | -1,1226 |
| Régression linéaire (algorithme n° 1) | 0,0903 | 0,1150 ± 0,0814 | **0,1051** | 0,1302 | -1,2922 |
| Ridge réglé ($\alpha=100$, algorithme n° 2) | 0,0922 | 0,1113 | **0,1009** | 0,1259 | -1,1443 |

**Conclusion principale :** L'objectif d'une réduction de 10 % de la MAE par rapport à la référence naïve n'est pas atteint. L'équation estimée ($\widehat{\text{Pente}} = 0,5418 + 0,0380 \times \text{Taux\_directeur}$, $p = 0,225$) montre une relation positive faible et statistiquement non significative : le niveau seul du taux directeur ne suffit pas à prévoir l'aplatissement récent de la courbe des taux.

---

## Données

- **Sources officielles (extraites le 26/11/2026) :**
  1. *Historique des décisions de politique monétaire (Taux directeur)* — Bank Al-Maghrib : `https://www.bkam.ma/Politique-monetaire/Cadre-strategique/Decision-de-la-politique-monetaire/Historique-des-decisions`
  2. *Taux moyens pondérés mensuels des émissions du Trésor (TMP)* — Bank Al-Maghrib : `https://www.bkam.ma/Marches/Principaux-indicateurs/Marche-obligataire/Marche-des-bons-de-tresor/Marche-des-adjudications-des-bons-de-tresor/Taux-moyens-ponderes-mensuels-des-emissions-du-tresor`
- **Licence :** Données publiques officielles diffusées librement par Bank Al-Maghrib ; utilisation académique autorisée.
- **Échantillon :** 66 observations mensuelles complètes (février 2018 à mars 2026), découpées chronologiquement en 80 % apprentissage (52 mois) et 20 % test (14 mois).

---

## Installation et exécution

1. Cloner le dépôt :
   ```bash
   git clone [https://github.com/MariaprincesaMangue/23009441-EdjangAlene-G3Fin.git](https://github.com/MariaprincesaMangue/23009441-EdjangAlene-G3Fin.git)
   cd 23009441-EdjangAlene-G3Fin
