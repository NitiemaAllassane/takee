# 🎌 Manga Dashboard

Un dashboard moderne et élégant pour explorer et gérer votre collection de manga/NFT, développé avec SvelteKit et TailwindCSS.

## 📸 Aperçu

![Dashboard Overview](/static/images/screenshot.png)

## 🌐 Demo Live

🔗 **[Voir la démo](https://takee.vercel.app/)**


## 🛠 Technologies utilisées

- **[SvelteKit](https://kit.svelte.dev/)** - Framework full-stack moderne
- **[TailwindCSS](https://tailwindcss.com/)** - Framework CSS utility-first
- **[Lucide Svelte](https://lucide.dev/)** - Icônes SVG
- **TypeScript** - Typage statique
- **Vite** - Build tool ultra-rapide

## 🚀 Installation

```bash
# Cloner le projet
git clone [url-du-repo]
cd manga-dashboard

# Installer les dépendances
npm install

# Lancer le serveur de développement
npm run dev
```

Ouvrir [http://localhost:5173](http://localhost:5173) dans votre navigateur.

## 📁 Structure du projet

```
src/
├── lib/
│   ├── components/
│   │   ├── Sidebar.svelte      # Navigation principale
│   │   ├── Header.svelte       # En-tête avec recherche
│   │   ├── Badge.svelte        # Composant badge réutilisable
│   │   └── Logo.svelte         # Logo de l'application
│   └── ...
├── routes/
│   ├── +layout.svelte          # Layout principal avec grid
│   ├── +page.svelte            # Page d'accueil
│   └── ...
└── app.css                     # Styles globaux

static/
└── images/                     # Assets statiques
    ├── obito.svg
    ├── anounce.svg
    └── ...
```

## 🎨 Design System

### Couleurs personnalisées
```css
/* Configuration TailwindCSS */
bg-primary    /* Couleur de fond principale */
bg-second     /* Couleur de fond secondaire */
bg-red        /* Couleur d'accent rouge */
```

### Composants principaux
- **Sidebar** : Navigation avec profil utilisateur
- **Cards Manga** : Grille de découverte avec hover effects
- **Wallet Widget** : Suivi des crypto-monnaies
- **Top Sellers** : Classement des vendeurs

## 🔧 Scripts disponibles

```bash
# Développement
npm run dev

# Build de production
npm run build

# Prévisualisation du build
npm run preview

# Linting
npm run lint

# Formatage du code
npm run format
```

## 📱 Responsive Design

- **Desktop** : Layout en grid 2 colonnes (sidebar + contenu)
- **Mobile** : Stack vertical avec sidebar collapsible (à venir)
- **Breakpoints** : Utilisation des classes Tailwind `md:`, `lg:`

## 🎯 Fonctionnalités à venir

- [ ] Navigation entre les pages
- [ ] Intégration API manga/NFT réelle
- [ ] Système d'authentification
- [ ] Mode sombre/clair
- [ ] Filtres et tri avancés
- [ ] Favoris et wishlist
- [ ] Responsive mobile complet
- [ ] Animations de transition entre pages


## 🙏 Remerciements

- Design inspiré de la communauté Figma
- Icônes par [Lucide](https://lucide.dev/)
- Framework [SvelteKit](https://kit.svelte.dev/)

---

Développé avec ❤️ et beaucoup de ☕