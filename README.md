# La Tune Company — site vitrine

Site de La Tune Company : création de sites web pour les entreprises (Abidjan, Canada et à distance).

Site statique en HTML, CSS et JavaScript, sans bibliothèque externe. Hébergé sur Netlify, relié à ce dépôt GitHub : chaque modification envoyée sur la branche `main` met le site en ligne automatiquement.

## Les fichiers

| Fichier | Rôle |
| --- | --- |
| `index.html` | Le site complet : en-tête, accueil, services, réalisations, à propos, contact, pied de page. |
| `merci.html` | Page de confirmation après l'envoi du formulaire (utilisée seulement si JavaScript est désactivé). |
| `images/favicon-32.png` | Petite icône affichée dans l'onglet du navigateur. |
| `images/apple-touch-icon.png` | Icône utilisée quand on ajoute le site à l'écran d'accueil d'un téléphone. |
| `images/og-image.png` | Image affichée quand on partage le lien sur WhatsApp, Facebook, LinkedIn… |

## Le formulaire de contact

Le formulaire utilise **Netlify Forms** (attribut `data-netlify="true"`). Les messages arrivent dans Netlify, rubrique **Forms**. Pour les recevoir par e-mail : Netlify › ton projet › Project configuration › Notifications › Emails and webhooks › Form submission notifications.

## Faire une modification

- **Petit texte** : sur github.com, ouvrir `index.html`, cliquer sur le crayon, modifier, puis « Commit changes ». Le site se met à jour en une minute.
- **Changement plus important** : le demander à Claude en lui indiquant ce dépôt.

## Charte

- Logo : « LA TUNE » en Archivo Black + point orange, « COMPANY » en Space Grotesk avec un trait.
- Couleurs : noir `#111111`, blanc `#FFFFFF`, orange `#FF6B1A`.
- Polices : Archivo Black (titres), Space Grotesk (texte), hébergées sur le site dans `fonts/`.
