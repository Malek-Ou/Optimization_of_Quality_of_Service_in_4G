# 4G Quality of Service (QoS) Optimization

This project aims to analyze, model, and improve the Quality of Service (QoS) in 4G networks using **data processing, machine learning (ML), and reinforcement learning (RL)**.

---

## Project Structure


---

## Data Processing (`data_processing`)

The preprocessing pipeline includes:

- Cleaning the dataset and handling missing values.  
- Removing null or outlier data.  
- Feature engineering: creating new features from existing ones for more accurate insights.  
- Normalization of features using **MinMaxScaler** to scale values between 0 and 1.

### Feature Distributions

1. **RSRP (pcell)** – Reference Signal Received Power
   - Values mostly concentrated between 0.6 and 0.9.
   - Training and test sets cover a wide range and are consistent.

2. **RSRQ (pcell)** – Reference Signal Received Quality
   - Majority of values normalized between 0.6 and 1.0.
   - Indicates generally good signal quality.

3. **RLC downlink throughput**
   - Many values close to 0, with a few extending up to 1.0.
   - Indicates a skewed distribution with many low-throughput measurements.

**Observations:**
- Training and test distributions are consistent, which is favorable for learning.  
- MinMax normalization performed correctly.  
- High concentration around 0 for RLC throughput may indicate imbalanced data.


---

## Machine Learning (`ml_models`)

- **Clustering:** KMeans applied, identified 3 clusters in the data.  
- **Regression:** Linear Regression applied to features with non-normal distributions.  
- **Prediction:** XGBoost used for predicting QoS.

---

## Reinforcement Learning (`rl_models`)

- **Algorithm:** Deep Q-Network (DQN) used to dynamically improve QoS.  
- Contains training scripts, best models, and evaluation logs.  
- RL model learns optimal actions to maximize network performance metrics.

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/Malek-Ou/Optimization_of_Quality_of_Service_in_4G.git
