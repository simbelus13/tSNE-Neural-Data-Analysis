# t-SNE Synthetic Neural Data and EEG Data Analysis

## Overview
This project explores the use of t-SNE (t-Distributed Stochastic Neighbor Embedding) to analyze and visualize synthetic neural data and EEG recordings. It focuses on:

1. **Synthetic Neural Data Analysis**:
   - Generating synthetic neural activity data.
   - Experimenting with t-SNE parameters like perplexity, learning rate, and distance metrics.
   - Visualizing the impact of these parameters on data clustering.

2. **EEG Data Analysis**:
   - Analyzing EEG recordings during mental arithmetic tasks from real-world subjects.
   - Exploring the biological relevance of clusters in the context of brain regions and channels.
   - Investigating high-variance channels across clusters to identify significant neural activity.

---

## Key Features

### Synthetic Neural Data:
- Simulated 50-neuron activity over 1000 time steps.
- Added structured patterns (e.g., sinusoidal and exponential) to mimic real-world neural states.

### t-SNE Experiments:
- **Perplexity**: Experimented with values (5, 30, 50) to see how local vs. global relationships are captured.
- **Learning Rate**: Tested values (10, 50, 200, 500, 750, 1000) to observe its effect on cluster stability.
- **Metrics**: Compared Euclidean, Manhattan, and Cosine metrics to explore the impact on clustering behavior.

### EEG Data Analysis:
- **Dataset**: EEG recordings from 36 subjects performing mental arithmetic tasks (refer to the dataset section below).
- **Clustering**: Applied K-Means clustering to t-SNE-transformed data to uncover dominant patterns.
- **Channel Variance**: Identified high-variance EEG channels within each cluster.
- **Biological Relevance**: Linked high-variance channels to specific brain regions (e.g., frontal cortex, occipital cortex) based on the International 10/20 electrode placement scheme.

---

## Results

### Synthetic Neural Data:
- **Cluster Formation**: Observed two large clusters corresponding to dominant activity patterns (cosine and exponential).
- **Effect of t-SNE Parameters**:
  - Perplexity: Low values (5) focused on local patterns; high values (50) emphasized global trends.
  - Learning Rate: Medium values (200, 500) provided stable clusters; high rates (750, 1000) distorted the data.
  - Metrics: Euclidean and Manhattan metrics preserved magnitude-based clusters; cosine metric collapsed the clusters due to pattern similarity.

### EEG Data:
- **Cluster Analysis**: Discovered five distinct clusters, each associated with high-variance channels.
- **High-Variance Channels**:
  - Cluster 0: Channel_16 (Occipital Cortex)
  - Cluster 1: Channel_6 (Frontal Cortex)
  - Cluster 2: Channel_5 (Frontal Cortex)
  - Cluster 3: Channel_2 (Prefrontal Cortex)
  - Cluster 4: Channel_5 (Frontal Cortex)
- **Brain Region Distribution**:
  - Frontal Cortex dominated with three clusters, highlighting its significance during mental arithmetic tasks.
  - Occipital Cortex and Prefrontal Cortex showed distinct activity patterns in one cluster each.

---

## Dataset Reference
The EEG dataset used in this analysis is sourced from the following publication and repository:

- **Dataset Source**: [MDPI Data Resource](https://www.mdpi.com/2306-5729/4/1/14)
- **Original Publication**: Goldberger, A., et al. *PhysioBank, PhysioToolkit, and PhysioNet: Components of a new research resource for complex physiologic signals*. Circulation [Online]. 101 (23), pp. e215–e220 (2000).

The dataset contains 36 CSV files representing EEG recordings for individual subjects across 19 channels during 60-second artifact-free sessions.
