# Le Comptoir des nuages

Un café dans un dirigeable, au-dessus d’un archipel suspendu. Une première version jouable de gestion douce, avec illustrations détaillées, six voyageurs distincts et une progression sans compte ni chronomètre.

**[Jouer dans le navigateur](https://zachiran42.github.io/le-comptoir-des-nuages/)** · **[Télécharger l’APK Android](https://github.com/Zachiran42/le-comptoir-des-nuages/releases/latest/download/le-comptoir-des-nuages-0.1.0.apk)** · **[Cercle Store](https://zachiran42.github.io/cercle-store/)**

## Une première traversée

- Six escales au choix, avec des ambiances et réductions au marché différentes. Le salon illustré est commun aux escales, avec variations de lumière et de météo.
- Six voyageurs, portraits et silhouettes distincts, trois fragments de dialogue par personnage et liens persistants.
- Six recettes déverrouillées pendant les quatre premiers services. Chauffe manuelle avec zone de réussite, ou service détendu automatique.
- Réserve de sept ingrédients, prix selon l’escale, pourboires et quatre aménagements permanents. Plantes et lanternes apparaissent dans la scène ; les autres aménagements apportent des avantages de service.
- Six commandes par service. Aucun client ne part à cause du temps passé ; une eau fraîche gratuite permet de continuer même sans provisions ni pièces.
- Après la découverte des six ports, les traversées restent rejouables. Il ne s’agit pas encore d’une campagne longue, d’un système de cuisine libre ou d’un éditeur d’intérieur.

## Jouer

Touchez **Préparer** sur la carte d’un voyageur, puis **Préparer cette boisson** au comptoir. Lancez la chauffe et arrêtez l’aiguille dans la zone verte. Servez ensuite la bonne commande. Une tasse imparfaite reste servable. Discutez avec les voyageurs pour créer des liens et améliorer le pourboire.

Les pièces servent à acheter des provisions ou à aménager le dirigeable. Les réserves, liens et achats restent à bord pendant les voyages. Après six commandes, choisissez un port sur la carte et levez l’ancre.

## Android et sauvegardes

APK universel pour Android 8+ avec **Android System WebView à jour**. Le jeu, les illustrations et les sons synthétisés sont embarqués ; aucune permission Internet, publicité, analyse ou connexion à un compte. Le navigateur sert d’aperçu et doit charger la page ; l’APK fonctionne hors ligne dès l’installation.

Le carnet est enregistré sur cet appareil après les actions. Les réglages proposent un export/import JSON pour le transférer ou le conserver avant désinstallation. Les sauvegardes du navigateur et de l’APK sont distinctes. L’import demande confirmation avant remplacement. Un carnet invalide est rejeté et une copie précédente est utilisée si elle est exploitable.

Cette version utilise une clé de développement conservée hors du dépôt. Aucun essai sur téléphone physique n’a été effectué ici : les interactions web ont été vérifiées dans le navigateur et l’APK a été compilé et sa signature contrôlée.

## Développement

Sans dépendances npm : `npm test`, `npm run check`, `npm run preview` (port 8815). Les sources web dans `docs/` sont les mêmes que celles embarquées dans l’APK. Le moteur économique et la progression sont isolés dans `docs/engine.js` et testés sous Node.

Pour Android, copiez `.toolchain.example.json` vers `.toolchain.json` et renseignez JDK, Android SDK et build-tools. Fournissez votre propre clé et définissez `MINIGAMES_KEYSTORE_PASSWORD`, puis :

```powershell
./scripts/build.ps1 -KeyStore C:/chemin/cle.jks -KeyAlias comptoir
```

Le script utilise PowerShell 7, `javac`, `aapt2`, `d8`, `zipalign`, `apksigner` et embarque les ressources de `docs/`. La clé et les chemins privés sont exclus du dépôt.

Code et ressources sous [licence MIT](LICENSE). Illustrations originales générées avec l’outil imagegen intégré, puis intégrées au jeu. Direction artistique, personnages et briefs dans [ART-DIRECTION.md](ART-DIRECTION.md). Contrôles et limites dans [VALIDATION.md](VALIDATION.md).
