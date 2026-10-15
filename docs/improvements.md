# Améliorations Possibles (Roadmap)

Bien que ce workflow fonctionne extrêmement bien en production, voici des pistes d'optimisation (n'hésitez pas à ouvrir des *Issues* sur GitHub pour contribuer !) :

### 1. Externalisation du Prompt
Le prompt Gemini est actuellement codé en dur dans le nœud HTTP. Il serait judicieux de le stocker sur Notion, Airtable ou un Google Doc. Cela permettrait d'ajuster la stratégie éditoriale sans toucher au code n8n.

### 2. Gestion Globale des Erreurs
Actuellement, si ElevenLabs ou CloudConvert échoue, le workflow s'arrête silencieusement (bien que les nœuds aient un système de retry). Ajouter un nœud *Error Trigger* pour envoyer une alerte Telegram ou Slack sauverait beaucoup de temps de débogage.

### 3. Dynamisme Visuel (Pan & Scan)
Le filtre FFmpeg rogne actuellement les vidéos Pexels au format 9:16 de manière fixe. Ajouter un léger zoom dynamique lent ou un balayage dans `filter_complex` augmenterait la rétention visuelle.

### 4. Base de données Musicale
Les musiques de fond (liens Dropbox) sont codées en dur dans le nœud `Sélection Musique`. Connecter ce nœud à un Google Sheet permettrait d'ajouter de nouvelles musiques virales facilement.
