+++
authors = ["Spyros Rigas", "Paraskevi Tzouveli", "Stefanos Kollias"]
title = "An End-to-End Deep Learning Framework for Fault Detection in Marine Machinery"
date = "2024-08-16"
math = true
description = "An End-to-End Deep Learning Framework for Fault Detection in Marine Machinery"
+++


In this open-access paper, which can be found [here](https://www.mdpi.com/1424-8220/24/16/5310), we presented an end-to-end solution designed for Predictive Maintenance (PdM) of shipboard machinery. The framework covers the entire lifecycle from data collection at the edge to cloud processing and fault detection using a MTAD-GAT deep learning model. Below are brief summaries of its main constituents:

#### 1. Data Collection and Edge Computing
Sensor data from shipboard machinery are collected via the MQTT protocol and processed & compressed at the edge to reduce transmission overhead. By combining MQTT with solutions like Apache Kafka or Telegraf, the framework ensures reliable data streaming even in challenging marine environments with intermittent connectivity.

#### 2. Cloud Pipeline
The cloud infrastructure utilizes a lakehouse architecture with Apache Spark and Delta Lake for scalable, cost-efficient processing. Both batch and streaming data operations are supported, allowing continuous data ingestion and transformation, preparing the data for (near)-real-time analysis.

#### 3. Deep Learning Architecture
A deep learning model based on Graph Attention Networks (GATs) is employed to detect faults from the multivariate time-series data collected from the data acquisition devices. The model captures both spatial (inter-feature) and temporal relationships, providing explainable fault detection, for instance by highlighting the contribution of each feature to the model's prediction. It is trained in an unsupervised manner, making it effective for environments with minimal labeled data. The binary classification of points or segments as faulty or not is based on a scoring function and thresholding mechanism.

#### 4. Evaluation and MLOps
The framework is evaluated using a novel metric that balances fault detection accuracy with response time:

$$
\mathcal{F} = \frac{1}{\lambda_1 + \lambda_2 + \lambda_4} \cdot \max\left(0, \lambda_1F_1 + \lambda_2F_1^* - \lambda_3|F_1 - F_1^*| + \frac{\lambda_4}{N_E}\sum_{i=1}^{N_E}{\frac{1}{1+\theta_id_i}} - \lambda_5\frac{N_\text{und}}{N_E} \right),
$$

where $F_1$ is the model’s regular F1-Score, $F_1^*$ is the corresponding point-adjusted (PA) F1-Score obtained using the PA%K-L protocol, $N_E$ is the number of events in the time series, $N_\text{und}$ is the number of undetected events, and $d_i$ is the model’s delay in identifying the i-th event. Additionally, $\lambda_1, \dots, \lambda_5 \geq 0$ are tunable hyperparameters that regulate the contribution of each term to the overall score, and $\theta_i \geq 0$ are event-dependent factors that quantify the importance of the i-th event’s identification delay.
 
The results on three PdM-related datasets show high accuracy in detecting faults early. Additionally, the framework integrates MLflow to handle the lifecycle management of the models (model tracking, retraining, automated evaluation, deployment, etc.). 

{{< highlight html >}}
@article{s24165310,
	author = {Rigas, Spyros and Tzouveli, Paraskevi and Kollias, Stefanos},
	title = {An End-to-End Deep Learning Framework for Fault Detection in Marine Machinery},
	journal = {Sensors},
	volume = {24},
	year = {2024},
	number = {16},
	article-number = {5310},
	doi = {10.3390/s24165310}
}
{{< /highlight >}}