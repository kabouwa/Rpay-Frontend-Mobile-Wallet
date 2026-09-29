<p align="center"> <img src="https://raw.githubusercontent.com/kabouwa/Rpay-Frontend-Mobile-Wallet/main/assets/img/logos/Rpay.png" alt="Rpay" width="500"> </p>

# Rpay — Frontend Mobile Wallet

**Une interface de banque mobile / portefeuille numérique, entièrement responsive, construite from scratch en HTML5 et CSS3 pur — sans framework, sans librairie JS.**

Rpay est un concept front-end pour une banque internationale et un produit de portefeuille mobile. Ce projet a été construit pour apprendre en profondeur le développement web statique : structure de pages, CSS orienté composants, systèmes de layout (Flexbox + Grid), theming via CSS custom properties, et design responsive — sans Bootstrap, Tailwind, ni aucun framework JS.

🔗 Repo : [github.com/kabouwa/Rpay-Frontend-Mobile-Wallet](https://github.com/kabouwa/Rpay-Frontend-Mobile-Wallet)

🌐 Site : [kabouwa.github.io/Rpay-Frontend-Mobile-Wallet](https://kabouwa.github.io/Rpay-Frontend-Mobile-Wallet)

---

## ✨ Points forts

- **100% HTML5 & CSS3 écrit à la main** — chaque layout, animation et composant construit depuis zéro.
- **7 écrans entièrement designés**, partageant un seul design system cohérent.
- **Responsive par design** — grilles flexibles et media queries sur chaque feuille de style, du desktop au mobile.
- **Design system personnalisé** via variables CSS (`root.css`) : palette de couleurs complète (primary, success, warning, danger, muted, avec variantes light/dark), radius, ombres et dégradés cohérents sur toutes les pages.
- **Micro-interactions** : animation d'entrée logo/barre de chargement au chargement de page, états hover, mise en surbrillance de la nav active.
- **Police custom** (`Rpay Sans Big`) pour les titres, en accord avec l'identité de marque.

## 📱 Pages & Fonctionnalités

| Page | Ce qu'elle fait |
|---|---|
| **Landing (`index.html`)** | Page d'accueil marketing : pitch ("All your money, one smart wallet"), aperçu de solde en style live, support multi-devises, explication des frais transparents, et grille de fonctionnalités (transferts rapides, cartes liées, dashboard moderne, aide 24/7). |
| **Auth (`customer/auth/`)** | Écran combiné connexion / création de compte avec options de connexion sociale (Google, Facebook, LinkedIn) et un panneau visuel de marque en pleine hauteur. |
| **Dashboard (`customer/dashboard/`)** | Vue d'ensemble du compte : solde total, carrousel de cartes liées, flux d'activité récente, raccourci de transfert rapide vers les destinataires récents, et un panneau de statistiques revenus/dépenses. |
| **Wallet (`customer/wallet/`)** | Gestion de portefeuille multi-devises (USD / EUR / MAD), soldes par devise, cartes liées avec numéros masqués, ID de compte, limites journalières/mensuelles, et paramètres de sécurité. |
| **Transfer (`customer/transfer/`)** | Flux d'envoi d'argent : sélecteur de destinataire (avec destinataires récents), formulaire de détails de transfert, et conseils contextuels. |
| **Transactions (`customer/transactions/`)** | Historique complet des transactions avec filtres. |
| **Support (`customer/support/`)** | Centre d'aide avec vue de ticket / conversation de support. |

## 🛠️ Stack technique

- **HTML5** — balisage sémantique sur toutes les pages
- **CSS3** — Flexbox, CSS Grid, custom properties (design tokens), animations keyframe, effets glass en `backdrop-filter`, media queries
- **Font Awesome** pour les icônes
- Police custom embarquée pour les titres
- Aucun outil de build, aucune dépendance JS runtime — front-end statique pur

## 📂 Structure du projet

```
Rpay-Frontend-Mobile-Wallet/
├── index.html                    # Page d'accueil publique
├── customer/
│   ├── auth/index.html            # Connexion / Inscription
│   ├── dashboard/index.html       # Vue d'ensemble du compte
│   ├── wallet/index.html          # Portefeuille multi-devises
│   ├── transfer/index.html        # Envoi d'argent
│   ├── transactions/index.html    # Historique des transactions
│   └── support/index.html         # Centre d'aide
└── assets/
    ├── styles/                    # Une feuille de style par page + design system partagé (root.css)
    ├── fonts/                     # Police custom
    ├── icon/                      # Icônes app/navigateur
    └── img/                       # Illustrations & images
```

Chaque page vit dans son propre dossier avec un `index.html` (au lieu de fichiers `.html` à plat), pour permettre des URLs propres comme `/customer/dashboard/` une fois hébergé.

## 🎯 Ce que ce projet démontre

- Structurer un site multi-pages statique avec un design system partagé et réutilisable plutôt que des styles ponctuels par page
- Construire des patterns d'UI fintech from scratch : numéros de carte masqués, portefeuilles multi-devises, flux de transfert, flux d'activité
- Écrire du CSS maintenable à grande échelle avec des variables/tokens plutôt que des valeurs codées en dur
- Techniques de layout responsive sans framework CSS

## 🚀 Lancer le projet en local

⚠️ **Un serveur local est nécessaire** — le projet utilise des chemins relatifs à la racine (ex. `/assets/styles/root.css`), donc ouvrir `index.html` directement en double-cliquant (`file://`) ne fonctionnera pas correctement : le navigateur interprète `/` comme la racine du système de fichiers, pas comme la racine du projet.

```bash
git clone https://github.com/kabouwa/Rpay-Frontend-Mobile-Wallet.git
cd Rpay-Frontend-Mobile-Wallet
```

Puis lancer un serveur local, par exemple :

```bash
# Avec Python
python3 -m http.server 8000

# Ou avec Node
npx serve .

# Ou avec VS Code : extension "Live Server"
```

Puis ouvrir `http://localhost:8000` dans le navigateur.