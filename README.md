# Battle Pic

Appli Android de la médiathèque de Servon-sur-Vilaine pour les photos du podcast **La Battle**.

- Viseur en direct avec le cadre La Battle par-dessus (la photo remplace le vert).
- Retardateur 3 s ou 10 s, caméra avant ou arrière, import depuis la galerie.
- Textes des deux cases blanches (bouton « Écrire dans les cases ») : 1 ou 2 lignes par case, chacune avec sa taille, dans la police du visuel (Urbanist). La case fait 80 px de haut avec une ligne, 100 px avec deux, ombres comprises. Les textes s'affichent dès le viseur et restent en mémoire pour les photos suivantes.
- Photo en noir et blanc (rendu mat légèrement froid, calé sur les visuels du podcast), intensité réglable de 0 à 100 % au recadrage.
- Recadrage après la prise : glisser pour déplacer, pincer ou curseur pour zoomer.
- Chaque photo est enregistrée en 2 versions 1080 × 1350 (format post Instagram), avec et sans filtre, dans l'album « Battle Pic » de la galerie.
- Bouton « Partager » pour envoyer les 2 photos vers Canva, Drive, etc.

## Installer

Télécharger `battle-pic.apk` depuis la release **latest** du dépôt, sur le téléphone, puis l'ouvrir.
Android demande d'autoriser l'installation d'applis depuis le navigateur : c'est normal pour une appli qui ne vient pas du Play Store.

Android 10 minimum.

## Construire

Chaque envoi sur `main` lance le workflow « Construire l'APK » (onglet Actions), qui compile l'APK signé et remplace la release `latest`.
La clé de signature est rangée dans les secrets du dépôt (`BATTLEPIC_KEYSTORE_B64` et `BATTLEPIC_KEYSTORE_PASSWORD`), jamais dans le code. Elle reste la même pour que les nouvelles versions s'installent par-dessus l'ancienne.

## Contenu

- `app/src/main/assets/index.html` : l'interface (page web embarquée, cadre inclus).
- `app/src/main/java/fr/servon/battlepic/MainActivity.java` : la coque Android (caméra, galerie, enregistrement, partage).
- Polices Anton, Barlow et Urbanist (licence SIL OFL) dans `app/src/main/assets/fonts/`.
