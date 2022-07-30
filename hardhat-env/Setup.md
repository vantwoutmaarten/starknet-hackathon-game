# macOS Setup

Install system dependencies (more details [here](https://www.cairo-lang.org/docs/quickstart.html)).

Download [Miniconda](https://docs.conda.io/en/latest/miniconda.html#macos-installers).

```
# Install
sh ~/Downloads/Miniconda3-xxx.sh

# Update
conda update -n base -c defaults conda

# Open new shell and test that python is selected via miniconda
which python
```

Create and setup conda environment:

```
cd hardhat/

conda create --name starknet-dev-env python=3.8.11
conda activate starknet-dev-env
```

Setup the python venv:

```
brew install gmp

# macOS with M1
CFLAGS=-I`brew --prefix gmp`/include LDFLAGS=-L`brew --prefix gmp`/lib pip3 install ecdsa fastecdsa sympy

# Install Cairo, Devnet and OpenZepellin
pip install cairo-lang==0.8.0 starknet-devnet werkzeug==2.0.3 openzeppelin-cairo-contracts

# Or, upgrade the packages
pip install --upgrade cairo-lang starknet-devnet werkzeug openzeppelin-cairo-contracts
```

If you are on macOS and installing `cairo-lang` fails, use [this guide](https://mirror.xyz/clacla.eth/obrY1Y89LjH4xrc4C0GR5OLudLpJq5dKClSsTJBOVFg).

Install the Node.js dependencies:

```
# Install NVM to manage multiple versions of Node.js
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash

# Install the required version
nvm install

# Select the required version
nvm use

# Install the project Node's dependencies
yarn install
```
