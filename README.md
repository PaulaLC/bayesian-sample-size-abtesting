# Sample Size Calculator

This Python script calculates the sample size required for a hypothesis test (only for conversion/proportion metrics) based on significance level, power, lift and conversion base, p0. It uses the `streamlit` library for creating a user interface, and other libraries such as `numpy`, `plotly.graph_objects`, and `statsmodels.stats.power`.

## Usage

1. Install the required libraries by running `pip install streamlit numpy plotly statsmodels`.
2. Run the script using `streamlit run sample_size_calculator.py`.
3. Enter the baseline conversion rate, lift, significance level, power, and alternative hypothesis in the input fields.
4. Click the "Calculate" button to calculate the sample size.
5. The calculated sample size will be displayed in a formatted manner.
6. A plot showing the sample size by lift will also be displayed.

## Functions

### `calculate_sample_size(p0, lift, sig_level, power, alternative)`

This function calculates the sample size required for a hypothesis test.

- `p0` (float): The baseline conversion rate.
- `lift` (float): The minimum detectable effect size.
- `sig_level` (float): The desired significance level (alpha).
- `power` (float): The desired statistical power.
- `alternative` (str): The alternative hypothesis ('two-sided', 'larger', or 'smaller').

Returns:
- `n` (int): The calculated sample size.

### `plot_sample_size(lifts, n_values)`

This function plots the sample size by lift.

- `lifts` (list): List of lift values.
- `n_values` (list): List of corresponding sample sizes.

Returns:
- None

## Example

You can add the following data as an example:

- baseline_conversion_rate = 0.1
- lift = 0.05
- significance_level = 0.05
- power = 0.8
- alternative = 'two-sided'

And then click the "Calculate" button.