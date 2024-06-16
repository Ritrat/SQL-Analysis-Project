# SQL Analysis and Visualization App

This application processes two SQL files, extracts various elements (like comments, table names, variables, return values, and mathematical formulae), and generates visualizations. The data and visualizations are then embedded into an Excel file which can be downloaded.

## Features
- Extracts comments, table names, variables, return values, and mathematical formulae from SQL files.
- Counts word occurrences and filters out words occurring less than a specified number of times.
- Generates visualizations including bar plots, pair plots, word frequency distributions, and word clouds.
- Embeds the extracted data and visualizations into an Excel file.

## Installation

1. Clone the repository:
    ```bash
    git clone <repository-url>
    cd <repository-directory>
    ```

2. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Run the Flask app:
    ```bash
    python app.py
    ```

2. Open your web browser and navigate to:
    ```
    http://127.0.0.1:5000/process
    ```

3. Upload the two SQL files you want to process.

4. The application will process the files and provide a downloadable link for the generated Excel file containing the extracted data and visualizations.

## Code Explanation

### `app.py`

- **Libraries**: Imports necessary libraries for text processing, data handling, visualization, and web app functionalities.
- **Flask App**: Sets up a Flask web server with a single route `/process` to handle file uploads.
- **Preprocessing Functions**: Functions to preprocess SQL text, extract elements, and count word occurrences.
- **Visualization Functions**: Functions to create and save visualizations as images.
- **Excel Export**: Uses `openpyxl` to create an Excel file, embedding data and visualizations in different sheets.
- **File Download**: Sends the generated Excel file as a download.

## File Structure

- `app.py`: Main application script.
- `requirements.txt`: List of Python dependencies.
- `README.md`: This file providing an overview of the application.

## Example

### Input:
Two SQL files uploaded via the web interface.

### Output:
An Excel file containing:
- Extracted comments, table names, variables, return values, and mathematical formulae.
- Visualizations such as:
  - Bar plots of the 20 most and least frequent words.
  - Pair plots for variable interactions.
  - Word frequency distribution histogram.
  - Word cloud for comments.

### Unique Insights:
To add unique insights to the EDA process of SQL data, I have implemented individual data visualization processes. These include:

- **Word Frequency Distribution**: Analyzing the distribution of words within the SQL files to identify the most common terms.
- **Pair Plot Visualization**: Using Seaborn and NumPy to visualize the interactions between different variables, which helps in identifying potential correlations.
- **Word Cloud**: Creating a word cloud from the comments in the SQL files, providing a visual representation of word frequency that is particularly useful for natural language processing (NLP) applications.
These visualizations offer valuable insights and enhance the exploratory data analysis of SQL data.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
