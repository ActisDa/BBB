# BBB Permeability Prediction
Predicting blood-brain barrier (BBB) permeability based on molecular descriptors computed from SMILES strings.

This repository contains a Jupyter Notebook for predicting blood-brain barrier (BBB) permeability based on molecular descriptors computed from SMILES strings.


## Project Overview

The goal of this project is to build a classification model to predict whether a compound can cross the blood-brain barrier (BBB+) or not (BBB–), using physicochemical and topological molecular descriptors. The Dataset used in this project was obtained from https://deepchemdata.s3-us-west-1.amazonaws.com/datasets/BBBP.csv


##  Descriptors Used

Descriptors are calculated using the `mordred` library and include:

- Molecular weight
- Topological Polar Surface Area (TPSA)
- SLogP (logP)
- H-bond donors and acceptors
- Atom counts (total, C, N, O)
- Ring counts (aromatic/non-aromatic, heteroaromatic)
- Polarizability
- Rotatable bonds ratio
- Molecular radius
- Topological shape index
- Topological charge
- Zagreb index

These features are derived from the SMILES representation of each molecule.


## Modeling

The dataset is split into training and test sets using stratified sampling to preserve class balance (75% BBB+, 25% BBB–). A classification model is trained and evaluated to assess predictive performance.
