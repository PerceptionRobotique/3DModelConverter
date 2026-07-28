# 3DModelConverter
🇫🇷 Version française : [README.fr.md](README.fr.md)

3DModelConverter allows you to convert point cloud files in **PTS format** into **OCTI format**.  
This format is required for visualizing point clouds using the [ESILab](https://github.com/PerceptionRobotique/ESILab) software.

## ⚙️ Installation Windows

1. Download [`3DModelConverter_Setup.exe`](https://github.com/PerceptionRobotique/3DModelConverter/releases/download/latest/3DModelConverter_Setup.exe)
2. Run the installer from your Downloads folder  
   - If a Windows security warning appears, click **“More info”** then **“Run anyway”**
3. Follow the installation wizard

## 🚀 Usage

1. Click **Open file** and select a PTS file (Point Cloud Text)
2. Click **Save As** and choose the output folder for OCTI and TXT files
3. Click **Convert** to start the conversion

## 📄 Recommended PTS file format

To ensure optimal performance, PTS files must follow this format:

- ASCII text format  
- One point per line: `X Y Z Intensity R G B`  
- Intensity must be an integer between **-2000 and 2000** for correct visualization in ESILab

Download sample [`PTS files`](https://extra.u-picardie.fr/nextcloud/index.php/s/mJbjbPCqEjPc9k7)

## ℹ️ About

3DModelConverter is developed by the **MIS Laboratory (Modélisation, Information & Systèmes)**  
at **UPJV (University of Picardie Jules Verne)**.

👉 https://www.mis.u-picardie.fr/

This application is proprietary software.
Third-party components - Qt (LGPL v3), Boost and PCL - are licensed under their respective licenses.
See THIRD_PARTY_LICENSES.txt for details.

## 🛠️ Support

For any technical support requests, please contact:  
📧 esilab@u-picardie.fr

## 📦 Releases

👉 [See all versions](https://github.com/PerceptionRobotique/3DModelConverter/releases)


## Third-Party Libraries

This software uses the following third-party components:

- Qt (LGPL v3)
- Boost (Boost Software License 1.0)
- PCL - Point Cloud Library (BSD 3-Clause)
- PDAL (BSD 3-Clause)
- libE57Format (Boost Software License 1.0)

These components are subject to their own licenses.

See THIRD_PARTY_LICENSES.txt for full details.


### Qt compliance

This application uses Qt under the LGPL license.

Users are allowed to replace or modify these library and relink the application accordingly, as required by the LGPL.