# Roanne.info

Site web statique indépendant consacré à Roanne et au pays roannais. La page d'accueil met en avant le territoire, la Loire, le patrimoine, la culture, la gastronomie et la vie locale.

Le site ne nécessite ni framework, ni base de données, ni étape de compilation.

## Structure du projet

```text
.
├── index.html    # Page d'accueil, styles et données structurées
├── robots.txt    # Directives pour les robots d'indexation
└── sitemap.xml   # URL publique à explorer
```

Le dossier `images/` peut accueillir les futures ressources visuelles du site.

## Prévisualisation locale

Depuis la racine du dépôt, lancez un serveur HTTP local :

```bash
python -m http.server 8000
```

Puis ouvrez [http://localhost:8000](http://localhost:8000) dans un navigateur.

L'utilisation d'un serveur local plutôt que l'ouverture directe du fichier permet de tester le comportement dans des conditions proches d'un hébergement réel.

## Déploiement

Le projet peut être déployé sur n'importe quel hébergement de fichiers statiques, notamment :

- GitHub Pages ;
- Netlify ;
- Cloudflare Pages ;
- un serveur web classique.

Le domaine public doit servir les fichiers suivants à la racine :

- [`index.html`](./index.html) ;
- [`robots.txt`](./robots.txt) ;
- [`sitemap.xml`](./sitemap.xml).

Le site est configuré pour l'URL canonique `https://roanne.info/`. Si le domaine change, mettez à jour les URL absolues dans [`index.html`](./index.html), [`robots.txt`](./robots.txt) et [`sitemap.xml`](./sitemap.xml).

## Référencement naturel

La page d'accueil contient notamment :

- un titre et une meta description optimisés ;
- une URL canonique ;
- les balises Open Graph et Twitter Card ;
- les directives `robots` et `googlebot` ;
- des données structurées JSON-LD décrivant le site et son sujet géographique ;
- un sitemap XML déclaré dans `robots.txt`.

Après chaque ajout de page publique, ajoutez son URL dans [`sitemap.xml`](./sitemap.xml) et vérifiez que ses balises `title`, `description` et canonical correspondent à la page.

## Contribuer

1. Créez une branche dédiée.
2. Modifiez les fichiers nécessaires en conservant le HTML sémantique et l'accessibilité existante.
3. Vérifiez la page dans un navigateur, en version mobile et bureau.
4. Lancez un serveur local pour contrôler les liens et le rendu.
5. Ouvrez une Pull Request avec une description claire des changements.

Les contenus locaux doivent rester précis, vérifiables et respectueux des personnes et des lieux cités.

## Vérifications rapides

Avant de publier une modification :

- vérifier que le HTML reste valide ;
- contrôler les liens internes et les URL absolues ;
- vérifier le rendu avec les préférences de mouvement réduit et le mode sombre ;
- contrôler que [`robots.txt`](./robots.txt) référence bien [`sitemap.xml`](./sitemap.xml) ;
- ne pas ajouter de secret, de clé API ou de donnée personnelle au dépôt.
