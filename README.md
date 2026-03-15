# Anomaly-detection-using-dual-autoencoders-with-help-of-DBSCAN-unsupervised-technique.ipynb
A robust system for identifying sensor faults and ecological events by employing a dual-autoencoder architecture: the first autoencoder uses wavelet transforms for signal reconstruction to detect transient spikes, while the second operates in the feature domain to identify systematic drift, with consensus scoring for high-fidelity anomaly alerts.


OBJECTIVE OF THE INVENTION (Provide minimum two)
1. Design dual autoencoder architecture that purpose is to detect anomalies environment sensor data, anomalies types involves both transient (sudden spikes) and systematic (slow deviation).
2. Precise and robust anomaly identification by combining deep learning with wavelet-based signal reconstruction.
3. Design model for scalable deployment of massive, diverse crowdsourced environmental sensor network.
4. Inherit consensus scoring between the autoencoders, which lead to improvement in detection accuracy and decrease false positive(alarms).


PROBLEM ADDRESSED BY THE INVENTION:  
Environmental interference, calibration drift, and sensor malfunctions cause data quality degradation in current environmental sensor networks. While supervised models require labelled defect data, which are infrequently available, manual validation is unfeasible at scale. This innovation provides autonomous anomaly detection in dynamic, dispersed sensing systems by doing away with the need for manual calibration and labelled datasets.


To use this project, a sample sythetic dataset is provide replace the cvs file withe the provide sample dataset inoredr to test the project


#Interactive webpage is also provide for better visualization and for better management of data understanding
How to use it:

1.Drop or upload your iot_telemetry_data.csv
2.Select which sensor columns to analyze (auto-detects temp, humidity, co, lpg, smoke)
3.Tune the parameters (window size, step, DBSCAN eps/min_samples, anomaly percentile)
4.Hit ⚡ RUN DETECTION

What it does (web based visual representation of notebook):

Sliding windows — same 128/64 logic as notebook (can be update according to need of dataset)
Wavelet Autoencoder — Haar-like decomposition + reconstruction error per channel
Statistical Autoencoder — mean-structure bottleneck, simulates as per jupyter notebook linear AE
DBSCAN — noise points (label = -1) flagged as anomalies, same as notebook scatter plot
Threshold — combined error above the Nth percentile also flags anomalies

#As it is difficult for model and interface to handle large datset a small, synthetic datset (iot_telemetry_data_1000_rows.csv) is given for the demo purpose in order to try and run the interface for understanding of working and output.
