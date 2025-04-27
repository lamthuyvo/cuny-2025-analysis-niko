# cuny-2025-analysis

Analysis of Retail Sales Data from January 2020 to March 2025 
This repository contains data, analytic code, and findings that will possibly support portions of an as of now, unpublished article. That article will contain important context and details.

## Data
This analysis uses a compilation of the Advance Monthly Sales for Retail and Food Services Report spreadsheet compiled from the [Census Bureau](https://www.census.gov/retail/sales.html).

The spreadsheets come from the following sources:

- Name of source:
  - [`SeriesReport-202504171535-V.xlsx`](../data/SeriesReport-202504171535-V.xlsx): Raw data of the retail sales.

Each of the spreadsheets contain the following columns relevant to the analysis:

- 'Period' — The month and year that the data for report was released.
- 'Value' — The sales for that month in the millions of dollars seasonally adjusted except for March 2025.

## Methodology

#### Part 1: Cleaning

- Removed the metadata rows from the raw spreadsheet using Google Sheets.
- Kept the 'Period' and 'Value' columns.
- Removed April to December 2025 from the 'Period' column because there is no data for those months.
- Downloaded that new spreadsheet to add to the data folder to analyze in Jupyter Notebook.

The notebook retail-sales-project.ipynb performs the following analyses:

#### Part 2: More Cleaning and Analysis

- Checked the data types and converted 'Value' column to numeric values.
- Calculated a 3-month moving average.
- Calculated the average to figure if a month had below or above average sales.
- Calculated year-over-year growth.
- Rounded the numbers to make them more readable.


## Outputs

The results from above are saved as: output/retail_sales_analysis.csv.

## Running the analysis yourself

You can run the analysis yourself. To do so, you'll need the following installed on your computer:

- Python 3
- The Python libraries specified in requirements.txt

## Licensing

All code in this repository is available under the MIT License. The data file in the output/ directory is available under the Creative Commons Attribution 4.0 International (CC BY 4.0) license. All files in the data/ directory are released into the public domain.

## Feedback / Questions?

Contact Niko Balkaran at niko.balkaran40@journalism.cuny.edu
