
# Dynamic Pricing for Urban Parking Lots

This project implements a dynamic pricing model for urban parking lots using real-time data. The goal is to optimize occupancy and pricing through intelligent decision-making based on features such as traffic conditions, queue lengths, special events, and time of day.

## Project Overview

Urban parking lots suffer from inefficiencies in occupancy and pricing. Fixed-rate systems fail to adapt to real-time demand, resulting in congestion or underutilization.

We propose three dynamic pricing models that adjust parking rates based on contextual features to maintain optimal occupancy:

- **Model 1**: Rule-based pricing
- **Model 2**: Queue-aware pricing using threshold-based classification
- **Model 3**: ML-enhanced pricing using real-time traffic and hourly data

Each model is visualized using interactive Bokeh plots for comparison.

## Features

- Real-time price level adjustment (Low, Medium, High)
- Models trained on:
  - Occupancy levels
  - Traffic condition
  - Queue length
  - Event day (special day flag)
  - Hour of the day
- Interactive time-series visualizations using **Bokeh**

## 🛠️ Tech Stack

| Layer        | Tools / Frameworks                      |
|--------------|------------------------------------------|
| Programming  | Python 3                                 |
| Data Handling| pandas, NumPy                            |
| Visualization| Bokeh                                    |
| ML/Rules     | Custom Python logic |

## Architecture Flow
Raw Data (CSV).
The data goes through Preprocessing to clean and structure it.
Feature Engineering is applied to extract and create relevant features.
Based on logic or input, a Model is Selected:

Model 1: Rule-Based Price Logic

Model 2: Queue-Aware Logic

Model 3: Traffic + ML-Based Logic

Each model outputs a CSV file with a new column indicating the Price Level.
The final output is visualized using Interactive Bokeh Plots.

## 📊 Output Columns in Processed Data

- `SystemCodeNumber`
- `Occupancy`
- `Capacity`
- `QueueLength`
- `TrafficConditionNearby`
- `IsSpecialDay`
- `Hour`
- `rate` (Predicted price)
- `PriceLevel_Model1`, `PriceLevel_Model2`, `PriceLevel_Model3`
- `Timestamp`

## 📈 Visualizations

Each model has its own interactive plot showing **occupancy over time**, colored by **Price Level**:

- Line plots for time-series trend
- Hover tooltips for detailed inspection

