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

