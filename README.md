# CinéHits 🎬

Un jeu façon Hitster, uniquement avec des **compositions de musiques de films**, jouable sur un seul téléphone, par équipes. La musique est lue par ton compte **Spotify Premium**.

## Mise en ligne (une seule fois)

1. Dépose les 3 fichiers à la racine de ton dépôt GitHub : `index.html`, `songs.js`, `README.md`
   (bouton **Add file → Upload files**, puis **Commit changes**).
2. Dans le dépôt : **Settings → Pages → Source : Deploy from a branch → Branch : `main` / `(root)` → Save**.
3. Après une minute, ton jeu est en ligne à l'adresse :
   `https://TON-PSEUDO.github.io/NOM-DU-DEPOT/`

## Relier Spotify (une seule fois)

1. Sur [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard), ouvre ton app.
2. **Edit settings → Redirect URIs** : ajoute exactement
   `https://TON-PSEUDO.github.io/NOM-DU-DEPOT/` (avec le `/` final), puis **Save**.
   L'adresse exacte est aussi affichée dans le jeu : **⚙️ Réglages → Redirect URI**.
3. Coche bien **Web API** dans les API utilisées par l'app.
4. Le Client ID est déjà intégré au jeu. Ouvre le jeu sur ton téléphone → **Se connecter à Spotify**.

> Mode développeur Spotify : seuls toi et 5 comptes autorisés peuvent se connecter, et le propriétaire de l'app doit avoir Premium. Comme tout se joue sur ton téléphone avec ton compte, c'est suffisant.

## Jouer

1. Ouvre l'application **Spotify** sur le téléphone (lance puis mets en pause n'importe quel titre, pour qu'il soit « actif »).
2. Dans CinéHits : **Nouvelle partie → nombre d'équipes → Lancer le jeu**.
3. À chaque tour :
   - **▶ Lecture** : la musique se lance dans Spotify, le titre reste caché dans le jeu.
   - **↺ Réécouter** si besoin.
   - Touche la **case entre deux années** où le film se situe.
   - **Valider** : film, morceau, compositeur et année sont révélés.
   - **Passer à l'équipe suivante**.
4. La première équipe qui atteint l'objectif (10 cartes par défaut) gagne.

Astuce : ajoute la page à l'écran d'accueil (Safari : Partager → Sur l'écran d'accueil).
Pour éviter de voir le titre sur l'écran de Spotify, choisis une enceinte, un PC ou une TV dans **Réglages → Appareil de lecture**.

## Vérifier et corriger la liste

- **Réglages → Vérifier la liste** cherche tous les morceaux sur Spotify et affiche ceux qui ne sont pas trouvés.
- Pour forcer un morceau précis : dans Spotify, *Partager → Copier le lien du titre*. Le lien ressemble à
  `https://open.spotify.com/track/4uLU6hMCjMI75M1A2tKUQC?si=...` → l'ID est `4uLU6hMCjMI75M1A2tKUQC`.
  Ajoute-le en 6e position de la ligne dans `songs.js` :
  `["Titanic", 1997, "James Horner", "Rose", "Titanic", "4uLU6hMCjMI75M1A2tKUQC"],`
- Ajouter un morceau = ajouter une ligne dans `songs.js` (maximum 2 par film). L'année est celle de **sortie du film**.
