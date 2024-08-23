
# Deep Q-Learning Trading Bot

## Overview

This repository contains a trading bot that leverages deep Q-learning to optimize trading strategies and maximize profits. The bot is designed to interact with financial markets, continuously learning from market data to improve its decision-making capabilities over time. The goal is to achieve a higher return on investment by adapting to market conditions using reinforcement learning.

## Features

- **Deep Q-Learning Algorithm**: The bot employs a deep Q-learning model to predict the best actions to take based on current market conditions.
- **Continuous Learning**: The model is trained and updated continuously to adapt to changing market dynamics.
- **Profit Optimization**: The bot's primary objective is to maximize profits by selecting optimal trading actions.
- **Customizable Parameters**: Various hyperparameters and configurations can be adjusted to tailor the bot's behaviour to specific trading scenarios.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/NeuroVortex/simple-deep-q-learning-trading-bot
   cd simple-deep-q-learning-trading-bot
   ```

2. **Install required packages**:
   Make sure you have Python 3.11+ installed. Then, install the necessary dependencies using pip:
   ```bash
   pip install -r requirements.txt
   ```

3. **Use offline Data**:
   The bot requires offline candlestick data of specific tickers as stored in a repository.

## Usage

1. **Training the Model**:
   Run the script to start training the model using historical market data:
   ```bash
   python train.py
   ```

2. **Running the Bot**:
   Once the model is trained, you can start the bot to begin trading:
   ```bash
   python run_bot.py
   ```

3. **Evaluating Performance**:
   After running the bot, you can evaluate its performance by reviewing the profit/loss logs generated in the `logs/` directory.

## Configuration

- **Learning Rate**: Adjust the learning rate in the `config.py` file to control how quickly the model adapts to new data.
- **Exploration vs. Exploitation**: Modify the epsilon-greedy strategy parameters to balance the exploration of new strategies versus the exploitation of known profitable ones.
- **Batch Size**: Set the batch size for training the model. Larger batches can lead to more stable learning but require more memory.
- **Replay Memory**: Configure the replay memory size, which stores past experiences to be replayed during training for more robust learning.

## Example

Here's a basic example of how the bot might be configured and run:

```python
from trading_bot import TradingBot

# Initialize the bot
bot = TradingBot(api_key='YOUR_API_KEY', secret_key='YOUR_SECRET_KEY')

# Train the model
bot.train(epochs=1000)

# Run the bot for live trading
bot.run(trade_duration='1d', risk_tolerance=0.05)
```

## Contributing

Contributions are welcome! If you have ideas for new features or improvements, please feel free to submit a pull request or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or questions, please contact Fatemeh Salboukh at [mkarbasioun@gmail.com].
