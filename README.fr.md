# 3DModelConverter
🇫🇷 English version: [README.md](README.md)

3DModelConverter permet de convertir des fichiers de nuages de points aux formats PTS, E57 ou LAS vers le format OCTI.
Ce format est nécessaire pour visualiser des nuages de points dans le logiciel [ESILab](https://github.com/PerceptionRobotique/ESILab).

## ⚙️ Installation Windows

1. Télécharger [`3DModelConverter_Setup.exe`](https://github.com/PerceptionRobotique/3DModelConverter/releases/download/latest/3DModelConverter_Setup.exe)
2. Lancer l’installateur depuis le dossier Téléchargements  
   - Si un avertissement de sécurité Windows apparaît, cliquer sur **“Plus d’informations”**, puis **“Exécuter quand même”**
3. Suivre l’assistant d’installation


## 🚀 Utilisation

1. Cliquer sur **Ouvrir un fichier** et sélectionner un fichier PTS (Point Cloud Text)
2. Cliquer sur **Enregistrer sous** et choisir le dossier de sortie pour les fichiers OCTI et TXT
3. Cliquer sur **Convertir** pour lancer la conversion

## 📄 Format recommandé des fichiers PTS

Pour garantir des performances optimales, les fichiers PTS doivent respecter le format suivant :

- Format texte ASCII  
- Une ligne par point : `X Y Z Intensity R G B`  
- L’intensité doit être un entier compris entre **-2000 et 2000** pour une bonne visualisation dans ESILab

Télécharger des exemples de [`fichiers PTS`](https://extra.u-picardie.fr/nextcloud/index.php/s/mJbjbPCqEjPc9k7)

## 📄 Format recommandé des fichiers E57
Les champs minimums requis dans un fichier E57 sont :

- cartesianX
- cartesianY
- cartesianZ

Les champs optionnels suivants sont également pris en charge :

- intensity
- colorRed
- colorGreen
- colorBlue

Si les champs optionnels ne sont pas présents, le fichier OCTI sera tout de même généré. Les informations d'intensité et/ou de couleur seront alors remplacées par des valeurs par défaut.

Un fichier E57 peut contenir les données d'une ou de plusieurs stations de numérisation. Toutes les stations présentes dans le fichier sont importées puis fusionnées dans un unique nuage de points OCTI.

Pour chaque station, la transformation définie dans le fichier E57 (rotation et translation) est appliquée à l'ensemble des points avant la fusion des stations. Cela garantit que tous les scans sont exprimés dans le même système de coordonnées global.

## 📄 Format recommandé des fichiers LAS
Les champs minimums requis dans un fichier LAS sont :

- X
- Y
- Z

Les champs optionnels suivants sont également pris en charge :

- Intensity
- Red
- Green
- Blue

Les valeurs d'intensité stockées dans le fichier LAS (comprises entre 0 et 65535) sont automatiquement normalisées dans l'intervalle [-2000 ; 2000] afin d'assurer une visualisation optimale dans ESILab.

Si les champs optionnels ne sont pas présents, le fichier OCTI sera tout de même généré. Les informations d'intensité et/ou de couleur seront alors remplacées par des valeurs par défaut.


## ℹ️ À propos

3DModelConverter est développé par le **Laboratoire MIS (Modélisation, Information & Systèmes)**  
de l’**UPJV (Université de Picardie Jules Verne)**.

👉 https://www.mis.u-picardie.fr/

Cette application est un logiciel propriétaire.
Les composants tiers — Qt (LGPL v3), Boost et PCL — sont distribués sous leurs licences respectives.
Voir le fichier THIRD_PARTY_LICENSES.txt pour plus de détails.

## 🛠️ Support & maintenance

Pour toute demande de support technique, veuillez contacter :  
📧 esilab@u-picardie.fr

## 📦 Versions

👉 [Voir toutes les versions](https://github.com/PerceptionRobotique/3DModelConverter/releases)

## Bibliothèques tierces

Ce logiciel utilise les composants tiers suivants :

- Qt (LGPL v3)
- Boost (Boost Software License 1.0)
- PCL - Point Cloud Library (BSD 3-Clause)
- PDAL (BSD 3-Clause)
- libE57Format (Boost Software License 1.0)

Ces composants sont soumis à leurs propres licences.

Voir THIRD_PARTY_LICENSES.txt pour plus de détails.


### Conformité Qt

Cette application utilise Qt sous licence LGPL.

Les utilisateurs sont autorisés à remplacer ou modifier cette bibliothèque et à relier l’application en conséquence, conformément aux exigences de la LGPL.