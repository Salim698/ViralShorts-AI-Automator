# Contribuer au projet ViralShorts AI

Toute aide pour améliorer les prompts de l'IA, optimiser les filtres FFmpeg ou ajouter de nouvelles plateformes de publication (TikTok, Instagram) est la bienvenue !

## Processus
1. Fais un fork du dépôt.
2. Crée une branche pour ta fonctionnalité (`git checkout -b feature/ajout-tiktok`).
3. Soumets une Pull Request (PR) détaillée.

## ✅ Checklist d'export de workflow (Make & n8n)
Avant de commiter des fichiers `.json` de workflows :
- [ ] **n8n** : Supprime les blocs `credentials` et vide l'objet `meta`.
- [ ] **n8n** : Remplace l'ID des dossiers Drive par des placeholders.
- [ ] **Make** : Vérifie qu'aucun identifiant de page Facebook personnel, nom de compte ou URN n'est en clair dans le blueprint. Remplace-les par `YOUR_PAGE_ID`.
- [ ] **Général** : Aucune clé API en clair. Utilise des variables d'environnement.
