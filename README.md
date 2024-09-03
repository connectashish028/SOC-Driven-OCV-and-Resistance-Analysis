# SOC-Driven-OCV-and-Resistance-Analysis

# Battery Performance Analysis: KOKAM vs. LG Chem

This repository contains a Jupyter Notebook that performs a comprehensive analysis of battery performance metrics, focusing on Open Circuit Voltage (OCV), internal resistance, and power discharge across various States of Charge (SOC). The analysis is conducted on two different battery types:

- **KOKAM SLPB 52495 Pouch Cell**
- **LG Chem INR21700 M50**

## Key Features

### Data Processing
- **SOC Calculation**: Functions are provided to calculate the SOC based on the raw voltage data.
- **Resistance & Power Metrics**: The notebook computes the internal resistance at 0.1 seconds and 5 seconds after a load is applied and calculates the power discharge at each SOC level.

### OCV Analysis
- **SOC vs. OCV**: The relationship between SOC and OCV is explored for both battery types:
  - **KOKAM**: OCV increases non-linearly from ~3.1V at 10% SOC to ~4.2V at 100% SOC, with a steeper rise at lower SOC levels.
  - **LG Chem**: OCV shows a more linear increase from ~3.1V at 10% SOC to ~4.2V at 100% SOC, indicating a more predictable voltage response.

### Internal Resistance Characterization
- **Resistance vs. SOC**: Internal resistance is calculated and plotted against SOC:
  - **KOKAM**: Resistance decreases from ~0.07Ω at low SOC to ~0.05Ω at high SOC, with slight variations between the 0.1s and 5s measurements.
  - **LG Chem**: Exhibits lower resistance overall, ranging from ~0.03Ω to ~0.05Ω, consistently lower than KOKAM across all SOC levels.

### Power Discharge Evaluation
- **Power Discharge vs. SOC**: The power output is analyzed at different SOC levels:
  - **KOKAM**: Power increases from ~4.75W at low SOC to ~6.5W at high SOC, with minimal difference between 0.1s and 5s measurements.
  - **LG Chem**: Displays higher power output, from ~6.5W at low SOC to ~9.5W at high SOC, making it more suitable for high-power applications.

### Comparative Analysis
- **Strengths & Weaknesses**: The analysis provides a detailed comparison of the two batteries:
  - **LG Chem**: Superior in terms of linear OCV-SOC relationship, lower internal resistance, and higher power output.
  - **KOKAM**: Exhibits a more pronounced non-linear OCV increase and higher resistance, which may affect efficiency at lower SOC levels.

## Data Sources
The notebook utilizes Excel files containing battery measurement data:
- `Kokam_OCV.xlsx`
- `LG_OCV.xlsx`

## Visualizations
The notebook includes several informative plots:
- **SOC vs. OCV**
- **Resistance vs. SOC** (at 0.1s and 5s)
- **Power Discharge vs. SOC** (at 0.1s and 5s)

## Dependencies
The following Python libraries are required:
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `plotly.express`

## How to Use
1. Upload the Excel data files (`Kokam_OCV.xlsx` and `LG_OCV.xlsx`) to your Jupyter environment.
2. Run the Jupyter Notebook to execute the analysis.
3. Explore the generated plots and conclusions to gain insights into battery performance.

## Conclusion
This repository provides a valuable resource for understanding the performance characteristics of different battery types. It can serve as a foundational tool for further research or the development of battery management systems.
