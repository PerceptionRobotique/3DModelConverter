# 3DModelConverter
🇫🇷 English version: [README.md](README.md)

3DModelConverter permet de convertir des fichiers de nuages de points au format **PTS** vers le format **OCTI**.  
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

## ℹ️ À propos

3DModelConverter est développé par le **Laboratoire MIS (Modélisation, Information & Systèmes)**  
de l’**UPJV (Université de Picardie Jules Verne)**.

👉 https://www.mis.u-picardie.fr/

## 🛠️ Support & maintenance

Pour toute demande de support technique, veuillez contacter :  
📧 esilab@u-picardie.fr

## 📦 Versions

👉 [Voir toutes les versions](https://github.com/PerceptionRobotique/3DModelConverter/releases)