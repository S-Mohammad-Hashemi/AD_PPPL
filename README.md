# AD_PPPL
Detecting Unseen Anomalies in Network Systems by Leveraging Neural Networks

This repository contains the code to train a model on the CICIDS2017 dataset with the help of the Proportional Progressive Pseudo Labeling (PPPL) technique as described in our paper.
This code is developed using TensorFlow.

Before running the code for CICIDS2017, the dataset should be first extracted.
```
bash ./extract_packet_data.sh
```

For more details on how this dataset is created and preprocessed, please look at [this paper](https://arxiv.org/abs/2008.03677).

To do domain adaptation between any pair of the domains in this dataset, s_domain and t_domain variables should be set appropriately.


## Paper

**Abstract:**

Despite all the progress achieved in recent years in detecting anomalies in network systems, detecting unseen anomalies such as zero-day attacks still remained a challenging task. Traditional signature-based Network Intrusion Detection Systems (NIDS) cannot detect such anomalies as there exists no known signature for them. Moreover, Machine Learning-based (ML-based) NIDS trained with a vanilla supervised learning method cannot detect them as they come from a different distribution compared to what the model has been trained on. Domain adaptation techniques help transfer the knowledge gained from a labeled source domain to an unlabeled target domain. Such techniques have the potential to make a model trained on a dataset containing a few network attacks to detect new types of anomalies that might happen in the future. However, recent domain adaptation methods have been mostly designed for images and provide very limited benefits when applied to network traffic.
In this paper, we introduce Proportional Progressive Pseudo-Labeling (PPPL), an effective approach for building a more general domain adaptation technique that can be leveraged to detect unseen anomalies in network systems. At the beginning of the training phase, PPPL progressively reduces target domain classification error, by training the model directly with pseudo-labeled target domain samples, while excluding samples with pseudo-labels that are more likely to be wrong from the training set and postponing training on such samples. Our evaluation conducted on the CICIDS2017 dataset shows that PPPL can significantly outperform other baselines in detecting unseen anomalies with up to 58\% improvement based on the average F1 score.
