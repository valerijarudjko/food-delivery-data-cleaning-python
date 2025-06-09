# Install the Kaggle CLI

1. Open your VS Code integrated terminal and run:
```bash
pip install kaggle
```
This gives you access to the kaggle command-line tool

2. Get your Kaggle API credentials

- Sign in at https://www.kaggle.com, click your user icon → Account, then hit Create API Token.
- A file named kaggle.json will download.
  
- Move it into your home Kaggle folder:
##### Mac/Linux: ~/.kaggle/kaggle.json
##### Windows: C:\Users\<YourUser>\.kaggle\kaggle.json
- Secure it (on Unix):
```bash
chmod 600 ~/.kaggle/kaggle.json
```
##### This lets the CLI authenticate.

# Download & unzip the dataset
- In the terminal, run:
```bash
kaggle datasets download \
  -d sudarshan24byte/online-food-dataset \
  -p data/online-food \
  --unzip
```
-d specifies the dataset slug; -p sets the target directory; --unzip extracts the files in place

- Load the data in Python:
In your .py or Jupyter file, use pandas to read whichever CSV(s) you need.

- For example (adjust the filename to match what was unzipped):
```bash
df = pd.read_csv('data/online-food/restaurant.csv')
print(df.head())
```

- Or, if you prefer to script the download inside Python, you can use the Kaggle API client:
```python
from kaggle.api.kaggle_api_extended import KaggleApi
import pandas as pd

# 1. Authenticate
api = KaggleApi()
api.authenticate()

# 2. Download & unzip the dataset into "./data/online-food"
api.dataset_download_files(
    'sudarshan

```

## Create your environment
```bash
python3.11.1 -m venv my_env1    # <-- name of your environment
```

## Importing libraries:
```bash
pip install pandas
```
```python
import pandas as pd
```












#### Acknowledgments
- Data Source: Kaggle’sOnline Food Dataset
- Inspiration: @onurdatascience
