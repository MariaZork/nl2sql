# nl2sql
Natural Language to SQL query using ML

This project use Python 3.9.13. The following installation and run instructions will be for Mac OS.

[References](docs/references.md)

# Training Data 

Download the data

```
git clone https://github.com/salesforce/WikiSQL && tar xvjf WikiSQL/data.tar.bz2 -C WikiSQL
```

Preprocess data

```
python wikisql_gendata.py
```

# Run project in conda env

```
conda create --name env python=3.9 
```

```
conda activate env
```

```
which pip
```

```
pip install -r requirements.txt
```

**Note:** if you get the following error while run the above command

```
ERROR: Could not build wheels for tokenizers, which is required to install pyproject.toml-based projects
```

You need to install RUST 
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
PATH="~/.cargo/bin:${PATH}"
source ~/.zshrc
```

Or install from source
```
git clone https://github.com/huggingface/transformers
cd transformers
 pip install .
```

Run Training
```
cd nl2sql/
source run.sh
```

```
conda deactivate
```