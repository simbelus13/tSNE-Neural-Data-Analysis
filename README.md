# t-SNE Synthetic Neural Data Analysis

## Overview
This project explores the use of **t-SNE** (t-Distributed Stochastic Neighbor Embedding) to analyze and visualize **synthetic neural data**. The focus is on:
- Generating synthetic neural activity data.
- Experimenting with t-SNE parameters like **perplexity**, **learning rate**, and **distance metrics**.
- Visualizing the impact of these parameters on data clustering.

## Key Features
- **Synthetic Neural Data**:
  - Simulated 50-neuron activity over 1000 time steps.
  - Added structured patterns (e.g., sinusoidal and exponential) to mimic real-world neural states.
- **t-SNE Experiments**:
  - **Perplexity**: Experimented with different values (5, 30, 50) to see how local vs. global relationships are captured.
  - **Learning Rate**: Tested a range of values (10, 50, 200, 500, 750, 1000) to observe its effect on cluster stability.
  - **Metrics**: Compared Euclidean, Manhattan, and Cosine metrics to explore the impact on clustering behavior.
- **Cluster Analysis**:
  - Added labels to validate whether t-SNE correctly identified neural states and transitions.

## Results
- **Cluster Formation**:
  - Observed two large clusters corresponding to the dominant activity patterns (cosine and exponential).
- **Effect of t-SNE Parameters**:
  - **Perplexity**: Low values (5) focused on local patterns; high values (50) emphasized global trends.
  - **Learning Rate**: Medium values (200, 500) provided stable clusters, while high rates (750, 1000) distorted the data.
  - **Metrics**: Euclidean and Manhattan metrics preserved magnitude-based clusters; cosine metric collapsed the clusters due to pattern similarity.
