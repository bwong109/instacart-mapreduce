# Instacart Market Basket Analysis Using SON Algorithm
SON algorithm in Python for identifying frequent itemsets in Instacart data using simulated MapReduce; includes map and reduce stages

## Overview
This repository contains an implementation of the SON algorithm using a simulated MapReduce framework to discover frequent itemsets in large-scale transaction data, such as that from Instacart. The project aims to predict customer purchasing patterns by identifying items that frequently appear together in transactions.

## Problem Statement
The goal of this project is to implement the SON algorithm to learn association rules for predicting customer purchases on Instacart. The implementation requires two stages of map-reduce functions that process data to discover frequent itemsets and derive association rules from these itemsets. The project simulates the MapReduce architecture locally without the need for an actual distributed environment.

## Implementation Details
- **Map Step 1**: Processes chunks of data to identify local frequent itemsets based on a modified support threshold.
- **Reduce Step 1**: Combines all local frequent itemsets to filter out globally frequent itemsets.
- **Map Step 2**: Uses the frequent itemsets from the first reduce step as candidates and checks their occurrences in new data chunks.
- **Reduce Step 2**: Aggregates the counts from the second map step and finalizes the list of itemsets that meet the global support threshold.

The output of these functions is not directly in rule form but constitutes the frequent itemsets from which rules can be derived.

## Usage
To run these functions, you will need:
- Python environment with libraries such as Pandas, NumPy, itertools, and collections.
- A dataset formatted in a specific way (refer to the provided data structure in the script comments).

## Results
After processing, the script outputs frequent itemsets that surpass the specified support thresholds. These itemsets can then be used to derive association rules which predict the likelihood of items being purchased together.

This project provides a foundation for understanding customer behavior and enhancing strategies for product placement, inventory management, and personalized marketing.
