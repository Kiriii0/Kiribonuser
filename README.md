# Kiri Bonus — Landing Page

Site statique (HTML/CSS/JS pur, aucun build nécessaire) prêt à déployer sur Vercel.

## Contenu du projet
- `index.html` — la page complète
- `vercel.json` — configuration Vercel (URLs propres)
- `package.json` — identifie le projet (aucune dépendance)
- `.gitignore` — fichiers à ignorer par Git

## Déployer sur Vercel — 3 méthodes

### Méthode 1 — Sans ligne de commande (la plus simple)
1. Va sur https://vercel.com et connecte-toi (ou crée un compte, gratuit).
2. Clique sur **"Add New..." → "Project"**.
3. Choisis **"Deploy without Git"** / glisse-dépose le dossier `kiri-bonus` complet (ou son .zip dézippé) dans la zone d'upload.
4. Vercel détecte automatiquement un site statique — laisse les réglages par défaut.
5. Clique sur **Deploy**. Ton site sera en ligne en moins d'une minute, avec une URL du type `kiri-bonus.vercel.app`.

### Méthode 2 — Avec GitHub (recommandé si tu veux mettre à jour le site facilement)
1. Crée un dépôt sur https://github.com (ex: `kiri-bonus`).
2. Mets tous les fichiers de ce projet dedans et push :
   ```bash
   cd kiri-bonus
   git init
   git add .
   git commit -m "Site Kiri Bonus"
   git branch -M main
   git remote add origin https://github.com/TON-USER/kiri-bonus.git
   git push -u origin main
   ```
3. Sur https://vercel.com, clique **"Add New..." → "Project"**, puis **"Import Git Repository"** et sélectionne ton dépôt.
4. Laisse les réglages par défaut (aucun build command nécessaire) et clique **Deploy**.
5. À chaque `git push`, Vercel redéploie automatiquement.

### Méthode 3 — Avec la CLI Vercel
1. Installe la CLI (nécessite Node.js) :
   ```bash
   npm install -g vercel
   ```
2. Dans le dossier du projet :
   ```bash
   cd kiri-bonus
   vercel
   ```
3. Suis les instructions à l'écran (connexion, nom du projet, réglages par défaut).
4. Pour mettre en production :
   ```bash
   vercel --prod
   ```

## Nom de domaine personnalisé
Une fois déployé, dans le dashboard Vercel du projet → **Settings → Domains**, tu peux ajouter ton propre nom de domaine (ex: `kiribonus.com`) et suivre les instructions DNS affichées.

## Modifier le contenu
Tout le site (textes, liens, couleurs) est dans `index.html`. Pas de build : modifie le fichier, puis redéploie (nouveau push Git, ou nouveau `vercel --prod`, ou nouveau glisser-déposer).
