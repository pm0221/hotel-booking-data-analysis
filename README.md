# Hotel Booking Data Analysis

## Project Overview
This project performs exploratory data analysis (EDA) on a hotel booking dataset using Python. It examines hotel booking records, checks data quality, handles missing values, summarizes numerical and categorical variables, and visualizes patterns in bookings and cancellations.

The analysis is implemented in the Jupyter Notebook `lab1.ipynb`.

## Objectives
- Load and inspect the hotel booking dataset.
- Understand the structure and summary statistics of the data.
- Identify and handle missing values.
- Separate categorical and numerical columns for analysis.
- Explore correlations between numerical variables.
- Visualize hotel types, lead times, numerical distributions, outliers, and cancellation patterns.

## Dataset
The notebook reads a CSV file named **`hotel_booking.csv`**.

The notebook expects the dataset at:

```text
/content/hotel_booking.csv
```

If you are running the notebook locally, update the `pd.read_csv()` path to the location of your `hotel_booking.csv` file.

## Analysis Workflow

### 1. Import Libraries
The notebook imports:
- **NumPy** – numerical operations.
- **Pandas** – data loading and manipulation.
- **Matplotlib** – plotting and visualization.
- **Seaborn** – statistical data visualization.

### 2. Load and Inspect the Dataset
- Load `hotel_booking.csv` into a Pandas DataFrame.
- Display the first few rows.
- Inspect column data types and non-null counts.
- Generate descriptive statistics.
- Check the dataset dimensions and column names.

### 3. Handle Missing Values
- Fill missing values in `children` with the column mode.
- Fill missing values in `country` with the column mode.
- Fill missing values in `agent` with the column mean.
- Drop the `company` column.
- Check missing-value counts again after preprocessing.

### 4. Separate Categorical and Numerical Data
The notebook selects a set of booking-related categorical columns, including hotel, cancellation status, arrival year and month, meal, country, market segment, distribution channel, guest status, deposit type, customer type, and reservation status.

Numerical columns are selected using their `int64` and `float64` data types.

### 5. Exploratory Data Analysis and Visualizations
The notebook creates the following visualizations:

- **Correlation heatmap:** Shows correlations among numerical variables.
- **Hotel type count plot:** Displays the distribution of hotel types.
- **Lead time histogram:** Shows the distribution of booking lead times.
- **Numerical box plots:** Helps inspect possible outliers across numerical columns.
- **Pair plot:** Explores relationships among lead time, ADR, weekend-night stays, and cancellation status.
- **ADR box plot by cancellation status:** Compares average daily rate (ADR) across canceled and non-canceled bookings.

## Technologies and Libraries
- Python
- Jupyter Notebook
- NumPy
- Pandas
- Matplotlib
- Seaborn

## Installation

Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

## How to Run
1. Place `lab1.ipynb` and `hotel_booking.csv` in your project folder.
2. Open a terminal in that folder.
3. Start Jupyter Notebook:

   ```bash
   jupyter notebook
   ```

4. Open `lab1.ipynb`.
5. If needed, update the CSV file path in the data-loading cell.
6. Run all notebook cells in order.

## Project Structure

```text
Hotel_Booking_Data_Analysis/
├── lab1.ipynb
├── hotel_booking.csv
└── README.md
```

## Notes
- The dataset is required to run the notebook and is not embedded in the notebook.
- Missing values are handled using the mode for `children` and `country`, and the mean for `agent`.
- The `company` column is dropped during preprocessing.
- This notebook focuses on data inspection, preprocessing, and exploratory visualizations. It does not train a predictive machine-learning model.

## Author
Add your name and academic details here.
