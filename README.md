# Representational Similarity Analysis & Multimodal Fusion Toolbox (RSA & Fusion Toolbox)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Language**: [English](README.md) | [中文](README_ZH.md)

A powerful MATLAB toolbox for performing **Representational Similarity Analysis (RSA)** and **Multimodal Fusion Analysis** on Electroencephalography (EEG), Magnetoencephalography (MEG), and functional Magnetic Resonance Imaging (fMRI) data. This toolbox is designed to streamline the computational pipeline, providing cognitive neuroscientists with an all-in-one solution for RSA and data fusion.

> **Core Features**:
> *   **End-to-End RSA Pipeline**: Supports the complete workflow from calculating Representational Dissimilarity Matrices (RDMs) to performing RSA.
> *   **Multimodal Data Support**: Seamlessly handles both E/MEG (high temporal resolution) and fMRI (high spatial resolution) data.
> *   **Cross-Modal Fusion**: Integrates E/MEG and fMRI data to explore unified neural representations across spatiotemporal dimensions.
> *   **User-Friendly GUI**: Offers a graphical interface to perform complex analyses without programming.
> *   **xjview Integration**: One-click visualization of results using the widely adopted xjview tool.

## 📦 Installation

1.  **Prerequisite**: Ensure [MATLAB](https://www.mathworks.com/products/matlab.html) (recommended R2018a or later) is installed on your computer.
2.  **Install the Toolbox**:
    *   Download all files of this toolbox to a local folder, e.g., `RSAandFusion_toolbox`.
    *   Navigate to this folder in the MATLAB Command Window.
    *   In the MATLAB **Home** tab, click **Set Path**.
    *   Select **Add with Subfolders**.
    *   Find and select the `RSAandFusion_toolbox` folder.
    *   Click **Save**, then **Close**.

## 🚀 Quick Start

After installation, type `RSA_Fusion_Toolbox` in the MATLAB Command Window to launch the main GUI. Follow these steps:

### 1. Calculate E/MEG RDM
*   **Purpose**: Computes Representational Dissimilarity Matrices for E/MEG data using MVPA based on a linear SVM classifier.
*   **Steps**:
    1.  Click "Calculate E/MEG RDM".
    2.  Import your `E/MEG data`, `trials label`, and `time file`.
    3.  Click "Calculate". Results are automatically saved in the `EMEG_RDMresults` folder.

### 2. Perform E/MEG RSA
*   **Purpose**: Conducts time-resolved Representational Similarity Analysis for E/MEG.
*   **Steps**:
    1.  Click "Calculate E/MEG RSA".
    2.  Import the neural RDM from the previous step (`xxx_RDM.mat`) and your theoretical model RDM.
    3.  Import the time file and click "Calculate". Results are saved in the `MEG_RSA_results` folder.

### 3. Perform fMRI RSA
*   **Purpose**: Performs whole-brain, searchlight-based Representational Similarity Analysis for fMRI data.
*   **Steps**:
    1.  Click "Calculate fMRI RSA".
    2.  Import the fMRI data folder (must contain `GLMforRSA.nii`), label name file, and label tag file.
    3.  Define the searchlight sphere size (voxel number).
    4.  Click "Calculate". Results are saved in the `fMRI_RSA_results` folder.

### 4. Perform E/MEG-fMRI Fusion
*   **Purpose**: Performs fusion analysis between E/MEG and fMRI data based on time points.
*   **Steps**:
    1.  Click "Fusion".
    2.  Import the E/MEG RDM, fMRI data folder, label name file, and label tag file.
    3.  Define the searchlight sphere size (voxel number).
    4.  Click "Calculate". Results are saved in the `fusion_results` folder.

### 5. View Results
*   Click "View results @ xjview" to directly launch the xjview tool for visualizing the generated `.nii` result files.

## 📁 Input File Format Specification

*   **E/MEG Data**: Toolbox-specific `.mat` format.
*   **Trial Labels**: A vector or cell array indicating the condition for each trial, saved as `.mat`.
*   **Time File**: Defines the time points for E/MEG analysis, saved as `.mat`.
*   **Theoretical RDM**: An `N x N` representational dissimilarity matrix, saved as `.mat`.
*   **fMRI Data**: NIfTI format images for RSA or fusion analysis, must be named `GLMforRSA.nii`.

## 🤝 Contributing

We welcome and appreciate contributions! If you have any questions, suggestions, or bug reports, please feel free to contact us via email.

## 📜 Citation

If you use this toolbox in your research, please cite:

Ruidi Wang. (2024). *Representational Similarity Analysis & Multimodal Fusion Toolbox (RSA & Fusion Toolbox)* (Version X.X) [Computer software]. Institute of Psychology, Chinese Academy of Sciences.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
