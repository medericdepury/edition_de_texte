# Poèmes lyriques – Documentation du processus d’éditorialisation

## 1. Cadre du cours et objectifs

Ce travail s’inscrit dans le cadre du cours **Édition de texte : introduction à l'édition numérique avec TEI**.
Comme c’est le cas ici, nous tenons à rappeler que l’édition numérique revient le plus souvent à parler d’**édition de documents en ligne**.

Les limites sémantiques de l’HTML dans le cadre d’éditions critiques ou de corpus textuels structurés ayant été mises en évidence, l’édition suivant se fait en langage **Text Encoding Initiative (TEI)**, cadre normatif visant la standardisation, la structuration sémantique et l’interopérabilité des éditions de textes.

L’objectif de ce dossier est de documenter **l’ensemble du processus d’éditorialisation**, depuis le choix du corpus jusqu’à son encodage et à son exploitation, et non de présenter un résultat définitif ou exhaustif.

---

## 2. Choix du corpus et démarche éditoriale

Chaque étudiant·e a été amené·e à choisir un corpus-exemple personnel. Le corpus retenu ici est constitué de **poèmes lyriques mis en musique**, principalement au XIXe et au début du XXe siècle.

Les textes ont été sélectionnés à partir du site *The LiederNet Archive* et présentent une forte cohérence thématique autour du lyrisme, de la nature, de l’amour, du bonheur et de la souffrance.

---

## 3. Concept d’éditorialisation

L’éditorialisation implique :
- des choix d’optique et de finalité ;
- une structuration du corpus ;
- des décisions sémantiques (que baliser, comment, pourquoi) ;
- une anticipation des usages possibles de l’édition (lecture, exploration, analyse).

Dans ce projet, l’éditorialisation vise à rendre lisibles et exploitables les thématiques du lyrisme à travers une **annotation sémantique ciblée**.

---

## 4. Dépôt GitHub et organisation générale

Le projet est hébergé dans un dépôt GitHub personnel, mis en place dès le début du travail afin de structurer clairement les différents éléments de l’édition.

Le dépôt comprend :
- un dossier `documentation` (présent document, ODD) ;
- un dossier `documents_TEI` (document XML, schéma XSD, CSS)  ;
- la license.

---

## 5. Découverte et usage de la TEI

Dans ce projet, seules les parties nécessaires à la visée éditoriale de la TEI ont été retenues. Le choix et la personnalisation de cet ensemble ont été réalisés à l’aide :
- de l’application **Roma** ;
- d’un document de spécification **ODD** ;
- d’un schéma d’encodage **XSD**, permettant la validation des documents XML dans l’éditeur VSCode.

---

## 6. Structure générale du corpus TEI

Le corpus est structuré autour de l’élément racine `<teiCorpus>`, qui regroupe plusieurs documents `<TEI>` indépendants.

Chaque poème constitue une unité autonome et comprend :
- un `<teiHeader>` propre ;
- un `<text>` contenant le poème ;
- une structuration poétique interne.

Ce choix reflète la volonté de constituer un corpus cohérent tout en respectant l’individualité documentaire de chaque texte.

---

## 7. Métadonnées et en-tête TEI

Les métadonnées sont encodées dans `<teiHeader>`, notamment dans `<fileDesc>`.

On y trouve :
- le titre du poème ;
- l’auteur du texte poétique ;
- le compositeur, indiqué dans `<editor>`, en tant qu’intermédiaire musical ;
- la source du texte, avec un lien vers *The LiederNet Archive*.

Ce choix correspond à une conception large de l’édition, intégrant à la fois les dimensions textuelle et musicale.

---

## 8. Encodage de la poésie

Les poèmes sont encodés conformément aux recommandations de la TEI pour les textes versifiés :

- `<div type="poem">` pour identifier l’unité poétique ;
- `<lg>` pour les strophes ;
- `<l>` pour les vers ;
- l’attribut `rend="refrain"` pour signaler les refrains.

Cette structuration permet de préserver l’organisation métrique et formelle des textes, tout en facilitant leur exploitation ultérieure.

---

## 9. Annotation sémantique

Le cœur du travail éditorial repose sur une **annotation sémantique manuelle** réalisée à l’aide de l’élément `<seg>` et de l’attribut `ana`.

Les principaux champs sémantiques retenus sont :
- `Natur` : éléments naturels et paysages ;
- `Glück` : amour, bonheur, joie, apaisement ;
- `Pein` : souffrance, tristesse, douleur, manque.

Cette annotation constitue la base des explorations ultérieures du corpus.

---

## 10. Exploration du corpus avec XPath

Dans la continuité du cours, le corpus annoté en TEI a été exploré à l’aide d’expressions XPath.

Ces explorations ont permis notamment d’identifier les segments annotés par champ sémantique et d’observer la répartition des thématiques dans le corpus.

---

## 11. Dimension méthodologique et évaluative

Ce projet vise avant tout à mettre en pratique les compétences méthodologiques présentées dans le cadre du cours.

Il ne s’agit pas de produire une édition définitive ou parfaite, mais de démontrer la capacité à :
- concevoir une édition numérique ;
- structurer un corpus ;
- faire des choix d’encodage cohérents ;
- documenter l’ensemble du processus d’éditorialisation.

---

## 12. Sources

Les textes poétiques sont issus du site *The LiederNet Archive* : https://www.lieder.net/.
