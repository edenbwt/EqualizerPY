# Equalizer Interface Project

## Introduction
Ce projet consiste à créer une interface graphique en Python permettant de modifier les bandes de fréquences d’un fichier audio `.wav` en appliquant des filtres d’égalisation. L'interface est conçue pour un égaliseur à cinq bandes de fréquence, permettant un ajustement précis des fréquences sonores pour améliorer ou modifier la qualité audio.

## Objectif du Projet
L'objectif est de créer un égaliseur graphique qui modifie les fréquences d'un fichier `.wav` en ajustant indépendamment cinq bandes de fréquence. Ce projet vous permettra d'apprendre les bases du traitement de signal audio, la manipulation de filtres d’égalisation, et la création d'interfaces utilisateur en Python.

## Fonctionnalités
1. Sélection de fichier `.wav` : Un bouton permet de sélectionner un fichier audio `.wav` à traiter.
2. Bandes de fréquence : Cinq curseurs permettent de régler le gain de chaque bande de fréquence pour moduler le son.
3. Lancement du traitement : Un bouton de traitement applique les réglages et affiche dans le terminal les valeurs des réglages actuels des curseurs de fréquence.

## Algorithmes et Techniques Utilisés

### Algorithme de Filtrage
Chaque bande de fréquence de l’égaliseur est associée à un filtre passif avec un coefficient de gain réglable. Ces filtres permettent de renforcer ou d’atténuer certaines plages de fréquence, afin de modifier le spectre sonore du fichier audio.

### Types de Filtres Utilisés
1. Filtre Passe-Bas : Atténue les fréquences au-dessus d’un seuil, utilisé pour la bande basse.
2. Filtre Passe-Haut : Atténue les fréquences sous un seuil, utilisé pour la bande haute.
3. Filtres Passe-Bande : Utilisés pour les bandes médium-basses, médium, et médium-hautes, ils permettent d’ajuster le gain d’une plage de fréquence spécifique.

### Réponses Impulsionnelles des Filtres
Les réponses impulsionnelles des filtres illustrent comment chaque filtre réagit à une impulsion sonore. Elles montrent l'effet de chaque bande de fréquence et aident à visualiser le traitement sonore appliqué.

### Exemples de Réponses Impulsionnelles
- Basse (Filtre Passe-Bas) : Réponse impulsionnelle pour la plage de fréquences basses.
- Medium-Bas, Medium, Medium-Haut (Filtres Passe-Bande) : Réponses impulsionnelles pour chaque bande centrale.
- Aigu (Filtre Passe-Haut) : Réponse impulsionnelle pour la plage de fréquences hautes.

