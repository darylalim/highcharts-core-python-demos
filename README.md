# Highcharts Core for Python Demos

Demo collection for Highcharts Core for Python - Python wrapper for the world's leading data visualization library.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Best Practices](#best-practices)
- [Performance Tips and Limitations](#performance-tips-and-limitations)
- [Integration with Jupyter Notebooks](#integration-with-jupyter-notebooks)
- [Support and Resources](#support-and-resources)
- [License](#license)

## Overview

Python wrapper for Highcharts JS with full API support, pandas/Jupyter integration, and automatic data validation. Write Python, generate JavaScript.

## Features

- 70+ chart types (line, bar, pie, heatmaps, network graphs, etc.)
- Direct Jupyter notebook display
- One-line pandas DataFrame plotting
- Export to JavaScript, PNG, SVG, PDF
- Responsive and interactive by default
- Real-time data updates

## Installation

**Requirements:** Python 3.10+, Highcharts JS 10.2+

```bash
# Create virtual environment
python3 -m venv highcharts_core_env
source highcharts_core_env/bin/activate  # On Windows: highcharts_core_env\Scripts\activate

# Install
pip install highcharts-core          # Basic
pip install highcharts-core[soft]    # With all optional dependencies (recommended)
```

## Best Practices

1. **Property maps for DataFrames**: Use `property_map={'x': 'col1', 'y': 'col2'}` with pandas
2. **Snake_case**: Write Python-style, auto-converts to JavaScript camelCase
3. **Validation**: Library catches config errors early
4. **Large datasets**: Enable boost module and set turboThreshold > 10000
5. **Reuse configs**: Create base HighchartsOptions for consistency

## Performance Tips and Limitations

**Performance:**
- Large datasets (>5000 points): Enable boost module, increase turboThreshold
- Multiple series: Disable animations and markers
- Memory: Clear unused series, use lazy loading for large files

**Limitations:**
- Requires JavaScript environment (browser/Jupyter)
- Static export needs Highcharts Export Server
- Browser-dependent max ~1M data points

## Integration with Jupyter Notebooks

All examples are provided as Jupyter notebooks. To run them:

```bash
# Install JupyterLab
pip install jupyterlab>=4.0.0

# Start JupyterLab
jupyter lab

# Navigate to any .ipynb file and run all cells
```

In Jupyter, you can display charts interactively:

```python
# Display chart inline
chart.display()

# Or save to file
chart.download_chart(filename='my_chart.png', format='png')
```

## Support and Resources

[Documentation](https://core-docs.highchartspython.com/) | [Forum](https://www.highcharts.com/forum) | [Issues](https://github.com/highcharts-for-python/highcharts-core/issues) | [Support](https://highchartspython.com/get-help/)

## License

See your Highcharts license terms. Commercial use requires a commercial license. [More info](https://www.highcharts.com/license).

---

Made with ❤️ by the human and Claude