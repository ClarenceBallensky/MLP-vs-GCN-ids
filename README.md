# MLP-vs-GCN-ids

https://colab.research.google.com/github/ClarenceBallensky/MLP-vs-GCN-ids/blob/main/MLP_vs_GCN_Intrustion_Detection.ipynb

## Dataset

This project uses the **improved CSE-CIC-IDS2018** dataset from Liu et al. (CNS 2022), which regenerates the flows from the original packet captures with a corrected CICFlowMeter and fixes labeling errors in the original release.

- **Source:** https://intrusion-detection.distrinet-research.be/CNS2022/Datasets/CSECICIDS2018_improved.zip
- **Sample used here:** the full dataset is ~9.8 GB (zipped), so the notebook downloads a pre-built sample (`ids_sample.parquet`, 300,001 rows × 91 columns) from this repo's [v1 release](https://github.com/ClarenceBallensky/MLP-vs-GCN-ids/releases/tag/v1). The notebook checks its SHA-256 hash so everyone trains on identical data.
- **How the sample was made:** rows with missing values were dropped, 10% of each daily CSV was sampled at random, and the combined result was sampled down to ~300k rows (seed 42).

### Citations
- L. Liu, G. Engelen, T. Lynar, D. Essam, W. Joosen. "Error Prevalence in NIDS datasets: A Case Study on CIC-IDS-2017 and CSE-CIC-IDS-2018." IEEE CNS, 2022. doi:10.1109/CNS56114.2022.9947235
- I. Sharafaldin, A. Habibi Lashkari, A. Ghorbani. "Toward Generating a New Intrusion Detection Dataset and Intrusion Traffic Characterization." ICISSP, 2018. (original CSE-CIC-IDS2018 / CIC-IDS2017 data)
