# SMSCI

# Overview
This repository contains the implementation of SMSCI: Simultaneous Modeling of Social and Contextual Interactions for Multi Pedestrian Trajectory Prediction.

We explore the limitations of prior methods reliant on pedestrian positions for modeling social interactions and scene influences. 
This research achieves a breakthrough in simultaneously predicting multiple pedestrian trajectories in a scene video by introducing the SMSCI model which uses Generative Adversarial Networks and sequence prediction. 
By integrating both historical paths and environmental context, SMSCI accounts for both social interactions and scene influences, outperforming previous approaches. 
Through experiments demonstrating enhanced accuracy and collision avoidance, the effectiveness of generating socially and physically valid trajectories is demonstrated. 

<img width="920" alt="SMSCI_arch" src="https://github.com/anonyme-anonymee/SMSCI/assets/159822306/67b7a872-958e-420a-ae3e-cd39152ce976">


# Prerequisites

To install all the dependency packages, please run:

pip install -r requirements.txt

# Data Preparation

1- We use ETH and UCY datasets. 
Please, run the following script to download the datasets:

```bash
bash scripts/download_data.sh
```

This will create the directory `datasets/<dataset_name>` with train/ val/ and test/ splits. All the datasets are pre-processed to be in world coordinates i.e. in meters. We support five datasets ETH, ZARA1, ZARA2, HOTEL and UNIV. 

We use leave-one-out approach, train on 4 sets and test on the remaining set. 
We observe the trajectory for 8 times steps (3.2 seconds) and show prediction results for 8 (3.2 seconds) and 12 (4.8 seconds) time steps.

2- Set the path for saving your trained models in the code.
3- Run the following jupyter to train and test the model

# Notes
The repository is still under construction. Please let me know if you encounter any issues.
Best, 
