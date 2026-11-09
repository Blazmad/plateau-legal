# plateau-legal

Pages légales publiques de l'app iPhone **Plateau** (suivi des calories, des macros et des fibres),
à servir par GitHub Pages.

| Page | URL (valable après publication) |
|---|---|
| Accueil | https://blazmad.github.io/plateau-legal/ |
| Politique de confidentialité | https://blazmad.github.io/plateau-legal/confidentialite/ |

**Pas encore publié.** Ce dépôt est local. Il ne devient public (`Blazmad/plateau-legal`, GitHub
Pages sur la branche `main`, dossier racine) qu'avec l'accord de Clément. Il ne contiendra que du
HTML statique, parce qu'Apple exige une URL publique pour la politique de confidentialité. Le code
de l'app vit dans `Code/Plateau`.

**Adresse de contact à confirmer.** `plateau.app@outlook.com` est provisoire : la boîte n'est pas
encore créée. Une fois l'adresse confirmée, la remplacer dans `confidentialite/index.html` (deux
liens `mailto:` et leur texte), dans `index.html` (un lien, page d'assistance) et dans `PlateauKit/Sources/PlateauKit/AppInfo.swift`
(`AppInfo.contactEmail`), qui doivent toujours être identiques.

Ce que dit la politique a été vérifié sur le code de l'app le 9 novembre 2026 (feature #17) : deux
appels réseau, `OFFClient` (`https://world.openfoodfacts.org/api/v2/product/<code>.json`, seulement
pour un code-barres sans fiche locale et hors codes propres au magasin) et `OFFSearchClient`
(`https://search.openfoodfacts.org/search`, recherche par nom, texte réduit à ses mots, à partir de
3 caractères), `PrivacyInfo.xcprivacy` sans pistage ni donnée collectée. Toute nouvelle connexion réseau dans l'app impose de revoir cette page.

Toute modification de la politique : changer la date « Dernière mise à jour » en tête de page.

## Contenu

- `index.html` : page d'accueil (URL d'assistance de la fiche App Store) : lien vers la politique et adresse de contact.
- `confidentialite/index.html` : politique de confidentialité.
- `assets/` : feuille de style aux couleurs de la marque (Brume, Encre, Marine, Gris d'atelier ;
  Instrument Sans via Google Fonts), logo horizontal et favicons copiés de
  `Code/Plateau/brand/logo/session-neutre/final/` (`assemblages/` et `web/`). Le manifeste
  `site.webmanifest` utilise des chemins relatifs, car le site est servi sous `/plateau-legal/`.
- `.nojekyll` : GitHub Pages sert les fichiers tels quels.
