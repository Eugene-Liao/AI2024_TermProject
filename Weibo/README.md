# BERT-based model for Weibo Dataset
BERT is fine-tuned for fake account detection based on [this shared dataset](https://www.kaggle.com/datasets/bitandatom/social-network-fake-account-dataset
).

## Data Formats
- fake_account.csv: userindex \t post_content \n
- legitimate_account.csv: userindex \t postdate \t retweet_count \t comment_count \t like_count \t post_content \n

## Usage
- `$python3 train_eval.py` for evaluation after each epoch of training
- `$python3 evaluation.py` for evaluation on a specific checkpoint

## Affilicated files
- `utils.py`: data pre-processing, `train()` and `evaluate()`
- `models.py`: model class
- `Data.py`: modified Dataset class, Sampler and custom_collate()
