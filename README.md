# OTC Wallet Analysis on Tron Blockchain

## Description
This project analyzes high-volume USDT (TRC20) transactions on the Tron blockchain with low transaction counts to identify suspicious over-the-counter (OTC) activity, with a focus on the Mexico region. The goal is to detect potential OTC providers and uncover patterns that may indicate anti-money laundering (AML) risks. By generating cleaned and enhanced datasets, visualizations, and network analysis, this project provides actionable insights for crypto compliance and fraud detection.

This analysis is designed for crypto data analysts and AML specialists, such as those at Chainlabs, who are focused on leveraging blockchain data to enhance compliance practices and mitigate financial crime risks.

## Features
- Identifies wallets with high USDT (TRC20) transaction volumes but low transaction counts, indicative of suspicious OTC behavior.
- Detects patterns in transaction flows to uncover potential OTC providers.
- Maps relationships between wallet entities using network analysis to highlight suspicious connections.
- Produces cleaned and enhanced datasets with computed metrics (e.g., transaction volume, frequency, and entity linkages).
- Includes visualizations (e.g., transaction networks, volume distributions) for intuitive insights.
- Focuses on the Mexico region to align with regional AML priorities.

## Tools and Technologies
- **Dune Analytics**: Custom query to generate the initial dataset (`possible_otc_wallets.csv`) of Tron USDT transactions.
- **Python**: Core language for data wrangling, analysis, and visualization.
  - **Libraries**:
    - `pandas`: Data manipulation and cleaning.
    - `matplotlib` and `seaborn`: Visualizations of transaction patterns and metrics.
    - `numpy`: Numerical computations for metrics.
    - `networkx`: Network analysis to map wallet relationships.
    - `base58`: Handling Tron address encoding/decoding.
- **Jupyter Notebook**: Interactive analysis environment (`OTC_wallets_addresses_analysis.ipynb`).
- **VSCode**: Integrated development environment for coding and version control.
- **Git/GitHub**: Version control and project hosting.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/tripl3tr3s/otc_wallet_analysis.git
   cd otc_wallet_analysis

- Set up a virtual environment:

```bash
python -m venv venv
source vevn/bin/activate 
```

- Install dependencies:
```bash
pip install -r requirements.txt
```

- Obtain the dataset: 
    - The original dataset [possible_OTC_wallets.csv](https://dune.com/queries/5241136/8613964/) is generated via a custom Dune query. Access requieres a Dune Analytics account. 

    - Place the dataset in teh project root or update file paths in teh notebook as needed. 

# Usage 

- Open `OTC_wallets_addresses_analysis.ipynb`in VSCode or Jupyter Notebook. 
- Run the notebook cells to:
    - Load and clean the raw dataset [possible_OTC_wallets.csv](https://dune.com/queries/5241136/8613964/).
    - Generate enhanced datasets:
        - `possible_OTC_wallets_cleaned_v1.csv`: Cleaned version of the raw data.
        - `possible_OTC_wallets_with_tron_addresses.csv`: Includes decoded Tron Addresses. 
        - `possible_OTC_wallets_analyzed.csv`: Final dataset with computed metrics and network analysis results. 
    - Produce visualizations 
    - Identify suspicious OTC patterns and entity linkages. 
- Review outputs in the notebook or exported CSV files for further analysis. 

# Data Sources

- **Dune Analytics**: Custom query to extract TRX(Tron) transaction data, stored in `possible_OTC_wallets.csv`. The query filters for high-volume, low-count transactions aimed to the Mexico region. 

# Contributing 
Contributors are welcome to enhance the analysis or extend its scope. 

# License 

MIT Licence 

# Contact

For questions or collaboration, reach out to tripl3tr3s on GitHub. 