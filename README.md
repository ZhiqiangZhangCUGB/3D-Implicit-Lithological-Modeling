# 3D Implicit Lithological Modeling

A research-oriented repository for **3D implicit lithological modeling** using geophysical attributes, spatial neighborhood features, machine learning, and deep learning methods.

This project explores several modeling strategies for lithology prediction in 3D space, including:

- Random Forest with spatial neighborhood features
- Random Forest enhanced by multi-scale RBF spatial basis functions
- 3D CNN for voxel-based lithology classification
- Anisotropic 3D CNN for direction-sensitive geological feature extraction
- RBF-enhanced anisotropic 3D CNN for implicit lithological modeling

The notebooks are designed for experiments on 3D geological/geophysical data containing spatial coordinates, physical property features, and lithology labels.

---

## Repository Structure

```text
3D-Implicit-Lithological-Modeling/
├── RF.ipynb          # Random Forest with spatial neighborhood features
├── RBF_RF.ipynb     # RBF-enhanced Random Forest workflow
├── CNN.ipynb        # 3D CNN lithology classification workflow
├── ACNN.ipynb       # Anisotropic 3D CNN workflow
└── ACNN_RBF.ipynb   # RBF-enhanced anisotropic 3D CNN workflow

git clone https://github.com/ZhiqiangZhangCUGB/3D-Implicit-Lithological-Modeling.git
cd 3D-Implicit-Lithological-Modeling

## Data Description

This project uses 3D spatial geological and geophysical data for implicit lithological modeling. The data are organized in a tabular format, where each row represents a sampling point in 3D space. Each point contains spatial coordinates, geophysical attributes, and the corresponding lithology label.

### Data Fields

| Field | Type | Description |
|---|---|---|
| `X` | float | X coordinate of the sampling point in 3D space |
| `Y` | float | Y coordinate of the sampling point in 3D space |
| `Z` | float | Z coordinate of the sampling point, usually representing depth or elevation |
| `den` | float | Density attribute, representing the density-related geophysical feature |
| `sus` | float | Magnetic susceptibility attribute, representing the magnetic property of the sample |
| `res` | float | Resistivity attribute, representing the electrical property of the sample |
| `lithology` | int / str | Lithology class label, represented by either numeric codes or lithology names |

### Data Format Example

```text
X,Y,Z,den,sus,res,lithology
100.0,200.0,-50.0,2.65,0.012,150.3,0
105.0,200.0,-50.0,2.71,0.018,132.5,1
110.0,200.0,-50.0,2.58,0.009,180.7,2
Field Explanation
X, Y, and Z describe the 3D spatial location of each sampling point. They are the basic spatial information used for geological modeling and neighborhood feature extraction.
den, sus, and res are geophysical attributes. These fields can be replaced or extended according to the actual dataset, such as gravity anomaly, magnetic anomaly, seismic velocity, or electrical conductivity.
lithology is the target label used for supervised learning.
Lithology Label Description

Lithology classes can be encoded using numeric labels, for example:
| Label | Lithology Class   |
| ----- | ----------------- |
| `0`   | Lithology class 1 |
| `1`   | Lithology class 2 |
| `2`   | Lithology class 3 |
If the original dataset uses lithology names, such as granite, sandstone, or limestone, they should be converted into numeric labels before model training.

Data Requirements
The dataset must contain the spatial coordinate fields X, Y, and Z.
The dataset should contain one or more geophysical attribute fields.
The dataset used for supervised learning must contain a lithology label field.
Coordinate units should be consistent, for example, all coordinates should be measured in meters.
Geophysical attributes are recommended to be standardized or normalized before model training.
Missing values, outliers, and duplicated sampling points should be checked and processed before training.
Recommended Data File Format

It is recommended to store the data in .csv, .dat, or .txt format, for example:

data.csv
mapped_s1_data.dat
lithology_samples.txt
