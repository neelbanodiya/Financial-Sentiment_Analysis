# Project Title

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/your_username/your_repository.svg)](https://github.com/your_username/your_repository/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/your_username/your_repository.svg)](https://github.com/your_username/your_repository/network)
[![GitHub issues](https://img.shields.io/github/issues/your_username/your_repository.svg)](https://github.com/your_username/your_repository/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/your_username/your_repository.svg)](https://github.com/your_username/your_repository/pulls)

Sentiment Analysis of financial data.

## Table of Contents

- [About](#about)
- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Documentation](#documentation)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## About

Fine-tuined the pretrained model that was trained on the financial data. Used your custom dataset to feed the model and do sentiment analysis  using pytorch

## Model

- This model is a distilled version of the RoBERTa-base model. It follows the same training procedure as DistilBERT. The code for the distillation process can be found here. This model is case-sensitive: it makes a difference between English and English.

The model has 6 layers, 768 dimension and 12 heads, totalizing 82M parameters (compared to 125M parameters for RoBERTa-base). On average DistilRoBERTa is twice as fast as Roberta-base.

Training Data Polar sentiment dataset of sentences from financial news. The dataset consists of 4840 sentences from English language financial news categorised by sentiment. The dataset is divided by agreement rate of 5-8 annotators.

Training procedure Training hyperparameters The following hyperparameters were used during training:

-learning_rate: 2e-05 
-train_batch_size: 8 
-eval_batch_size: 8 
-seed: 42 optimizer: 
-Adam with betas=(0.9,0.999) and epsilon=1e-08 lr_scheduler_type: linear num_epochs: 5


