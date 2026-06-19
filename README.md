# TrackForge

TrackForge est une application web statique pour préparer un fichier MP3 avant publication : import du morceau, ajout d'une cover, saisie des metadonnees ID3, preview type Spotify et export du MP3 tague.

L'application tourne entierement dans le navigateur. Aucun backend n'est necessaire et les fichiers audio restent locaux sur la machine de l'utilisateur.

## Fonctionnalites

- Import d'un fichier MP3 par selection ou glisser-deposer.
- Visualisation audio avec WaveSurfer.js.
- Ajout d'une cover et recadrage carre.
- Saisie des metadonnees principales : titre, artiste, album, annee, piste, genre, compositeur.
- Champs avances : commentaire, copyright, BPM, tonalite, label, ISRC.
- Preview desktop et mobile inspiree de Spotify.
- Export d'un MP3 avec tags ID3 et cover integree.

## Utilisation locale

Ouvre simplement `index.html` ou `trackforge.html` dans un navigateur moderne.

Pour servir le dossier en local :

```bash
python -m http.server 8000
```

Puis ouvre `http://localhost:8000`.

## Structure

```text
.
├── index.html       # Point d'entree pour GitHub Pages
├── trackforge.html  # Application principale
├── .gitignore
├── .gitattributes
└── .nojekyll
```

## Deploiement GitHub Pages

Une fois le projet pousse sur GitHub, active GitHub Pages depuis les parametres du depot :

1. Va dans `Settings` > `Pages`.
2. Choisis `Deploy from a branch`.
3. Selectionne la branche `main` et le dossier `/root`.
4. Enregistre.

L'application sera ensuite accessible depuis l'URL GitHub Pages du depot.

## Notes

- La dependance WaveSurfer.js est chargee depuis un CDN.
- Le projet ne necessite pas d'installation npm.
- Les fichiers audio et images importes ne sont pas envoyes vers un serveur.
