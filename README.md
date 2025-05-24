# 🧠 Connect4 with PPO (Proximal Policy Optimization)
This project implements a Proximal Policy Optimization (PPO) reinforcement learning agent to play the game Connect4. PPO is a reliable and efficient algorithm that enables stable policy learning through a clipped surrogate objective.

---
## 📁 Project Structure
 - **FinalProject_ppo.ipynb:** Interactive report showing training progress and model 
   insights.

 - **PPO_Summary_Report.pdf:** Summary report describing model architecture, training 
   process, and evaluation.

---
## 🏗 Model Architecture
The PPO model consists of:

 - **Input Layer:** Accepts Connect4 board state as a tensor of shape (1, 1, 6, 7).

 - **Convolutional Layers:**
    - **Conv1:** 32 filters, 3x3 kernel, ReLU
    - **Conv2:** 64 filters, 3x3 kernel, ReLU
    - **Shared Fully Connected Layer:** 128 units, ReLU

 - **Heads:**
   - **Policy Head:** Predicts probabilities over 7 actions.
   - **Value Head:** Predicts the value of a given state.
---
## ⚙️ Training Process
  1. **Environment Interaction:**
     Agent collects trajectories (state, action, reward, next state, done).

  2. **Policy Optimization:**
     Uses a clipped objective function to ensure safe updates.

  3. **Advantage Estimation:**
     Estimates advantages using value function and rewards.

  4. **Value Network Update:**
     Minimizes mean squared error between predicted and actual returns.
---
## 🔧 Key Hyperparameters
    - Parameter	Value
    - Learning Rate	1e-4
    - Discount Factor γ	0.99
    - Clipping ε	0.2
    - Batch Size	64
    - Epochs per Update	4
---
## 📊 Evaluation Metrics
   1. **Cumulative Reward:** Learning curve across episodes.
   2. **Win Rate:** Against random opponents.
   3. **Policy Improvement:** Quality of action selection.

The PPO agent showed consistent learning performance and increasing win rates.

---
## 📈 Results
View the full visualization and training progress:

Open FinalProject_ppo.ipynb in your browser.

---
## 📝 Conclusion
This project demonstrates PPO's ability to learn effective strategies for Connect4 using a stable and efficient reinforcement learning process. 

**Future improvements may include:**
  - Reward shaping
  - Curriculum learning
  - Testing against stronger opponents

