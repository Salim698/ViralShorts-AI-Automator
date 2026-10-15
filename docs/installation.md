# Guide d'Installation

## 1. La partie Make.com (Facebook)
Comme l'API Meta Developer est complexe, nous utilisons Make.com pour publier sur Facebook.
1. Créez un scénario Make et importez le fichier `make-blueprint.json`.
2. Connectez votre page Facebook au nœud **Upload a Video**.
3. Cliquez sur le nœud **Webhook**, créez un nouveau webhook et copiez l'URL générée.
4. Sauvegardez et activez le scénario.

## 2. La partie n8n (Orchestrateur)
1. Importez `n8n-workflow.json`.
2. Remplissez toutes les variables d'environnement (`.env.example`) dans les nœuds correspondants :
   - Noeud `Gemini`
   - Noeud `ElevenLabs`
   - Noeuds `CloudConvert`
   - Noeud `Pexels`
3. Dans le nœud **Envoi vers Make (Facebook)**, collez l'URL du webhook récupérée à l'étape 1.
4. Connectez votre compte Google dans le nœud **Sauvegarder sur Drive** et renseignez l'ID du dossier où stocker les vidéos.
5. Connectez votre compte YouTube.
6. Le nœud `Schedule Trigger` est configuré pour tourner toutes les 8 heures. Vous pouvez le modifier selon vos besoins.
7. Activez le workflow.
