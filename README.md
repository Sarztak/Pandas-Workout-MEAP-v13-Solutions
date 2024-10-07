# Pandas-Workout-MEAP-v13-Solutions
Documented solutions to solved and unsolved exercises in the book Pandas Workout by Dr. Reuven M. Lerner


# Pandas Workout Solutions

## Overview
This repository contains my solutions to the exercises from the book **Pandas Workout** by Dr. Reuven M. Lerner. This book has been an invaluable resource for enhancing my skills in data manipulation and analysis using the Pandas library. Through the exercises, I have gained hands-on experience with various data wrangling techniques and learned to tackle real-world data challenges.

# Pandas Workout Solutions

## Overview
This repository contains my solutions to the exercises from the book **Pandas Workout** by Dr. Reuven M. Lerner. This book has been an invaluable resource for enhancing my skills in data manipulation and analysis using the Pandas library. Through the exercises, I have gained hands-on experience with various data wrangling techniques and learned to tackle real-world data challenges.

## What I Learned

### Data Handling and Cleaning
- **Confronting Real-World Data Challenges**: 
  - Worked with messy datasets that included human errors, inconsistent formats, and missing values.
  - Developed patience and problem-solving skills by navigating the complexities of real data.
  
- **Techniques for Handling Missing Data**:
  - Utilized methods such as `.isnull()`, `.notnull()`, `.interpolation()`, `.dropna()`, and `.fillna()` to identify and manage missing values effectively.
  - Learned to use `.replace()` for mapping incorrect values to correct ones, enhancing data quality.
  - Gained insights into the importance of data fidelity and the underlying data generation process.

### Data Structures
- **Creating and Manipulating Series and DataFrames**:
  - Created Series from single-column CSV files using the `.squeeze()` method.
  - Set appropriate index and data types in the `read_csv()` method.
  - Constructed DataFrames using lists of lists, lists of dictionaries, dictionaries of lists, and 2D NumPy arrays.
  
- **Data Selection and Filtering**:
  - Mastered selection techniques using `.loc[]`, `.iloc[]`, and boolean indexing to filter rows and columns.
  - Set new columns by transforming existing columns.
  - Appended multiple DataFrames row-wise or column-wise using `pd.concat()`.
  - Set columns as index using `.set_index()`.
  - Understood the difference between altering DataFrames with and without `inplace=True`.
  - Explored how slices inside `[]` are interpreted to mean rows rather than columns, while `['x']` or `[['a', 'b', 'c']]` is interpreted to mean column names.
  - Filtered rows and columns using `.query()` similar to SQL queries.
  - Understood the dreaded `SettingWithCopyWarning`.

### Data Transformation and Aggregation
- **Method Chaining**:
  - Employed method chaining for complex data transformations.
  
- **Grouping and Aggregation**:
  - Gained proficiency in grouping data using `.groupby()` and applying multiple operations with `.agg()`, `.transform()`, and lambda functions.
  - Filtered on grouped DataFrames using `.filter()`.
  - Used numeric_only=True argument in `.mean()` to skip operations on non-numeric columns.
  - Understood the distinction between `.groupby()` and `.transpose()`.

- **Pivot Tables**:
  - Created pivot tables using `.pivot_table()` for better data summarization and analysis across multiple dimensions.

### Indexing and Multi-Indexing
- **Setting and Resetting Indexes**:
  - Learned to set and reset multi-index rows and columns using `.set_index()` and `.reset_index()`.
  - Retrieved elements from multi-indexed rows and columns using tuples of index values or `slice()` inside `.loc[]`.
  - Utilized alternative slicing methods such as `.xs[]` and `pd.IndexSlice`.
  - Optimally sorted multi-indexed labels by using `.is_monotonic_increasing()`.

### Importing and Exporting Data
- **Reading and Writing Data**:
  - Gained proficiency in reading and writing data in various formats (CSV, JSON) with appropriate parameters such as `sep`, `index_col`, `usecols`, `header`, `dtypes`, `low_memory`, `skip_blank_lines`, `names`, and `comment` in `.read_csv()`.
  - Read CSV files from the web using `requests` and decoded the data using `StringIO`.
  - Read JSON files with `.read_json()`.

### String Manipulation
- **String Methods and Accessors**:
  - Understood the `str` accessor on Series containing string data types.
  - Explored the utility of `pd.StringDType`.
  - Learned several common string methods such as `.isdigit()`, `.lower()`, `.upper()`, `.strip()`, etc.
  - Used regex expressions for filtering strings using `.contains()`.
  - Split a single string column into multiple columns using `.split()` and `.explode()`.
  - Created dummy/indicator variables using `.get_dummies()`.

### Date and Time Handling
- **Working with Timestamps**:
  - Created Timestamp objects from strings of dates using `pd.to_datetime()`.
  - Understood different time formats and how Pandas processes them automatically.
  - Provided correct time format if automatic extraction fails due to exotic or incorrect time formats not generally used.
  - Extracted days, months, years, and weekdays from dates.

### Visualization
- **Data Visualization Techniques**:
  - Created various plots using Pandas' built-in `.plot` utility, including:
    - **Pie plots** for visualizing proportions.
    - **Scatter plots** for examining relationships between two variables.
    - **Box plots** for displaying the distribution of data and identifying outliers.
    - **Histograms** for understanding the frequency distribution of numerical data.
    - **Density distribution plots** for visualizing the probability density function of a continuous variable.
  
- **Faceting Plots**:
  - Facetted plots by a category to compare distributions across different groups.

- **Using Seaborn Library**:
  - Utilized Seaborn functions such as:
    - `.relplot()` for visualizing relationships between variables with additional context.
    - `.catplot()` for categorical data visualization.
    - `.displot()` for flexible histogram and density plots, allowing for better control over aesthetics and layout.

### Performance Optimization
- **Memory Management**:
  - Checked memory usage with `.memory_usage()` and the `deep=True` argument to understand memory consumption.
  - Specified data types while importing data to save memory and improve performance.
  - Cast string data to categorical data type using `.astype('category')` to enhance memory efficiency.

- **Efficient Data Storage**:
  - Explored storing data efficiently using binary formats like Apache Arrow for faster read/write operations.

- **Speeding Up File Operations**:
  - Improved file read operations by parsing files using the `engine='python'` or `engine='pyarrow'` argument in `.read_csv()`.
  - Set `low_memory=False` in `.read_csv()` to speed up reading by preventing Pandas from guessing data types, which can be time-consuming.

- **Reducing Memory Usage**:
  - Reduced memory usage required in building boolean series from multiple conditions using `eval()` and `query()` for more efficient data manipulation.

### Midway Project
- **Integration of Skills**:
  - Utilized all the skills learned throughout the exercises on a real dataset: the Stack Overflow Survey results.
  - The project involved various data wrangling tasks, including:
    - Merging multiple datasets to create a comprehensive view of the survey results.
    - Sorting data to organize it meaningfully for analysis.
    - Setting multiple indexes to facilitate easier data retrieval and manipulation.
    - Performing general cleaning tasks to ensure data quality and consistency.
    - Extracting summary statistics and insights from the datasets to draw meaningful conclusions.

### Final Project
- **Culmination of Learning**:
  - Applied all the skills acquired throughout the book in a comprehensive final project.
  - Focused on a dataset of interest, integrating various techniques learned, such as:
    - Data cleaning and preprocessing.
    - Advanced data manipulation and transformation.
    - Visualization of results to communicate findings effectively.
  - The final project served as a practical demonstration of my proficiency in using the Pandas library for data analysis and reinforced my understanding of the concepts covered in the book.
    
Contribution
I welcome feedback, suggestions, and corrections on my solutions. Feel free to explore the repository and reach out with any remarks!

Thank you for your interest in my work with the Pandas Workout book!
