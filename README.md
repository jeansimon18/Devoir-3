# Devoir‑3

Résumé
------

Ce document contient l'énoncé du Problème 1 (40 points) portant sur le test de modèles linéaires d'évaluation d'actifs. La tâche consiste à évaluer dans quelle mesure des facteurs communs expliquent la coupe transversale des rendements pour des portefeuilles sectoriels, en utilisant un cadre de régression en deux étapes et des données mensuelles réelles issues de la bibliothèque de Ken French.

Table des matières
------------------

- [Enoncé du problème](#probl%C3%A8me-1-40-points--test-de-mod%C3%A8les-lin%C3%A9aires-d%C3%A9valuation-dactifs)
	- [Données à utiliser](#donn%C3%A9es-%C3%A0-utiliser)
	- [Période d'échantillonnage](#p%C3%A9riode-d%C3%A9chantillonnage)
	- [Questions (a) à (e)](#questions-a-%C3%A0-e)

## Problème 1 [40 points] — Test de modèles linéaires d’évaluation d’actifs

Dans cette question, vous testerez la performance de modèles de facteurs linéaires en utilisant des données de rendement réelles. Votre tâche est d’évaluer dans quelle mesure les facteurs communs expliquent la coupe transversale des rendements pour les portefeuilles sectoriels en utilisant un cadre de régression en deux étapes.

### Données à utiliser

- `F-F_Research_Data_5_Factors_2x3` : le modèle standard à 5 facteurs de Fama et French.
- `F-F_Momentum_Factor` : le facteur de momentum (UMD).
- `17 Industry Portfolios` : rendements excédentaires pondérés par la valeur par secteur.

Récupérez toutes les séries pour la période d’échantillonnage 1980–2021. Assurez-vous que tous les rendements sont sous forme excédentaire.

### Questions (a) à (e)

a. Récupérez et fusionnez l’ensemble de données à six facteurs et les 17 portefeuilles sectoriels du site Web de Ken French. Assurez-vous que les données sont correctement alignées et nettoyées. Rapportez des statistiques sommaires de base pour toutes les séries et fournissez des graphiques de séries chronologiques pour au moins trois secteurs et deux facteurs. Discutez brièvement de toute différence notable entre les séries. [10 points]

b. Estimez le modèle de facteurs linéaires suivant via les MCO :

Rit = αi + β⊤i ft + εit

où Rit est le rendement excédentaire sur le secteur i, et ft sont les six facteurs (incluant le momentum). Rapportez le R2 moyen, les bêtas estimés et les statistiques t robustes. Commentez les tendances ou anomalies à travers les secteurs et les facteurs. [10 points]

c. Exécutez la régression transversale de deuxième étape :

R¯i = λ⊤βi + ηi

Estimez les prix du risque λ, rapportez les statistiques t robustes, et effectuez le test J de la performance d’évaluation du modèle. Toutes les erreurs d’évaluation sont-elles expliquées ? Quels facteurs sont évalués ? [10 points]

d. Répétez la partie (c) en supposant que les facteurs ne sont pas négociés. Comparez vos résultats du test J. Quelle spécification est plus appropriée, et pourquoi ? [5 points]

e. Réfléchissez brièvement à ce que vous avez appris. Répondez à chacune des questions suivantes en 1 à 2 phrases : [5 points]

- Certains portefeuilles semblent-ils obtenir un rendement inexpliqué par les facteurs ?
- Vos conclusions dépendent-elles du fait que les facteurs soient négociés ou non

---

Remarques sur le format
----------------------

Le contenu original a été conservé intégralement; la mise en forme a été clarifiée pour faciliter la lecture et la navigation. Si vous souhaitez un style différent (par exemple, sections plus détaillées pour les résultats, exemples de code, ou une version en anglais), dites-le et je l'appliquerai.