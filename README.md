# 🍸 Le Bar — Configuration de votre espace de données

Bienvenue sur **Le Bar**. L'application est déjà hébergée et prête à l'emploi — vous n'avez qu'à créer votre propre repo GitHub pour stocker vos données personnelles (ingrédients et recettes).

---

## Comment ça marche

Toutes vos données sont sauvegardées dans votre propre repo GitHub sous forme de trois fichiers JSON :

- `ingredients.json` — le catalogue des ingrédients
- `myIngredients.json` — les ingrédients que vous avez chez vous
- `recipes.json` — vos recettes

Ces fichiers sont créés automatiquement au premier lancement. Vous n'avez rien à faire manuellement.

---

## Étape 1 — Créer le repo GitHub

1. Connectez-vous sur [github.com](https://github.com) (créez un compte si vous n'en avez pas)
2. Cliquez sur **New repository** (bouton vert, ou via [github.com/new](https://github.com/new))
3. Donnez-lui le nom de votre choix, par exemple `mon-bar`
4. Laissez le repo en **Public** ou **Private** — les deux fonctionnent
5. **Ne cochez rien** dans les options d'initialisation — le repo doit rester vide
6. Cliquez **Create repository**

---

## Étape 2 — Créer un Personal Access Token

Le token est une clé qui permet à l'application d'écrire dans votre repo depuis votre navigateur. Il ne sera utilisé que pour lire et écrire vos trois fichiers JSON.

1. Allez dans les **Settings** de votre compte GitHub
   → cliquez sur votre avatar en haut à droite → **Settings**
2. Dans le menu de gauche, tout en bas → **Developer settings**
3. Cliquez **Personal access tokens → Tokens (classic)**
4. Cliquez **Generate new token → Generate new token (classic)**
5. Donnez-lui un nom (ex: `le-bar`)
6. Expiration : choisissez **No expiration** pour ne pas avoir à le renouveler
7. Sous **Select scopes**, cochez uniquement **`repo`**
8. Cliquez **Generate token** en bas de page
9. **Copiez le token immédiatement** — il ne sera affiché qu'une seule fois

> ⚠️ Ne partagez jamais votre token. Il donne un accès en écriture à votre repo.

---

## Étape 3 — Connecter l'application

Sur l'application, une fenêtre de configuration s'ouvre automatiquement au premier lancement. Renseignez :

- **Nom d'utilisateur GitHub** — votre login (ex: `johndoe`)
- **Nom du repo** — le nom choisi à l'étape 1 (ex: `mon-bar`)
- **Personal Access Token** — le token copié à l'étape 2

Cliquez **Connecter**. L'application crée les fichiers JSON dans votre repo et vous êtes prêt.

---

## Reconfigurer plus tard

Le bouton **⚙ GitHub** en haut à droite de l'application permet de modifier la configuration à tout moment — utile si vous changez de repo ou si votre token expire.

> Votre configuration (token inclus) est stockée uniquement dans le `localStorage` de votre navigateur. Elle ne quitte jamais votre appareil sauf lors des appels à l'API GitHub.
