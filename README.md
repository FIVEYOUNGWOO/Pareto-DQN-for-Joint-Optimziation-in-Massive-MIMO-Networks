# PQN-for-Joint-Optimization-in-Massive-MIMO-Networks
* We achieve joint optimization of spectral efficiency (SE) and energy efficiency (EE) in Massive MIMO networks by approximating the Pareto Front in a 2D space with multiple objectives, using a replay buffer and DQN model.

# Introduction
* Reinforcement learning (RL) is a powerful tool for optimization and decision-making, aiming to maximize rewards as an alternative to human decision-making. However, RL has limitations in real-world problems where multiple objectives or dynamic environments with shifting priorities exist. In these contexts, adaptive decision-making performance may degrade. To address this, we designed a **multi-objective RL algorithm** focused on jointly optimizing SE and EE, which are critical objectives in 5G networks.

# Massive MIMO Network Environments
* The code for the virtual environment is available for use and modification in my repository [Massive-MIMO-PY](https://github.com/FIVEYOUNGWOO/Open-AI-GYM-Based-Massive-MIMO-Network-Environments).
* Our environment is based on [Emil Bjornson, Jakob Hoydis, and Luca Sanguinetti (2017), 'Massive MIMO Networks: Spectral, Energy, and Hardware Efficiency', Foundations and Trends in Signal Processing: Vol. 11, No. 3-4, pp. 154-655. DOI: 10.1561/2000000093.](https://www.massivemimobook.com/).

# Pareto Front Apprixmation Deep Q-Network (PQN)
* **Pareto Front Approximation** : PQN approximates a Pareto front for multiple conflicting objectives, using reinforcement learning to balance SE and EE.

* **Replay Buffer for Multi-Objective Optimization** : PQN leverages a replay buffer to store and sample experiences, maintaining diverse solutions across SE and EE objectives. These experiences are replayed to enhance the network’s ability to optimize both objectives.

* **Deep Q-Learning Approach** : PQN employs a Deep Q-Network (DQN) to evaluate and optimize actions for each state, aiming to achieve a balance between the two objectives over time.

* **Adaptive Decision-Making in Dynamic Environments** : PQN is designed for adaptability in environments where priorities may shift between objectives, such as in Massive MIMO networks, where balancing SE and EE is critical.

# Experiemental results
* **Spectral Efficiency** : This plot shows the SE reward across episodes. The upward trend indicates that PQN effectively improves SE over time as it learns from interactions in the environment.

* **Energy Efficiency** : This plot represents the EE reward across episodes. Similar to SE, there is a clear upward trend, signifying that PQN is capable of consistently improving EE through training.

* **Trade-off** : This scatter plot visualizes the trade-off between SE and EE achieved by PQN. The diagonal distribution suggests that the network balances the two objectives, with improvements in one objective often correlating with improvements in the other.

<table>
  <tr>
    <td><img src="/README_images/spectral_efficiency.png" width="290" height="300"/></td>
    <td><img src="/README_images/energy_efficiency.png" width="290" height="300"/></td>
    <td><img src="/README_images/train_results.png" width="290" height="300"/></td>
  </tr>
</table>
