# RansomGuard: Network Intrusion Detection (Deep Learning)

Autoencoder (trained on normal traffic only) + MLP classifier that also
uses the autoencoder's reconstruction error. Built with PyTorch, with a
Streamlit app for scanning uploaded traffic files.

Dataset: CIC-IDS2017 (not included; download from the Canadian Institute
for Cybersecurity). Train/test split is chronological: the first 70% of
each traffic type is used for training and the last 30% for testing.

## Results (held-out later traffic)
- Attacks caught: 96.6%
- False alarms: 1.39%
- Autoencoder alone: 36.8% caught, 0.61% false alarms

## Limits
- Works on known attack types; weak on unseen ones (PortScan, Bot in zero-day tests).
- Blocking is simulated, not real.
- Class-weight setting was chosen by looking at test results.

## How to run
Open the notebook in Google Colab and Run all (Sections 1-11).
