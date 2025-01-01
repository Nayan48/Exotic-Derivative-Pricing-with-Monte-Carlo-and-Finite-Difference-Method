# Exotic-Derivative-Pricing-with-Monte-Carlo-and-Finite-Difference-Method

## Overview

This project focuses on pricing and sensitivity analysis of exotic derivatives, specifically **Asian Options** and **Lookback Options**, using **Monte Carlo Simulations** and **Finite Difference Methods**. These methods address the challenges associated with the valuation of path-dependent options by leveraging advanced numerical techniques.

The primary objective of this project is to compute the expected payoff under **risk-neutral valuation** while analyzing sensitivities (Greeks) using **parameter perturbation**.

---

## Project Structure

The project includes the following sections:

1. **Outline of Finance Problems and Numerical Methods**

   - Challenges in valuing exotic options.
   - Role of Monte Carlo simulations and Finite Difference Methods.

2. **Results**

   - Option pricing tables for Asian and Lookback options.
   - Comparative results under varying parameters.

3. **Observations with Visualizations**

   - Key insights on the impact of parameter variations.
   - Sensitivity analysis with Greeks.

4. **Conclusion and References**

---

## Key Concepts

### Exotic Options

1. **Asian Options:**

   - Payoff depends on the average price of the underlying asset over a specified period.
   - Smooths volatility and reduces price manipulation.
   - Applications: Used in commodities and foreign exchange markets.

2. **Lookback Options:**

   - Payoff depends on the maximum or minimum price during the life of the option.
   - Eliminates the risk of poor timing decisions.
   - Applications: Used for speculative investments and hedging.

### Numerical Methods Used

1. **Monte Carlo Simulations:**

   - Uses the **Euler-Maruyama scheme** for simulating stock price paths.
   - Tracks path dependency for payoff calculations.
   - Implements risk-neutral valuation for fair pricing.

2. **Finite Difference Methods (FDM):**

   - Approximates sensitivities (Greeks) by perturbing parameters.
   - Efficient for calculating Delta, Gamma, Vega, and Theta.

---

## Code Implementation

### Monte Carlo Simulation Framework

The simulation uses **Geometric Brownian Motion (GBM)** to model the stock price evolution:

- **SDE:**


  Where:

  - : Stock price.
  - : Risk-free rate.
  - : Volatility.
  - : Wiener process.

- **Euler-Maruyama Discretization:**


  Where .

### Payoff Calculations

1. **Asian Options:**
   - Call Payoff:&#x20;
   - Put Payoff:&#x20;
2. **Lookback Options:**
   - Call Payoff:&#x20;
   - Put Payoff:&#x20;

### Sensitivity Analysis with Greeks

1. **Delta:** Sensitivity to the underlying price.


2. **Gamma:** Rate of change of Delta.


3. **Vega:** Sensitivity to volatility.


4. **Theta:** Sensitivity to time decay.


---

## Results

### Parameter Variations

1. **Volatility (****)**

   - Higher volatility leads to increased option prices.
   - Lookback options are particularly sensitive to extreme price movements.

2. **Strike Price (****)**

   - Higher strike prices decrease call option prices and increase put option prices.

3. **Time to Expiration (****)**

   - Longer durations result in higher prices due to increased uncertainty.

4. **Risk-Free Rate (****)**

   - Higher rates increase call prices and decrease put prices.

### Key Insights

- **Asian Options:**

  - Call prices increase significantly with time and volatility.
  - Delta decreases with longer expiration and higher strike prices.

- **Lookback Options:**

  - Highly sensitive to extreme price variations.
  - Gamma and Vega are prominent for long-dated options with high volatility.

---

## Visualizations

- **3D Surface Plots:**

  - Sensitivity of option prices to volatility and time.

- **Greeks Visualization:**

  - Delta, Gamma, Vega, and Theta trends.

- **Comparison:**

  - Asian vs. Lookback options under identical parameters.

---

## File Descriptions

1. **`Exotic_Derivatives_Analysis.pdf`****:** Detailed project report, including methodology, results, and visualizations.
2. **`Exotic_Derivatives_Analysis.ipynb`****:** Jupyter Notebook containing the Python code for simulations and sensitivity analysis.

---

## How to Run

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/Exotic-Derivatives-Pricing.git
   ```

2. **Install Dependencies:**

   ```bash
   pip install numpy pandas matplotlib
   ```

3. **Run the Jupyter Notebook:**

   ```bash
   jupyter notebook Exotic_Derivatives_Analysis.ipynb
   ```

4. **Generate Results:**

   - Visualize stock price paths and payoffs.
   - Compare option pricing tables and Greeks.

---

## Conclusion

This project demonstrates how advanced numerical methods can be used to value exotic options and analyze their sensitivities. The comparison of Monte Carlo simulations with sensitivity analysis provides actionable insights for financial practitioners.

---

## License

MIT License

---

## References


CQF Lectures from Module-3:
JA243.4 Intro to Numerical Methods
JA243.5 Exotic Options
CQF Python Labs:
JA24P6 Monte Carlo Simulation
JA24P7 Finite Difference Methods
Paul Wilmott (2007), Paul Wilmott introduces Quantitative Finance
Tavella, D., & Randall, C. (2000). Pricing Financial Instruments: The Finite
Difference Method. Wiley.
Python Resources
