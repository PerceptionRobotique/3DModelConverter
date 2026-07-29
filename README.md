# 3DModelConverter
🇫🇷 Version française : [README.fr.md](README.fr.md)

3DModelConverter allows you to convert point cloud files in PTS, or in E57, or in LAS format into OCTI format.
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

## 📄 Recommended E57 file format

The minimum required fields in an E57 file are:

- `cartesianX`
- `cartesianY`
- `cartesianZ`

The following optional fields are also supported:

- `intensity`
- `colorRed`
- `colorGreen`
- `colorBlue`

If the optional fields are not present, the generated OCTI file will still be created, but intensity and/or color information will still be created using the default values.

An E57 file may contain data from one or multiple scan stations. All scan stations present in the file will be imported and merged into a single OCTI point cloud. 

For each scan station, the transformation defined in the E57 file (including rotation and translation) is applied to all points before merging the stations. This ensures that all scans are expressed in the same global coordinate system.

## 📄 Recommended LAS file format

The minimum required fields in a LAS file are:

- `X`
- `Y`
- `Z`

The following optional fields are also supported:

- `Intensity`
- `Red`
- `Green`
- `Blue`

Intensity values stored in the LAS file (ranging from 0 to 65535) are automatically normalized to the interval **[-2000, 2000]** for optimal visualization in ESILab.

If the optional fields are not present, the generated OCTI file will still be created, but intensity and/or color information will still be created using the default values.

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