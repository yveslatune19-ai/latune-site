# CLAUDE.md — site La Tune Company

Mode d'emploi du projet, lu au début de chaque séance. Site vitrine de La Tune Company (création de sites web pour entreprises, Abidjan, Canada et à distance).

## Charte

- **Logo (variante 3A, celle qui a été choisie)** : « LA TUNE » en majuscules, en Archivo Black, suivi du point orange `#FF6B1A`. En dessous, un trait horizontal mène à « COMPANY », écrit en Space Grotesk avec des lettres espacées. Il existe deux versions : texte noir sur fond blanc, et texte blanc sur fond noir. On n'utilise pas d'autre variante.
- **Couleurs** : noir `#111111`, blanc `#FFFFFF` et orange `#FF6B1A`. L'orange est la couleur du point du logo : on l'utilise comme accent, pas comme couleur de fond principale. Les couleurs sont définies en variables CSS dans `:root` (`--fg`, `--bg`, `--accent`…). Il faut toujours les utiliser, et ne pas écrire les codes couleur en dur.
- **Polices** : Archivo Black pour les titres, Space Grotesk pour le texte, toutes deux chargées depuis Google Fonts.
- **Ton** : le site parle au nom de l'entreprise, en « nous ». Les phrases sont simples et directes, et s'adressent au visiteur en « vous ».
- **Thème sombre** : le site suit le réglage clair ou sombre de l'appareil. Chaque changement doit être vérifié dans les deux thèmes.

## Règles de travail

- Expliquer en français simple, sans jargon. Si un terme technique est nécessaire, l'expliquer en une phrase.
- Proposer d'abord un plan court, puis **attendre l'accord** avant de modifier le code.
- Une seule fonctionnalité à la fois, avec une pull request par fonctionnalité.
- Aucune bibliothèque externe sans l'expliquer et sans demander l'accord avant. Par défaut, on utilise du HTML, du CSS et du JavaScript natifs.
- Tester sur téléphone (390 px de large) et sur ordinateur, et vérifier que la console du navigateur n'affiche aucune erreur.
- Respecter le réglage « réduire les animations » (`prefers-reduced-motion`) : dans ce cas, rien ne doit bouger.
- Animations : sobres et rapides (200 à 600 ms). On n'anime que `transform` et `opacity`. Le contenu doit rester visible même si JavaScript ne fonctionne pas : jamais de texte bloqué à `opacity: 0`.
- Accessibilité : l'état de focus au clavier doit toujours rester bien visible.
- À la fin, toujours résumer ce qui a changé, pourquoi, et comment le vérifier.

## Règles du site

- **Ne jamais inventer** de faux clients, de faux témoignages, de faux chiffres ou de fausses réalisations.
- **Garder le formulaire de contact Netlify intact** : `name="contact"`, `data-netlify="true"`, le champ caché `form-name`, le piège à robots `bot-field` (`netlify-honeypot`) et `action="/merci.html"`. Les noms des champs ne doivent pas changer.
- Toujours travailler sur une branche, puis ouvrir une pull request. Ne jamais envoyer directement sur `main`.
- Vérifier l'aperçu Netlify (Deploy Preview) sur téléphone et en navigation privée avant d'accepter une pull request.

## Fonctionnement technique

- `index.html` contient tout le site : HTML, CSS dans `<style>` et JavaScript dans `<script>`. `merci.html` est la page de confirmation du formulaire, utilisée si JavaScript est désactivé. Les images sont dans `images/`.
- Le dépôt GitHub `yveslatune19-ai/latune-site` est relié à Netlify : chaque changement fusionné sur `main` est mis en ligne automatiquement.
- Chaque pull request reçoit un aperçu Netlify à une adresse temporaire.
- Les messages du formulaire arrivent dans Netlify, rubrique **Forms**.
- Adresse du site : https://latunecompany.netlify.app
