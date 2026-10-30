# Missions innu-aimun : feuille de route

Dernière mise à jour : 30 octobre 2026

Outil web gratuit et non commercial pour apprendre le vocabulaire et les bases
grammaticales de l'innu-aimun (dialecte de Uashat mak Mani-utenam), en classe
et à la maison.

- Site des élèves : https://onirix42.github.io/missions-innu-aimun/
- Sources et crédits : https://onirix42.github.io/missions-innu-aimun/#apropos
- Dépôt : Onirix42/missions-innu-aimun
- Validation de la langue : Hubert Lessart (école Manikanetish), Virginie Michel
  (coordonnatrice des programmes, recherche et développement, ITUM)
- Direction de l'éducation d'ITUM : Yan-Daniel Vollant

## Principes

- On termine d'abord la base : genre, pluriel, possessifs, noms animés et
  inanimés, mots de liaison, verbes.
- On n'invente aucune donnée linguistique. Chaque forme a une source et un
  statut : « validé » ou « à valider ».
- Le matériel existant passe avant le programme : le classement reste souple,
  sans niveaux scolaires imposés.
- Sons du dialecte de Uashat seulement, sans synthèse vocale.
- Images : aucune image trouvée sur le Web. Illustrations produites dans le
  style de l'appli, et photos d'objets culturels innus prises par Eric Boily.
- `main` n'affiche que ce qui est prêt pour les élèves.

---

## Phase 0 — Stabilisation, droits et règles de travail (immédiat)

### Règles de travail
- [ ] Toujours faire `git pull` avant de modifier un fichier, localement ou sur GitHub.
- [ ] Ne jamais travailler directement sur `main` : une branche par chantier
      (`chantier-grammaire`, `chantier-virginie`, etc.).
- [ ] Fusionner dans `main` seulement après test et confirmation.
- [x] Ajouter `ROADMAP.md` à `main` (sans effet sur le site des élèves).
- [ ] Attendre le retour d'innu-aimun.ca avant toute saisie linguistique
      (genre, catégorie, pluriel).
- [ ] Ne jamais extraire le contenu d'innu-aimun.ca par script (extraction interdite).

### Droits d'utilisation et autorisations
- [x] Page #apropos en ligne : sources, sons lus depuis leurs sites d'origine,
      illustrations générées par IA.
- [ ] Présenter le courriel de demande à Yan-Daniel Vollant (rencontre de la
      semaine prochaine).
- [ ] Avec Yan-Daniel, vérifier ce que couvre l'entente sur l'éducation entre
      ITUM et Tshakapesh.
- [ ] Obtenir une autorisation écrite pour les sons :
  - [ ] Leçons d'innu (Institut Tshakapesh, Université Carleton / atlas-ling.ca,
        Université Memorial)
  - [ ] Atlas linguistique algonquien (phrases de Doris Vollant) : même équipe
        que les Leçons (atlas-ling.ca, Carleton), dans la même demande. Si l'Atlas
        n'est pas autorisé, retirer ces sons et mettre à jour #apropos.
  - [ ] Demander comment les créditer et si on peut copier les fichiers pour
        le mode hors ligne
  - [ ] Demander quels autres titulaires de droits consulter
- [ ] Conserver les réponses écrites dans le dossier du projet.
- [ ] Ne pas copier les MP3 dans le dépôt et ne pas les mettre en cache avant
      l'autorisation.
- [ ] Décider avec Yan-Daniel si le dépôt reste dans le compte personnel ou
      passe sous ITUM.
- [x] Illustrations des affiches de Virginie : trouvées sur Google. Elles ne vont
      ni dans l'appli, ni dans le dépôt, ni dans les instructions données à l'IA.
- [ ] Ne pas mettre les PDF des affiches dans le dépôt ni sur le site public.
- [ ] Vérifier l'origine des illustrations qui ne sont pas indiquées comme faites
      par IA (corps, couleurs, chiffres, calendrier).
- [ ] Vérifier que les conditions de l'outil de génération permettent de publier
      les images.
- [ ] Photos d'objets culturels : obtenir l'accord écrit de l'équipe de Virginie
      Michel (ou du propriétaire de l'objet) pour photographier et publier
      chaque objet, et savoir comment le créditer.
- [ ] Demander quels objets ne doivent pas être photographiés ni diffusés
      (objets sacrés, de cérémonie ou personnels).
- [ ] Préparer un formulaire de consentement pour les futurs enregistrements
      faits à Uashat.
- [ ] Compléter #apropos :
  - [ ] nommer les producteurs des sons (Tshakapesh, Carleton, Memorial);
  - [ ] ajouter « outil éducatif gratuit et non commercial »;
  - [ ] préciser qui a fourni les fiches papier;
  - [ ] indiquer l'origine des illustrations restantes (corps, fruits et légumes…);
  - [ ] ajouter une mention pour les photos d'objets culturels
        (« Photo : Eric Boily. Objet : [prêteur ou collection] »);
  - [x] ajouter #fruits aux adresses directes;
  - [ ] ajouter « utilisés avec l'autorisation de… » une fois l'autorisation reçue.

### Document pour Virginie
- [ ] Remplacer le passage sur le programme par le paragraphe « Enrichir
      l'application à partir du matériel existant ».
- [ ] Ajouter la signature, puis l'envoyer.

---

### Refonte de la page d'accueil (branche `refonte-accueil`)
- [x] Retirer les encadrés d'activités qui ressemblaient à des boutons.
- [x] Bandeau court avec « Comment jouer ? » (fenêtre d'aide) et « Pour les enseignants ».
- [x] Thématiques en premier, regroupées en sections.
- [x] Nom innu et nombre de mots sur chaque carte (tirés des données).
- [x] Défis propres à un thème lancés directement depuis la carte
      (Plateau, Muffins, Panier, Trier).
- [ ] Faire valider les noms des sections avec Virginie (et leur version innue).
- [ ] Tester avec des élèves (Hubert), sur tableau interactif et sur tablette.
- [ ] Fusionner dans `main` après les tests.
- [ ] Plus tard : recherche de mots, quand le matériel de Virginie sera intégré.

## Phase 1 — Modèle de données : genre et noms dépendants

- [ ] Ajouter à chaque mot : identifiant unique, catégorie, source, statut.
- [ ] Prévoir pour chaque mot des champs séparés : audio du mot, phrase
      d'exemple (innu), traduction, audio de la phrase, source et statut de la
      phrase (champs vides jusqu'à la phase 5).
- [ ] Remplir le genre (animé ou inanimé) à partir du dictionnaire innu-aimun.ca.
- [ ] Repérer les noms dépendants (parties du corps, parenté).
- [ ] Trancher ushkush / ussun (« son nez ») avec Virginie ou Hubert.
- [ ] Valider les mots en attente de Fruits et légumes (dont ka uishakak min et
      kushimash, présents dans le cahier de Virginie).
- [ ] Étendre « Animé ou inanimé ? » aux thématiques dont le genre est validé.

## Phase 2 — Pluriels

- [ ] Ajouter le pluriel de chaque nom, à partir du dictionnaire.
- [ ] Gestion intelligente du pluriel dans toutes les thématiques.
- [ ] Clarifier avec Virginie les terminaisons entre parenthèses du cahier
      ((an), (i), (a)).
- [ ] Mode d'entraînement singulier ↔ pluriel.
- [ ] Adapter les défis existants (plateau, panier, muffins) au pluriel.

## Phase 3 — Possessifs

- [ ] Ajouter les formes possessives (mon, ton, son), validées avec Hubert.
- [ ] Commencer par les noms dépendants du corps, puis les objets familiers.
- [ ] Missions associées, préparées selon le plan de cours d'Hubert.

## Phase 4 — Matériel de Virginie et nouvelles thématiques

- [ ] Transcrire le cahier (94 pages, environ 400 mots) dans le tableur :
      page | innu | fr | thème(s) | déjà dans l'appli ? | catégorie | pluriel |
      provenance et autorisation | audio Uashat ? | statut | notes
- [ ] Repérer les doublons dans le cahier et avec les mots de l'appli, sans
      fusion automatique.
- [ ] Questions pour Virginie :
  - [ ] traductions françaises;
  - [ ] graphies (kaipitshiminet / kaiapitshiminet,
        kamitshinanusht / kaminnanusht);
  - [ ] prononciation de Uashat.
- [ ] Ranger les mots dans les thèmes existants, dans de nouveaux thèmes ou dans
      la réserve « À classer ».
- [ ] Thématiques candidates : nombres (construction avec ashu), formes (à
      confirmer), animaux, village et école, saisons et météo.
- [ ] Comparer les couleurs du cahier avec la thématique actuelle.
- [ ] Bouton « Masquer / Afficher le texte » (on parle → on lit).
- [ ] Affichage d'une planche de 9 mots sur le tableau interactif.
- [ ] Nouvelles thématiques tirées du plan de cours annuel d'Hubert.

### Images et photos
- [ ] Créer STYLE-IMAGES.md : instructions de base, palette, cadrage, 3 ou 4 images
      de référence tirées de l'appli, et ce qu'il faut éviter (texte dans l'image,
      personnages connus, symboles autochtones génériques).
- [ ] Produire les illustrations par lots à partir de descriptions écrites, en
      commençant par les séries prioritaires (nombres, formes, animaux).
- [ ] Dessiner dans le code (SVG) les formes, les couleurs et les chiffres.
- [ ] Ne pas générer par IA les objets culturels innus : utiliser les photos
      prises par Eric Boily avec l'équipe de Virginie Michel.
- [ ] Séance photo des objets culturels :
  - [ ] dresser la liste des objets disponibles avec l'équipe de Virginie
        (nom innu, nom français, thème, prêteur);
  - [ ] cadrage uniforme : fond neutre, lumière douce, objet entier et centré,
        même format que les cartes de l'appli;
  - [ ] une photo principale par objet, plus des détails au besoin (matériaux,
        motifs);
  - [ ] retirer les métadonnées de localisation (GPS) avant la publication;
  - [ ] garder les originaux hors du dépôt; seules les versions web optimisées
        vont dans `img/`.
- [ ] Faire valider le nom innu, le sens et la présentation de chaque objet par
      Virginie ou Hubert (et par une personne qui connaît l'objet).
- [ ] Prévoir pour chaque objet une courte capsule culturelle (usage, matériaux),
      rédigée ou validée par l'équipe de Virginie, pour l'innu-aitun.
- [ ] Choisir la licence des photos d'Eric Boily (droits d'auteur conservés, ou
      licence libre non commerciale) et l'indiquer dans #apropos.
- [ ] Ajouter au tableur une colonne « image » : type (illustration / photo /
      SVG), à produire / produite / validée, crédit et autorisation.
- [ ] Plus tard : produire un cahier imprimable (planches de 9 mots, « on parle /
      on lit ») avec les images de l'appli, pour remplacer les affiches actuelles.

## Phase 5 — Verbes, mots de liaison et phrases

- [ ] Banque de verbes tirée du cahier (nipau, mitshishu, nikamu,
      mashinaitsheu…), formes et sens à valider.
- [ ] Mots de liaison simples, à choisir avec Hubert et Virginie.
- [ ] Premières phrases courtes.
- [ ] Modèle « mot + phrase courte » : on entend le mot, puis une phrase d'exemple.
- [ ] Bouton « écouter la phrase » à côté de 🔊 et 🐢.
- [ ] Faire des phrases de l'Atlas (Doris Vollant) les premiers exemples,
      quand elles correspondent au mot.
- [ ] Écrire et valider les phrases avec Hubert et Virginie (dialecte de Uashat),
      en suivant une même structure par thématique.
- [ ] Jeu de dés (nombres, sujets, verbes).

## Phase 6 — Hors ligne et enregistrements locaux

- [ ] Enregistrements de Uashat faits avec Hubert, Virginie ou d'autres
      locuteurs, avec un consentement signé.
- [ ] Enregistrer le mot et sa phrase dans la même séance, avec la même voix.
- [ ] Le formulaire de consentement couvre les mots et les phrases.
- [ ] Mode hors ligne (PWA), seulement pour les sons autorisés par écrit ou
      dont ITUM détient les droits.
- [ ] Remplacer progressivement les liens externes par des fichiers autorisés.

## Module complémentaire — moteur de jeu de dés Désire-moi

- [ ] À commencer une fois la base solide (phases 1 à 3).
- [ ] Réunir les deux projets GitHub pour Uashat et la Côte-Nord.
- [ ] Réutiliser le modèle de données et la gestion du pluriel.

---

## En attente

- Retour d'innu-aimun.ca.
- Réponses de Virginie (traductions, graphies, prononciation).
- Liste des objets culturels à photographier et accord de leurs prêteurs.
- Autorisations écrites pour les sons, demandées par Yan-Daniel Vollant.
- Portée de l'entente ITUM–Tshakapesh.
