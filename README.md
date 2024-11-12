# Interface d'Équaliseur Sonore

## Objectif du Projet

Ce projet consiste en la création d'une interface graphique en Python pour modifier des bandes sonores en appliquant des effets de filtrage. Dans le cadre de ce mini-projet, vous jouerez le rôle d'un ingénieur travaillant sur des techniques pour améliorer la qualité sonore des enregistrements. Plus spécifiquement, l'objectif est de créer un équaliseur capable de manipuler différentes bandes de fréquence d'un fichier audio en temps réel.

## Fonctionnalités

L'application d'équalisation inclut :
- **Sélection d'un fichier `.wav`** : Permet de sélectionner un fichier audio `.wav` pour appliquer des modifications.
- **Contrôle de fréquence par bandes** : Interface avec 5 bandes de fréquence contrôlables individuellement pour ajuster le gain.
- **Traitement et affichage** : Un bouton pour lancer le traitement et visualiser les gains appliqués dans la console.

Dans un premier temps, l'interface se limite à afficher les valeurs des sliders dans le terminal.

## Technologies et Bibliothèques

Le projet utilise les technologies et bibliothèques suivantes :
- **Python** pour la programmation générale et le traitement audio.
- **Qt pour Python** pour créer l'interface graphique.
- **NumPy et SciPy** pour le traitement du signal, notamment pour implémenter les filtres.
- **Matplotlib** pour les visualisations temporelles et fréquentielles.

## Structure du Projet

Le dépôt est organisé comme suit :
- `00-interfaceEqualizer.py` : Interface de base pour l'équaliseur.
- `01-generationSignaux_T_et_F.py` : Génération de signaux pour les visualisations temporelle et fréquentielle.
- `02-filtrageEx.py` : Exemple de filtrage.
- `LW_20M_amis.wav` : Fichier de test `.wav` pour valider le fonctionnement de l'équaliseur.

## Algorithmes

Les filtres de l'équaliseur sont implémentés pour diviser le signal en plusieurs bandes de fréquence, permettant d'amplifier ou de diminuer certaines gammes de fréquences. Voici les algorithmes principaux :

### 1. Filtrage par Bandes de Fréquences

L'équaliseur utilise cinq filtres en bande pour diviser le spectre sonore en bandes spécifiques. Chaque filtre peut être ajusté pour augmenter ou diminuer l'amplitude de sa bande de fréquence correspondante. Les bandes peuvent être définies comme suit :
- **Graves** (20 Hz - 200 Hz)
- **Basses moyennes** (200 Hz - 1000 Hz)
- **Moyennes** (1 kHz - 4 kHz)
- **Hautes moyennes** (4 kHz - 10 kHz)
- **Aigus** (10 kHz - 20 kHz)

### 2. Réponse Impulsionnelle des Filtres

Chaque filtre est conçu pour produire une réponse impulsionnelle qui dépend de ses paramètres de gain et de fréquence. La réponse impulsionnelle permet de visualiser comment chaque bande de fréquence est affectée par les réglages de gain.

### Coefficients des Filtres

Les coefficients des filtres sont calculés en fonction des fréquences de coupure de chaque bande. Nous utilisons des filtres numériques de type FIR ou IIR, en ajustant les paramètres de manière à obtenir la réponse en fréquence souhaitée.

## Instructions d'Installation et d'Exécution

1. **Installation des dépendances**  
   Clonez le dépôt GitHub, puis installez les bibliothèques nécessaires :
   ```bash
   git clone <URL-du-dépot>
   cd <nom-du-dossier>
   pip install -r requirements.txt
