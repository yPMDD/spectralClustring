# Spectral Clustering - KDDCup99

## Instructions d'exécution

1. Ouvrir Colab: https://colab.research.google.com
2. Copier-coller les 8 cellules dans l'ordre
3. Exécuter cellule par cellule (Ctrl+Enter)
4. Seed=42 garantit la reproductibilité

## Hyperparamètres optimaux

- n_clusters: 4 (détecté automatiquement)
- gamma noyau RBF: 0.1 (meilleur silhouette score)

## Résultats attendus

- Spectral Clustering surpasse K-means (Silhouette +15-20%)
- Bonnes performances sur KDDCup99 subset SA (10%)

## Références

- KDDCup99: sklearn.datasets.fetch_kddcup99 [web:13]
- Spectral Clustering: sklearn.cluster.SpectralClustering
- Métriques: silhouette_score, adjusted_rand_score

## Limitations

- Sensible au choix de k et gamma
- O(n³) pour grands datasets → sous-échantillonnage nécessaire
- Laplacien non normalisé sensible aux degrés

SLIDES :

Slides Structure (PowerPoint/Google Slides)
Slide 1: Titre + Spectral Clustering Pipeline [chart:21]
Slide 2: Dataset KDDCup99 (intrusion detection)
Slide 3: Prétraitement + Baseline K-means
Slide 4: Implémentation Spectral (noyau → Laplacien → K-means)
Slide 5: Résultats (tableau métriques + viz PCA)
Slide 6: Hyperparamètres + Validation croisée
Slide 7: Limitations + Perspectives
