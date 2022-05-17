# Ethereum_Blockchain_Wallet

The goal of this project is to create a Streamlit application, called Fintech Finder, that employers can use to find potential candidates for hire. The app displays the hourly rate for each candidate, and then the employer can pay the candidate of their choice via the Ethereum Blockchain. 

---

## Technologies

This project uses the standard Python 3.8 and requires the following libraries and/or dependencies:

- [Streamlit](https://streamlit.io/) - turns datascripts into a shareable web apps. 
- [dataclasses](https://docs.python.org/3/library/dataclasses.html) - a decorator that is used to add generated special methods to classes.
- [typing](https://docs.python.org/3/library/typing.html) - provides runtime support for type hints. 
- [Web3.py](https://web3py.readthedocs.io/en/stable/overview.html) - A Python library for connecting to and performing operations on Ethereum-based blockchains.
- [bip44](https://pypi.org/project/bip44/) - A Python implementation for deriving hierarchical deterministic wallets from a seed phrase based on the BIP-44 standard.
- [Ganache](https://trufflesuite.com/ganache/) - Quickly fire up a personal Ethereum blockchain which you can use to run tests, execute commands, and inspect state while controlling how the chain operates.
- [dotenv](https://pypi.org/project/python-dotenv/) - Python-dotenv reads key-value pairs from a .env file and can set them as environment variables.
- [requests](https://pypi.org/project/requests/) - Requests is a simple, yet elegant, HTTP library.

---

### Imports

Imports for fintech_finder.py file:
```
import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3
```

Imports for crypto_wallet.py file:
```
import os
import requests
from dotenv import load_dotenv
load_dotenv()
from bip44 import Wallet
from web3 import Account
from web3 import middleware
from web3.gas_strategies.time_based import medium_gas_price_strategy
```

---

#### Methods

1. Create crypto_wallet.py file that contains the Ethereum transaction functions (generate account, get balance, send transaction).
2. Create the fintech_finder.py. Import the functions from the crypto_wallet.py file. Add the menmonic from Ganache and then add the candidate information to streamlit, and add streamlit functionality that allows a customer to sign and execute a payment transaction.
3. Inspect the transaction by reviewing the validated transaction hash and reviewing the transaction in Ganache.

---

##### Launching the Streamlit App

1. Fork and clone the repository to your local machine.
2. Open Ganache and create a new Ethereum workspace. Copy the mnemonic and paste it into the sample.env file.
3. Rename the sample.env file to .env.
4. Copy the unique addresses from Ganache, excluding the first address, and paste them into the candidate_database in the fintech_finder.py file.
5. Open your terminal and navigate to the cloned repository. Activate your dev environment.
6. Launch the Streamlit app by typing the following into your terminal:
```
conda activate dev
streamlit run fintech_finder.py
```

---

###### Results