# Developing a Trading Client Using Double Dueling DQNs

I developed a trading client using Double Dueling Deep Q-Networks (DQN) to train an RL agent for intelligent stock trading decisions. The main steps included:

1. **Data Preprocessing:**
   - Used `ultracemos.csv` as the dataset.
   - Cleaned and normalized stock price data.
   - Engineered features such as moving averages, RSI, and Bollinger Bands.

2. **Model Architecture:**
   - Implemented a Double Dueling DQN.
   - Used two networks: `online` and `target` networks.
   - The dueling architecture separated value and advantage streams to improve stability.

3. **Training Strategy:**
   - Defined actions: buy, sell, and hold.
   - Implemented an epsilon-greedy policy for exploration.
   - Reward function based on portfolio value changes.
   - Experience replay and target network updates.

4. **Enhancements & Refinements:**
   - Added volatility indicators and sentiment analysis from news data.
   - Incorporated multiple time frame data to improve decision-making.
   - Refined reward function by penalizing unnecessary trades and incorporating a Sharpe ratio-based component.
   - Used adaptive epsilon decay and Noisy DQN for better exploration.
   - Increased training data diversity by augmenting `ultracemos.csv` with external market data.
   - Applied prioritized experience replay for better learning efficiency.

### Results & Learnings:
- The model showed **better stability** and **reduced overfitting**.
- Performance in simulated market conditions improved, but **real-world testing remains a challenge**.
- Future work includes fine-tuning hyperparameters and exploring multi-agent reinforcement learning.

---
This project has been an insightful experience in reinforcement learning for financial applications. By iterating and refining the approach, I gained a deeper understanding of **Dueling DQNs, reward shaping, and feature engineering in trading environments**.

