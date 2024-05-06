# Workshop Unreal Partie 1

## Prérequis pour installer Unreal Engine 4.24.3 :

Vous devez installer le launcher Epic Games sur votre système. Vous pouvez le télécharger depuis le site officiel d'Epic Games : [Epic Games Launcher](https://store.epicgames.com/fr/download).

**Configuration minimale requise pour Unreal Engine 4.24.3 :**

- Système d'exploitation : Windows 7/8/10 64-bit
- Processeur : Quad-core Intel or AMD, 2.5 GHz ou plus rapide
- Mémoire vive (RAM) : 8 GB
- Carte graphique (obligatoire) : DirectX 11 compatible (NVIDIA GeForce GTX 470 ou AMD Radeon HD 6870 ou équivalent)
- Espace disque : 20 GB d'espace libre

## Introduction

Bienvenue dans ce workshop d'introduction à Unreal Engine ! Dans cette partie, nous allons explorer les bases de l'utilisation d'Unreal Engine, y compris son interface utilisateur et les techniques de navigation dans l'éditeur. Normalement, vous devriez avoir installé Unreal Engine sous la version 4.24.3 avant ce workshop.

## Unreal Engine qu'est-ce que c'est ?

Unreal Engine est un moteur de jeu développé par Epic Games, largement utilisé dans l'industrie du jeu vidéo mais également dans des domaines tels que la simulation, l'architecture, la réalité virtuelle, la réalité augmentée et le cinéma. Voici une présentation détaillée de ses principales caractéristiques :

**Puissance Graphique**
Unreal Engine est réputé pour sa puissance graphique exceptionnelle. Il offre des capacités avancées de rendu en temps réel, avec des effets visuels de haute qualité, tels que l'éclairage dynamique, les ombres en temps réel, les effets de particules sophistiqués, les effets de post-traitement et bien plus encore. Ces fonctionnalités permettent aux développeurs de créer des mondes virtuels immersifs et époustouflants.

**Outils Intuitifs**
L'interface utilisateur d'Unreal Engine est conçue pour être intuitive et conviviale. Elle offre une large gamme d'outils pour la création de jeux, y compris des éditeurs de niveaux, des éditeurs de matériaux, des outils d'animation, des outils de modélisation, et bien plus encore. Ces outils permettent aux développeurs de donner vie à leur vision créative de manière efficace et sans heurts.

**Flexibilité et Personnalisation**
Unreal Engine est extrêmement flexible et personnalisable. Il offre un langage de script visuel appelé Blueprint, qui permet aux développeurs de créer des fonctionnalités de jeu complexes sans écrire une seule ligne de code. De plus, Unreal Engine prend en charge le langage de programmation C++, ce qui offre aux développeurs une grande liberté pour personnaliser et étendre le moteur selon leurs besoins spécifiques.

**Déploiement Multiplateforme**
Unreal Engine prend en charge le déploiement sur une variété de plateformes, y compris PC, consoles de jeu, appareils mobiles, réalité virtuelle, réalité augmentée et plus encore. Cela permet aux développeurs de créer un jeu une fois et de le publier sur plusieurs plateformes, ce qui leur permet d'atteindre un public plus large et de maximiser leur potentiel de revenus.

En résumé, Unreal Engine est un moteur de jeu puissant, flexible et polyvalent, qui offre aux développeurs les outils nécessaires pour créer des expériences interactives immersives sur une multitude de plateformes. Que ce soit pour développer des jeux vidéo, des simulations ou des expériences virtuelles, Unreal Engine est un choix populaire et éprouvé dans l'industrie.

## Blueprint vs C++

### Blueprint :

**Avantages :**

1. Accessibilité : Blueprint est conçu pour être accessible aux non-programmeurs. Son interface visuelle intuitive permet de créer des logiques de jeu et des fonctionnalités "sans écrire de code".

2. Rapidité de Développement : Grâce à son interface visuelle et à sa facilité d'utilisation, le Blueprint permet un développement rapide de prototypes et d'itérations de gameplay.

3. Visualisation Immédiate : Les scripts Blueprint peuvent être visualisés directement dans l'éditeur Unreal Engine, ce qui permet de voir instantanément le comportement des objets et des acteurs dans le monde de jeu.

**Inconvénients :**

1. Performance : Dans certains cas, les scripts Blueprint peuvent être moins performants que le code C++, car ils sont généralement interprétés au moment de l'exécution plutôt que compilés en langage machine.

2. Complexité Limitée : Bien que puissant, le Blueprint peut devenir difficile à gérer pour des logiques de jeu très complexes. Les projets massifs avec beaucoup de scripts Blueprint peuvent devenir difficiles à organiser et à débuguer.

### C++ :

**Avantages :**

1. Performance : Le code C++ est compilé en langage machine, ce qui lui permet d'être plus performant que les scripts Blueprint dans de nombreux cas, notamment pour les opérations intensives en calcul.

2. Contrôle Total : En utilisant C++, vous avez un contrôle total sur le moteur Unreal Engine. Vous pouvez accéder à toutes ses fonctionnalités et optimiser votre code selon vos besoins spécifiques.

3. Réutilisabilité : Le code C++ est plus facile à réutiliser et à partager entre différents projets. Il est également plus facile à intégrer avec des bibliothèques tierces et des outils externes.

**Inconvénients :**

1. Courbe d'Apprentissage : L'apprentissage du C++ peut être plus difficile pour les débutants et pour ceux qui n'ont pas d'expérience en programmation. Il nécessite une compréhension plus approfondie des concepts de programmation et de la syntaxe du langage.

2. Temps de Développement : Le développement en C++ peut prendre plus de temps que le développement en Blueprint, en raison de la nécessité d'écrire et de débug du code, ainsi que de la compilation nécessaire à chaque modification.

## Création du projet
Tout d'abord, vous allez lancez Unreal via le launcher d'Epic Games avec la version que vous avez installé.

![launcher_epic](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/71fdbfac-e7c0-464a-88ab-7091d9f1a041)

![launcher_2](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/81cf2f77-a561-4c1c-b21e-b271eada6c9e)

![version_moteur](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/fd296cc2-7baf-4a0c-a2c3-77c3d36bd279)

Maintenant vous allez créer un projet afin de découvrir le logiciel ainsi que son interface.
Dès que vous avez lancez le logiciel vous devrez tomber sur une interface contenant ceci :

![create_project](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/d75faaa4-bba8-4994-8ab8-aab213ddf972)

Vous allez sélectionner Games car nous souhaitons créer un jeu.
Comme dis au dessus nous pouvons créer plusieurs type de projet avec Unreal voici les types autre que les jeux vous pouvez choisir.
Dès que vous avez sélectionnez "Games" vous pouvez appuyer sur le bouton Next en bas à droite.

## Template

Après nous allons choisir le "Template".

Qu'est-ce que c'est les "Templates" ?

Les "templates" sur Unreal Engine sont des modèles de projet préconfigurés qui fournissent une base de départ pour différents types de jeux ou d'applications interactives. Lorsque vous créez un nouveau projet dans Unreal Engine, vous avez la possibilité de choisir parmi plusieurs templates prédéfinis, chacun étant conçu pour répondre à des besoins spécifiques. Voici quelques-uns des templates couramment disponibles dans Unreal Engine :

1. Blank (Vide) : Ce template fournit une scène vierge sans aucun contenu préconfiguré, idéale pour démarrer un nouveau projet à partir de zéro.

2. First Person (Première Personne) : Ce template est conçu pour les jeux à la première personne, comme les jeux de tir ou les jeux d'aventure immersifs. Il inclut une caméra à la première personne et des mécaniques de mouvement de base.

3. Flying (Vol) : Ce template est orienté vers les jeux mettant en vedette des personnages ou des objets volants, comme les simulateurs de vol ou les jeux d'exploration aérienne.

4. Handheld AR (Réalité Augmentée Portable) : Ce template est spécialement conçu pour les applications de réalité augmentée sur appareils mobiles, offrant des fonctionnalités spécifiques pour interagir avec le monde réel à travers la caméra du périphérique.

5. Puzzle (Puzzle) : Ce template est destiné aux jeux de réflexion et de puzzle, avec des mécanismes de jeu spécifiques pour résoudre des énigmes et des défis.

6. Rolling (Roulement) : Ce template est axé sur les jeux de roulis et de boule, où le joueur contrôle une boule roulante à travers des niveaux complexes.

7. Side Scroller (Défilement Latéral) : Ce template est conçu pour les jeux de plateforme en 2D où le personnage se déplace de gauche à droite à travers des niveaux.

8. 2D Side Scroller (Défilement Latéral 2D) : Ce template est similaire au template de Side Scroller, mais avec une orientation spécifique pour les jeux en deux dimensions.

9. Third Person (Troisième Personne) : Ce template est destiné aux jeux à la troisième personne, comme les jeux d'action-aventure ou les jeux de plateforme. Il inclut une caméra à la troisième personne et des mécaniques de mouvement adaptées.

10. Top Down (Vue de Dessus) : Ce template est conçu pour les jeux avec une perspective de vue de dessus, tels que les jeux de stratégie en temps réel ou les jeux d'aventure isométriques.

11. Twin Stick Shooter (Tir à Double Stick) : Ce template est centré sur les jeux de tir à double stick, où le joueur contrôle un personnage avec un stick pour se déplacer et un autre pour viser et tirer.

12. Vehicle (Véhicule) : Ce template fournit une base pour les jeux mettant en vedette des véhicules, comme les jeux de course, les simulateurs de conduite ou les jeux d'action à bord de véhicules.

13. Virtual Reality (Réalité Virtuelle) : Ce template est spécialement conçu pour les jeux et les expériences en réalité virtuelle, offrant des fonctionnalités spécifiques pour une immersion maximale dans le monde virtuel.

14. Vehicle Advanced (Véhicule Avancé) : Ce template étendu offre des fonctionnalités avancées pour les jeux mettant en avant des véhicules, avec un contrôle plus précis et des options de personnalisation supplémentaires.

Nous allons nous focaliser sur la troisième personne donc veuillez bien à sélectionner le template "Third Person"

![type_project](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/26376ab3-d30e-4fd5-8f48-b9a9f42a56ba)

Vous pouvez appuyer sur le bouton Next.

Maintenant on peut personnaliser notre projet :

1. Blueprint/C++ : Vous pouvez choisir entre créer votre projet avec le système de script visuel "Blueprint" d'Unreal ou en utilisant le langage de programmation C++. Blueprint est plus accessible pour les non-programmeurs, tandis que C++ offre un contrôle plus granulaire et des performances potentiellement meilleures.

2. Qualité Graphique : Vous pouvez sélectionner le niveau de qualité graphique par défaut pour votre projet. Les options incluent des paramètres de rendu bas, moyens, élevés ou cinématiques, qui ajustent automatiquement les réglages graphiques pour correspondre à différentes configurations matérielles.

3. Ray Tracing : Si votre carte graphique prend en charge le ray tracing, vous pouvez activer cette fonctionnalité pour votre projet. Le ray tracing permet des effets d'éclairage et de réflexion plus réalistes, mais il nécessite une carte graphique compatible et peut avoir un impact sur les performances.

4. Plateforme de Déploiement : Vous pouvez choisir la plateforme sur laquelle vous souhaitez déployer votre projet, comme Windows, macOS, iOS, Android, etc. Cette sélection influence les options disponibles dans le projet, ainsi que les configurations par défaut.

5. Starter Content : Vous avez la possibilité d'inclure ou d'exclure le contenu de départ (Starter Content) dans votre projet. Le contenu de départ comprend des modèles 3D, des textures, des matériaux et des effets sonores préfabriqués qui peuvent être utiles pour démarrer rapidement le développement de votre jeu.

![project_settings](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/ed6ea9db-7f7d-4bb8-b73e-617beb3c4907)

Pour les paramètres on ne changera rien on laisse tel quel donc :

- Blueprint.
- Maximum Quality (Vous pouvez baisser si votre configuration n'est pas élevé).
- Raytracing Disabled
- Desktop/Console
- With Starter Content

Une fois que vous avez configuré ces paramètres selon vos besoins, vous pouvez cliquer sur le bouton "Create Project" (Créer le Projet) pour générer un nouveau projet avec les options que vous avez choisies. Ces paramètres vous permettent de personnaliser la base de votre projet dès le début, en vous donnant le contrôle sur des éléments tels que le langage de programmation, la qualité graphique, le rendu avancé et la plateforme cible.

## Interface

Comme tout les logiciels on aura le File, Edit, Window et Help nous utiliserons que certains d'entre eux bientôt !
Dès que votre projet lancé vous découvrerez l'interface global d'Unreal :

![interface_global](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/cd1d34c8-50fe-41b0-a4ba-a36324166fb0)

Vous trouverez plusieurs parties :

**1. Viewport :**
C'est la fenêtre principale où vous pouvez visualiser et interagir avec votre scène en 3D. Vous pouvez y naviguer, placer des objets, ajuster l'éclairage et visualiser vos effets en temps réel.
La où vous pourrez jouer votre jeu en simulation.

![viewport](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/ed63d893-bcde-4241-abac-94ededfd5388)

Le viewport d'Unreal Engine est équipé de plusieurs outils qui vous permettent de naviguer dans votre scène, d'interagir avec les objets et d'effectuer des ajustements en temps réel. Vous pouvez voir en bas à gauche du viewport trois axes avec des couleurs ce qui correspondera avec le nom des axes renseignés.
Voici une liste des principaux outils disponibles dans le viewport :

**- Côté haut à gauche :**

![opt](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/f47b24da-c4d5-4559-a89d-daabe81ef760)

Vous trouverez en cliquant sur la flèche les viewport options.
Vous pouvez utiliser différentes options mais celles qui sont le + utiles sont le show FPS et après vous pouvez changer le FOV du viewport et d'autres choses mais ça reste personnel au niveau des options.
Si vous désirez changer vous pouvez les changer.

![vp_opt](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/24c9c0e2-e0a3-4667-92f9-6d3cb475f7d5)

Ensuite où il y a marqué Perspective c'est la vue de comment sera votre viewport.
Changer cette option est souvent récurrente lorsqu'on doit aligner des objets dans notre scène, en utilisant la vue de face, de gauche, de droite, ...

![type_view](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/6d5cc725-3a15-42db-a2ed-18ac0583cb02)

Vous avez le View mode (où il y a marqué Lit).
Cette option sera très utile, vous utiliserez souvent le mode Lit et Unlit.
Par exemple le monde Unlit enlève toutes les lumières de la scène donc plus d'ombre.
Si vous faites un jeu d'horreur qui aura tendance à être sombre ou dans un lieu fermé par exemple avec très peu de lighting le mode Unlit sera très utile afin de placer des éléments ou autres.

![view_mode](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/1cc25b58-1cfd-4d2d-b6c8-28f46d6e0f24)

Le Show est une option où l'utilisation sera très rare mais cliquez dessus et regarder ce que vous pouvez afficher ou enlever.

![show_flags](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/9453f6af-741d-4870-8156-a4b5078590b4)

**- Côté haut à droite :**

![transform_cam_tooltip](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/417eb20a-c1ac-497d-a68a-a079598c6de8)

Nous commençons avec le transform qui peut être utilisé grâce à des raccourcis : W pour les translations, E pour les rotations et R pour le scaling.
Soit vous utilisez les raccourcis où vous pouvez cliquez directement dessus.

Le W (Translate) sert à déplacer des objets dans la scène sur les trois axes, vous pouvez évidemment bouger sur un, deux ou même trois axes en même temps grâce au demi-carré présent sur l'axe lorsque vous cliquez sur l'objet.
Le E (Rotate) sert à tourner des objets dans la scène sur les trois axes.
Le R (Scale) sert à redimensionner des objets présents dans la scène sur les trois axes, vous pouvez évidemment le scale sur un, deux ou même trois axes en même temps grâce à une ligne présente entre deux axes.
Mais attention pour le scaling pour que l'objet soit uniforme il doit avoir la même valeur sur les trois axes.
Vous pouvez également effectuer une sélection multiple en maintenant la touche Shift enfoncée tout en cliquant, qui fonctionne avec chaque outil.

Ensuite, vous verrez une grille, un triangle et une flèche en orange.
Cela signifie que la valeur où vous aller translate, rotate ou scale votre objet sera par la valeur à droite de chacun d'entre elle.
Si vous décochez l'une d'entre elle cela fera une unité par une unité.
Mais évidemment si vous cliquez sur la valeur présente à droite de chaque figure, cela vous donnera une liste déroulante avec la valeur que vous souhaitez translate, rotate ou scale votre objet dans la scène.

Pour le derniere ça sera pour la caméra, vous pouvez déplacer votre caméra dans le viewport, en restant appuyer sur le clic droit vous pouvez bouger la "tête" et pour vous déplacer : W pour avancer, S pour reculer, A pour aller à gaucher et D pour aller à droite.
Vous pouvez aussi utiliser la molette afin de zoomer et dézoomer.
Au début vu que nous sommes dans un petit level (map) la vitesse de déplacement de caméra est ok.
Mais si nous sommes sur une map très grande nous pouvons changer cette vitesse de déplacement.
Vous trouverez en haut à droite le dernier bouton qui est lié à la caméra.
Lorsque vous cliquez dessus vous verrez une barre que vous pouvez scale à la vitesse que vous voulez et cela changera la vitesse de la caméra :

![vitesse_cam](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/7d93bf84-5601-4b41-af51-294800e6fc39)

**2. World Outliner :**
Il s'agit d'une liste hiérarchique des objets de votre "niveau" aussi appelé "Level". Vous pouvez y trouver des acteurs tels que des personnages, des objets, des lumières, etc. Vous pouvez également les organiser en groupes et les manipuler facilement.

![world_outliner](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/da676b27-4e9f-4275-a57c-d7d86f6435c5)

**3. Details Panel :**
C'est là que vous pouvez affiner les propriétés des objets sélectionnés dans la scène. Vous pouvez ajuster les paramètres tels que la position, la rotation, l'échelle, les matériaux, les collisions, etc.
Pour avoir accès aux détails de votre actor (objet) présent dans la scène vous avez juste à cliquer dessus.

![detail_panel](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/2a3ec0c0-669f-417b-a862-a942eab0d758)

**4. Modes Panel :**
Ce panneau contient les différents modes de construction et d'édition, tels que le mode Sélection, le mode Placement d'objets, le mode Édition de paysage, etc. Vous pouvez basculer entre ces modes pour effectuer différentes actions de conception.

![window_mode](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/f6e0a555-b7e1-4c8c-bcd4-20af4401b68f)

**- Mode placement d'objets :**

Ce mode vous permet d'ajouter de nouveaux objets à votre scène. Vous pouvez choisir parmi une variété d'acteurs prédéfinis tels que des objets statiques, des personnages, des lumières, des caméras, etc. Une fois que vous avez sélectionné un type d'objet, vous pouvez cliquer déposer dans le viewport pour le placer dans votre scène.

![place_objets](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/977bae81-488b-497c-8d7e-fa03ab17dd6d)

**- Mode Paint (Peinture) :**

Ce mode est utilisé pour peindre des textures et des matériaux sur votre paysage ou d'autres surfaces. Vous pouvez choisir parmi une variété de textures et de matériaux prédéfinis, ajuster la taille et l'opacité du pinceau, et peindre directement dans le viewport pour ajouter des détails visuels à votre scène.

![paint](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/b8b3183a-ece2-4b07-bd18-ab1cba549368)

**- Mode Landscape (Paysage) :**

Le mode Landscape est spécialement conçu pour l'édition et la personnalisation des terrains dans votre scène. Vous pouvez utiliser des outils de sculpture pour modifier la forme du terrain, peindre des textures pour ajouter des détails, et ajouter des éléments tels que des rochers, des arbres et de la végétation pour enrichir votre paysage.

![landscape](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/ef6ba58a-c092-41b3-8fae-62d609454db9)

**- Mode Foliage (Végétation) :**

Ce mode est utilisé pour ajouter de la végétation et des éléments de nature à votre scène. Vous pouvez choisir parmi une variété d'objets de végétation prédéfinis tels que des arbres, des buissons, des fleurs, etc., et les placer dans votre paysage de manière réaliste. Vous pouvez également ajuster les propriétés de chaque élément de végétation, comme sa taille, son orientation et sa densité.

![folliage](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/35fe83be-ff96-400c-a77a-72099bc957bb)

**- Mode Geometry Editing (Édition de géométrie) :**

Ce mode est utilisé pour manipuler et éditer la géométrie des objets dans votre scène. Vous pouvez sélectionner, déplacer, faire pivoter et mettre à l'échelle des composants individuels tels que des vertices, des arêtes et des faces, pour modifier la forme et la structure des objets. C'est particulièrement utile pour des ajustements précis ou des modifications de dernière minute sur la géométrie de vos modèles 3D.

![geometry](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/d75a997c-6bce-40af-9685-8e8f97412672)

**5. Content Browser :**
C'est une fenêtre où vous pouvez parcourir, importer, organiser et gérer les ressources de votre projet telles que les modèles 3D, les textures, les matériaux, les animations, etc.

![content_browser](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/94c9540b-9eb9-4fd8-bcca-5d48fb9e404d)

## Exercice 1

**- Exploration du viewport :**

Passez du temps à explorer le viewport par vous-même. Utilisez les contrôles de la souris et du clavier pour naviguer dans la scène, zoomer et faire pivoter la caméra. Familiarisez-vous avec la façon dont vous pouvez visualiser votre projet sous différents angles et perspectives.

**- Sélection et manipulation d'objets :**

Sélectionnez différents objets dans la scène en utilisant l'outil de sélection. Pratiquez ensuite à les déplacer, les faire pivoter et les mettre à l'échelle en utilisant les outils correspondants. Expérimentez avec la sélection multiple et la manipulation des objets pour mieux comprendre leur comportement dans le viewport.

**- Placement d'objets :**

Essayez d'ajouter quelques objets prédéfinis à votre scène en utilisant l'outil de placement d'objets. Placez-les à différents endroits et ajustez leur position, rotation et échelle selon vos besoins. Cela vous aidera à vous familiariser avec le processus de création de votre propre environnement.

**- Modification des paramètres d'objets :**

Sélectionnez un objet dans la scène et explorez les différentes options disponibles dans le Details Panel. Cela vous donnera un aperçu des possibilités de personnalisation des objets dans Unreal Engine.

**- Utilisation des modes de vue :**

Essayez différents modes de vue disponibles dans le viewport.
Observez comment chaque mode de vue présente la scène différemment et comment cela peut vous aider dans votre processus de création.

## Blockout du level

Très bien, maintenant que vous en savez plus sur l'interface Unreal et que vous savez comment vous déplacer dans le viewport, nous allons faire du blockout.

**Mais qu'est-ce que c'est du blockout ?**

Le blockout, également connu sous le nom de blockmesh ou grayboxing, est une étape préliminaire dans le processus de conception de niveaux de jeu ou de scènes dans des logiciels comme Unreal Engine. Cette étape consiste à créer une représentation basique et géométrique de la scène à l'aide de formes primitives simples telles que des cubes, des sphères, des cylindres, etc.
L'objectif principal du blockout est de définir la disposition générale de la scène, les volumes d'espace, et les interactions de base sans se soucier des détails visuels ou des éléments artistiques.

**Mais à quoi ça sert ?**

Le blockout permet aux concepteurs de définir la taille, la forme et la disposition des éléments de la scène, tels que les pièces, les couloirs, les obstacles, etc. Cela aide à planifier et à visualiser la structure générale du niveau.
En utilisant des formes primitives simples, les concepteurs peuvent rapidement expérimenter et modifier la disposition de la scène sans investir de temps dans les détails artistiques.
Le blockout permet aux développeurs de tester les mécanismes de gameplay de base tels que la navigation du joueur, les interactions avec les objets, les obstacles et les combats. Cela permet de détecter et de résoudre les problèmes de conception dès les premières étapes du développement.
Le blockout fournit une base visuelle simple qui peut être partagée avec les membres de l'équipe de développement pour obtenir des commentaires et des idées. Cela facilite la communication et la collaboration entre les différents membres de l'équipe.
Cela est très utile lors des gros rush de projet lorsqu'on doit rendre un projet de jeu vidéo très rapidement comme une Game Jam par exemple.

## Exercice 2

Vous allez créer une nouvelle map donc un nouveau level.

Allez dans votre Content Browser, allez dans le dossier Content.
Faites Clique droit dans le content browser et New folder.
Vous le nommez comme vous le souhaitez mais celui-ci contiendra votre map que vous allez créer.
Maintenant vous allez créer un nouveau level, tout en haut à droite appuyer sur File > New level > Default.
Avant de faire quoi que ce soit dans le level on va save notre level.
Soit vous allez dans File > Save Current As et vous enregistrez votre nouveau level dans le dossier que vous avez créer.
Ou sinon vous faites Ctrl + S et vous le mettez dans votre dossier.
Aussi, il va falloir nommer votre level mettez le nom que vous souhaitez.
Vous pouvez supprimer le carré qui est présent actuellement sur le level.
Ensuite vous allez dans le Modes panel et appuyer sur landscape et vous allez créer un terrain (landscape).
Sélectionner la taille que vous voulez dans le Section Size mais je vous conseille le plus bas c'est-à dire 7x7 et ensuite vous pouvez cliquez sur Create.

Maintenant vous allez faire le blockout de votre level.
Vous allez utiliser la section geometry afin de faire ce blockout.

![blockout](https://github.com/Wavitoo/Workshop-Unreal-1/assets/114447473/5650cadf-44f0-48da-a077-fe3abe2d6eb6)

Vous voyez que vous avez plusieurs formes disponibles.
Lorsque vous mettez une de ces geometry dans le level vous pouvez voir dans le Details panel "Brush Settings".
Le Brush Type contient Additive et Substractive.
Additive veut dire que l'actor placé dans le level disposera d'une collision.
Subtractive l'actor ne sera pas visible mais sera utile à enlever de la surface sur d'autres objets uniquement de la catégorie geometry.
Donc subtractive vous sera utile si vous voulez faire des entrées, des fenêtres, etc...
Ensuite vous avez X, Y et Z qui sera le scaling sur ces trois axes.

Je veux que maintenant que vous avez votre landscape et que vous connaissez les paramètres afin de réaliser le blockout.
Créer ce que vous voulez que ça soit un labyrinthe, une salle, une maison quoi que ce soit faites parler votre imagination mais prenez en main le blockout.
Vous pouvez rajouter des éléments interactifs virtuel pour le moment par exemple des cônes pour un interrupteur ou quoi que ce soit d'autre.

Essayez de compléter de votre level.

## Contact
Si vous avez des questions ou besoin d'informations, veuillez me contacter à arslan.tetu@epitech.eu