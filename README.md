# 💕 Camino del Corazón 💕

Un jeu de plateau romantique interactif pour couples, optimisé pour mobile.

## 🎮 Comment jouer

1. Ouvrez `index.html` dans votre navigateur mobile
2. Le **Joueur 1 (Alejandra)** commence et clique sur "Tirar los dados"
3. Les pions se déplacent automatiquement selon le résultat des dés
4. Une question apparaît - le joueur répond dans le champ texte
5. L'autre joueur valide ou rejette la réponse
6. Si correct → le joueur gagne des points (1 pt normal, 2 pts Reto/Verdad)
7. Le premier à atteindre la META termine la partie

## 🎁 Fonctionnalités

- ✅ Plateau de 32 cases en spirale
- ✅ Deux pions personnalisés (SVG)
- ✅ Drag & drop des pions
- ✅ Deux dés animés
- ✅ Système de questions/réponses
- ✅ Cases spéciales Reto/Verdad
- ✅ Bonus pour les doubles (5 pts, avancer, jouer 2x, vérité absolue)
- ✅ Système de points
- ✅ Tour par tour
- ✅ Écran de fin de partie

## 📦 Structure du projet

```
camino-del-corazon/
├── index.html          # Fichier principal du jeu
├── assets/
│   ├── pion1.svg      # Pion Alejandra
│   └── pion2.svg      # Pion Jaemeson
└── README.md          # Ce fichier
```

## 🚀 Déploiement sur GitHub Pages

### Méthode 1 : Via l'interface GitHub

1. **Créez un nouveau repository sur GitHub**
   - Allez sur https://github.com/new
   - Nom du repository : `camino-del-corazon` (ou autre nom)
   - Cochez "Public"
   - Cliquez sur "Create repository"

2. **Uploadez les fichiers**
   - Cliquez sur "uploading an existing file"
   - Glissez-déposez les fichiers :
     - `index.html`
     - `README.md`
     - Le dossier `assets/` complet avec les 2 SVG
   - Commit avec le message "Initial commit"

3. **Activez GitHub Pages**
   - Allez dans Settings > Pages
   - Source : "Deploy from a branch"
   - Branch : `main` / `root`
   - Cliquez sur "Save"

4. **Accédez à votre jeu**
   - Après 1-2 minutes, votre jeu sera accessible à :
   - `https://votre-username.github.io/camino-del-corazon/`

### Méthode 2 : Via Git en ligne de commande

```bash
# Dans le dossier camino-del-corazon
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/votre-username/camino-del-corazon.git
git push -u origin main

# Activez ensuite GitHub Pages dans Settings > Pages
```

## 🔧 Personnalisation

### Modifier les questions

Éditez le tableau `PREGUNTAS` dans `index.html` (ligne ~380) :

```javascript
const PREGUNTAS = [
    { pregunta: "Votre question", type: "normal", points: 1 },
    { pregunta: "Question Reto/Verdad", type: "reto-verdad", points: 2 },
    // ...
];
```

### Modifier les noms des joueurs

Dans `index.html`, cherchez :

```javascript
players: {
    1: { name: "Alejandra", points: 0, position: 0 },
    2: { name: "Jaemeson", points: 0, position: 0 }
}
```

### Modifier les pions

Remplacez les fichiers SVG dans `assets/` par vos propres images.

## 📱 Compatibilité

- ✅ iOS (Safari)
- ✅ Android (Chrome)
- ✅ Ordinateurs de bureau
- ✅ Tablettes

## 💡 Fonctionnalités futures

Pour ajouter le mode multijoueur en temps réel :
- Intégration Firebase Realtime Database
- Système de rooms avec codes
- Synchronisation des actions en temps réel

## 📄 Licence

Libre d'utilisation pour un usage personnel.

---

Fait avec 💕 pour Alejandra & Jaemeson
