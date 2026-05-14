# Antoine's Playables — Setup GitHub Pages

Ce dossier contient tout ce qu'il faut pour héberger ta galerie de playables sur ton propre GitHub Pages, façon Augusto.

## Structure

```
local-deploy/
├── index.html              # La landing page "Netflix" (gallery)
├── games/
│   └── farm-sort/
│       └── index.html      # Le playable Farm Sort (~4.4 MB)
└── README.md               # Ce fichier
```

## Étapes pour déployer (~10 minutes)

### 1. Crée le repo GitHub

1. Ouvre **GitHub Desktop** (déjà installé sur ton poste) — sinon va sur https://github.com/new
2. Crée un nouveau repo : nom au choix, par ex. **`antoine-playables`** ou **`playables`**
3. **Public** (obligatoire pour GitHub Pages gratuit)
4. Pas de README/license au création (on en a déjà)

### 2. Copie le contenu de `local-deploy/` dans le repo

Drag-and-drop dans GitHub Desktop ou directement dans le dossier local du repo cloné :
- `index.html`
- `games/` (dossier complet)
- `README.md`

### 3. Commit + Push

Via GitHub Desktop : "Commit to main" → "Push origin"

### 4. Active GitHub Pages

1. Sur GitHub.com, va dans **Settings** du repo
2. Onglet **Pages** (menu gauche)
3. Source : **Deploy from a branch**
4. Branch : **main** / dossier **/(root)**
5. Save

### 5. Ton URL

Quelques minutes après, ton site est live à :
**`https://<ton-github-username>.github.io/<nom-du-repo>/`**

Par exemple si tu te nommes `losty-wls` et le repo est `antoine-playables` :
→ `https://losty-wls.github.io/antoine-playables/`

Tu peux scanner le QR code de cette URL sur ton téléphone pour tester direct.

---

## Ajouter un nouveau playable

Quand tu construis un autre playable (via `/playable-blitz`) :

1. Copie le `playables/<nom>/dist/playable.html` vers `games/<nom>/index.html` dans le repo
2. Édite `index.html` du repo : duplique la balise `<a class="card">` du Farm Sort, change href + titre + emoji + couleurs
3. Commit + push → quelques minutes après, le nouveau jeu apparaît dans la galerie

---

## Customisation (optionnel)

Dans `index.html` :
- Change le titre `Antoine's Playables` ligne 90
- Change le gradient des couleurs dans `.brand` (lignes 18-22)
- Change `--c1` / `--c2` sur chaque card pour adapter la couleur de fond
- Remplace les emojis par tes propres thumbnails PNG (mets-les dans `assets/` et utilise `<img>` dans `.card-thumb`)
