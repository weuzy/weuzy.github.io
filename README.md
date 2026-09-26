# Portfolio — Ousseynou Diop

## Structure
```
portfolio_ousseynou/
└── index.html   ← tout est dans ce fichier (photo + CV PDF embarqués)
```

## Mettre à jour le contenu
Ouvre `index.html` dans un éditeur (VS Code recommandé).

### Modifier les textes / expériences
Recherche (Ctrl+F) le texte à modifier et remplace directement.

### Changer la photo de profil
1. Encode ta nouvelle photo en base64 :
   ```bash
   python3 -c "import base64; print('data:image/jpeg;base64,' + base64.b64encode(open('photo.jpg','rb').read()).decode())" > photo_b64.txt
   ```
2. Dans `index.html`, remplace la valeur `src="data:image/jpeg;base64,..."` de la balise `<img>` dans `.hero-photo-wrap`

### Changer le CV PDF
1. Encode ton nouveau PDF :
   ```bash
   python3 -c "import base64; print(base64.b64encode(open('cv.pdf','rb').read()).decode())" > cv_b64.txt
   ```
2. Dans `index.html`, recherche `data:application/pdf;base64,` et remplace la valeur

## Mettre en ligne

### Option 1 — GitHub Pages (gratuit, recommandé)
```bash
# 1. Crée un repo GitHub nommé : weuzy.github.io
# 2. Clone-le localement
git clone https://github.com/weuzy/weuzy.github.io
cd weuzy.github.io

# 3. Copie le fichier
cp /chemin/vers/index.html .

# 4. Push
git add . && git commit -m "Portfolio update" && git push

# → Accessible sur : https://weuzy.github.io
```

### Option 2 — Netlify Drop (le plus rapide, 30 secondes)
1. Va sur https://app.netlify.com/drop
2. Glisse-dépose le fichier `index.html`
3. Ton portfolio est en ligne instantanément avec une URL Netlify
4. Tu peux connecter un domaine personnalisé ensuite

### Option 3 — Vercel
```bash
npm i -g vercel
cd portfolio_ousseynou
vercel
```

### Option 4 — Domaine personnalisé
Achète un domaine (ex: ousseynou.dev sur Namecheap ~$10/an)
et pointe-le vers GitHub Pages ou Netlify.

## Couleurs (pour changer le thème)
En haut de `index.html` dans `:root { ... }` :
- `--accent: #C8963E`     ← or brûlé (couleur principale)
- `--accent2: #4F8EF7`    ← bleu électrique
- `--bg-deep: #050714`    ← fond cosmos
# weuzy.github.io
