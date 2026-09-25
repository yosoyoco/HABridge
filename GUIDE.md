# HABridge 1.2.1 — Guide utilisateur

Copyright © 2026 YoSoYoCo.

## 1. Présentation

Réglez le gain et le +48 V de vos préamplis directement dans la section PREAMP d’eMotion LV1. Pour commencer, associez votre console à son appareil SoundGrid dans HABridge Control.

**+48 V peut endommager ou perturber certains équipements. Vérifiez toujours le type de microphone, la source connectée et le câblage avant de l’activer ou de rappeler une session.**

## Soutenir HABridge

HABridge est gratuit. Si vous appréciez le projet, vous pouvez soutenir son développement sur [Ko-fi](https://ko-fi.com/yosoyoco). Le soutien est entièrement facultatif et ne débloque aucune fonction.

## 2. Compatibilité

HABridge 1.2.1 prend en charge les cartes SoundGrid WING, X-WSG et DN32-WSG avec les consoles compatibles Behringer WING, X32 et Midas M32, utilisées avec eMotion LV1.

HABridge permet de contrôler le gain et le +48 V des préamplis pris en charge par la console, y compris les préamplis accessibles via AES50.

HABridge est disponible pour Windows et macOS 12 ou version ultérieure. Sur Mac, HABridge Control est compatible Intel et Apple Silicon. Les modules Waves correspondant à l’interface SoundGrid utilisée doivent être installés.

Consultez la [liste des configurations compatibles](SUPPORTED_VERSIONS.md).

## 3. Installation et premier lancement

Reliez le port réseau de contrôle de la console à l’ordinateur qui exécute eMotion LV1, directement ou via un switch réseau.

1. Installez le module SoundGrid Waves correspondant à votre interface et vérifiez son fonctionnement dans LV1 avant d’installer HABridge.
2. Sauvegardez votre travail, puis fermez eMotion LV1.
3. Sous Windows : ouvrez le fichier HABridge-1.2.1-Windows.exe. La fenêtre HABridge Control s’ouvre : cliquez sur « Installer HABridge » et acceptez la demande d’autorisation de Windows. HABridge Control est alors disponible dans le menu Démarrer ; le fichier téléchargé n’est plus nécessaire.
4. Sous macOS : décompressez HABridge-1.2.1-macOS.zip, placez HABridge Control dans Applications, puis ouvrez-le. Si macOS refuse de l’ouvrir, ouvrez Réglages Système › Confidentialité et sécurité, puis cliquez sur « Ouvrir quand même ». Cliquez sur « Installer HABridge » et saisissez le mot de passe administrateur du Mac.
5. Dans eMotion LV1, affectez les appareils SoundGrid dans System Inventory, puis patchez leurs entrées vers les tranches souhaitées dans PATCH. Les commandes PREAMP correspondent aux sources ainsi affectées.
6. Laissez eMotion LV1 ouvert et ouvrez HABridge Control pour associer votre appareil (section 4).

### Mettre à jour HABridge

1. Sauvegardez votre travail, puis fermez eMotion LV1 et HABridge Control.
2. Sous Windows : ouvrez le nouveau fichier HABridge-…-Windows.exe. Sous macOS : remplacez HABridge Control dans Applications par la nouvelle version, puis ouvrez-la.
3. HABridge Control affiche « Mise à jour nécessaire » : cliquez sur « Installer cette version » et autorisez l’opération.

Vos associations sont conservées. Il n’est pas nécessaire de désinstaller l’ancienne version.

## 4. Associer un appareil

Associez chaque appareil SoundGrid à sa console.

1. Cliquez sur « Configurer ». Pour modifier une installation existante, utilisez « Gérer les appareils… ».
2. Choisissez l’appareil SoundGrid, puis cliquez sur « Rechercher les appareils ».
3. Choisissez sa console et cliquez sur « Associer ». Vérifiez les deux noms avant de confirmer.
4. Lorsque l’appareil est connecté, l’accueil affiche « Prêt » avec le nom de la console.

Si plusieurs consoles ont le même nom et le même modèle, utilisez le numéro de série affiché pour les distinguer.

« Modifier » permet de choisir une autre console pour l’appareil sélectionné. « Oublier » supprime uniquement l’association sélectionnée ; il ne désinstalle pas HABridge.

## 5. Plusieurs appareils

Vous pouvez associer plusieurs appareils compatibles. Chaque appareil SoundGrid conserve sa propre console associée.

Ouvrez « Gérer les appareils… » pour consulter, modifier ou supprimer une association. Les appareils sont retrouvés automatiquement après une reconnexion, même si leur adresse réseau a changé.

## 6. Sessions et rappel des préamplis

Le gain et le +48 V sont enregistrés avec la session LV1 lorsqu’ils sont pris en charge. Lors du chargement ou de l’ouverture d’une session, HABridge rappelle ces réglages sur les préamplis disponibles.

Avant de charger une session contenant du +48 V, vérifiez les microphones, les sources et le câblage connectés.

Une simple reconnexion réseau ne rappelle pas les valeurs de la session : HABridge commence par relire les réglages actuels de la console.

## 7. Déconnexion et reconnexion

Après la déconnexion d’un appareil, HABridge désactive immédiatement son contrôle. Control affiche « Appareil hors ligne ».

PREAMP peut rester visible dans LV1 sur certaines tranches non sélectionnées. **Un contrôle PREAMP encore visible reste inactif tant que l’appareil est hors ligne.** Sélectionnez la tranche pour actualiser son affichage.

À la reconnexion, les contrôles redeviennent disponibles automatiquement avec les réglages actuels de la console. Les commandes interrompues ne sont pas renvoyées.

## 8. Particularités des consoles

### WING — préamplis AES50 à paliers

Certains préamplis AES50 utilisent des paliers de gain analogiques plus larges que les pas disponibles dans LV1. Entre deux paliers, LV1 conserve la valeur demandée tandis que le préampli reste sur le palier inférieur.

Par exemple, en montant depuis **15,5 dB**, LV1 peut afficher **16, 16,5, 17 ou 17,5 dB** tandis que le préampli reste à **15,5 dB**. Lorsque LV1 atteint **18 dB**, le préampli passe à **18 dB**.

**Les valeurs intermédiaires n’ajoutent aucun gain numérique.** La valeur affichée entre deux paliers ne correspond donc pas au gain analogique effectivement appliqué.

Ce comportement concerne uniquement les préamplis utilisant ce type de grille. Les entrées LOCAL de la WING ne sont pas concernées.

### X32/M32

Sur les configurations compatibles X32/M32, HABridge utilise directement le contrôle de gain fourni par la console. Le gain peut évoluer par pas de 0,5 dB lorsque cette résolution est prise en charge par la configuration connectée.

## 9. Dépannage

### Le PREAMP n’apparaît pas

- Vérifiez que Control affiche « Prêt » et que l’association correspond à la bonne console.
- Vérifiez la source de la tranche LV1 et sa correspondance avec une entrée compatible.
- Vérifiez que la console et, le cas échéant, la stagebox sont connectées.

### Ma console n’est pas détectée

- Vérifiez qu’elle est allumée et que sa connexion réseau de contrôle est branchée.
- Dans « Gérer les appareils… », cliquez sur « Rechercher les appareils ».
- Si nécessaire, ouvrez « Avancé… » puis « Connexion manuelle… » et saisissez l’adresse IP affichée sur la console.

### Le gain ne change pas

- Vérifiez que l’appareil est connecté et que vous commandez le bon préampli.
- Sur WING avec préampli AES50 à paliers, une valeur intermédiaire peut laisser le gain analogique inchangé ; consultez l’exemple ci-dessus.
- Comparez la valeur affichée dans LV1 avec celle de la console.

### Le +48 V ne répond pas

- Vérifiez d’abord le type de source et le câblage ; ne répétez pas les commandes sans cette vérification.
- Vérifiez que l’appareil est connecté, puis comparez l’état du +48 V dans LV1 et sur la console avant d’essayer à nouveau.
- Si la réponse reste incertaine, ouvrez « Avancé… » puis « Ouvrir le journal ».

### Un PREAMP reste visible après une déconnexion

- Vérifiez l’état de l’appareil dans Control.
- Sélectionnez la tranche concernée pour actualiser son affichage.
- Rétablissez la connexion et attendez le retour de l’appareil avant toute commande.

### Une association a disparu

- Ouvrez « Gérer les appareils… » et vérifiez la liste.
- Si l’association a été oubliée ou supprimée lors d’une désinstallation, associez de nouveau le bon appareil à sa console.
- Si Control indique « Configuration à vérifier », ouvrez « Avancé… » puis « Ouvrir le journal ».

### HABridge indique « Appareil hors ligne »

- Vérifiez l’alimentation et la connexion réseau de la console associée.
- Vérifiez que l’association désigne toujours la console utilisée.
- Attendez sa détection automatique. Il n’est pas nécessaire d’oublier l’association pour une coupure temporaire.

Si ces vérifications ne suffisent pas, ouvrez « Avancé… » puis « Ouvrir le journal ». Avant de partager un journal, retirez les informations personnelles ou réseau inutiles.

## 10. Désinstallation

1. Sauvegardez votre travail et fermez eMotion LV1.
2. Dans HABridge Control, ouvrez « Avancé… », puis « Désinstaller HABridge… ».
3. Choisissez de conserver les associations pour une réinstallation ultérieure ou de les supprimer.

Les modules Waves d’origine restent nécessaires à votre installation et ne sont pas supprimés par cette opération.

## 11. Confidentialité et licence

HABridge ne nécessite aucun compte et n’envoie pas de télémétrie. Les associations, réglages locaux et journaux HABridge sont enregistrés sur votre ordinateur.

Dans Avancé, « Confidentialité », « Licence » et « Mentions légales » donnent accès aux documents correspondants. L’utilisation et la redistribution de HABridge sont régies par la licence fournie.

HABridge est indépendant de Waves, Behringer, Midas et Music Tribe. Les marques appartiennent à leurs propriétaires.
