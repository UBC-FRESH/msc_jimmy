
# Emission Calculation Model

This repository contains the Python script for calculating emissions based on various scenarios and parameters.

## Overview

The script mainly focuses on:
- Allocation rates for lumber.
- Applying a decay curve for Cross-Laminated Timber (CLT).
- Conversion rates for various products.
- Emission factors associated with different life cycle stages.
- Assumptions made regarding decay and landfill.

## Dependencies

- `pandas`: For data manipulation and analysis.
- `math`: Provides mathematical functions.
- `numpy`: For numerical operations.
- `os`: Provides functions to interact with the operating system.
- `matplotlib`: For plotting and visualization.
- `json`: To work with JSON data.

You can install the required packages using:
```
pip install pandas numpy matplotlib
```

## Usage

1. Set the required variables such as `scenario_name`, `inventory_retention`, and `clt_percentage`.
2. Optionally, there's a commented section to read configurations from a `scenario.json` file.
3. Run the script to generate emission calculations and outputs.

## Results

The results will be saved in a CSV file within the `model_result/emission_calculation/` directory, named based on the `scenario_name` and `inventory_retention`.

## Future Enhancements

The current version of the script provides a foundation for emission calculations. Future versions might include:
- Improved handling of configurations.
- More detailed analysis and visualizations.
- Better error handling and logging.

## Contributions

Feel free to fork this repository, make your changes, and submit a pull request. We appreciate your input!

## License

This project is licensed under the MIT License.

---

**Note**: This README is a draft and might require modifications based on the complete functionality and context of the script.
