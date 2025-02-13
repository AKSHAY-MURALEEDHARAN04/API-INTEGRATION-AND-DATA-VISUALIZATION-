API-INTEGRATION-AND-DATA-VISUALIZATION

COMPANY:CODTECH IT SOLUTIONS
NAME:AKSHAY.M
INTERN ID:CT08NEP
DOMAIN:PYTHON
BATCH DURATION:January 15th/2025 to February 15th/2025


### Description of the Code

This Python script provides a streamlined way to visualize weather data using the OpenWeatherMap API, leveraging the power of the `requests`, `matplotlib`, and `seaborn` libraries for fetching and plotting weather trends. Here's a detailed breakdown of the functionality and workflow of the script:

---

#### **Overview**
The script fetches a 5-day weather forecast for a specified city (in this case, New York) from the OpenWeatherMap API and plots the temperature trends over time. The result is a clear and interactive line plot that helps users understand the variations in temperature throughout the forecast period.

---

#### **Key Functionalities**
1. **Fetching Weather Data from OpenWeatherMap API**
   - The script begins by setting up the API URL with placeholders for the city name (`CITY`) and the user's API key (`API_KEY`).
   - Using the `requests` library, it makes a GET request to the API endpoint to retrieve forecast data in JSON format. The `units=metric` parameter ensures that temperatures are provided in Celsius for consistency.

2. **Parsing and Extracting Data**
   - The script extracts relevant information, specifically:
     - **Dates and times** (`dt_txt`): Timestamps when the forecast data was recorded.
     - **Temperatures** (`main['temp']`): Forecasted temperatures at the corresponding timestamps.
   - These values are stored in lists (`dates` and `temperatures`) for easy manipulation.

3. **Data Visualization**
   - A temperature trend plot is created using the `seaborn` library's `lineplot` function, which enhances the visual aesthetics of the graph.
   - The X-axis represents the dates and times of the forecasts, while the Y-axis shows the temperatures in Celsius.
   - The `matplotlib` library's features are utilized to:
     - Rotate X-axis labels for better readability.
     - Add a title (`Temperature Trend in New York`) and axis labels for context.
     - Enable a grid to improve visual clarity.

4. **Customization and Presentation**
   - The plot is designed to be visually appealing and easily interpretable:
     - A marker (`o`) is added to each data point to highlight individual measurements.
     - The figure's size is adjusted (`figsize=(12, 6)`) for better viewing.
     - The `tight_layout()` function ensures the elements of the plot fit neatly within the display area.

---

#### **Requirements**
To run this script, the following dependencies need to be installed:
- **`requests`**: For making HTTP requests to the OpenWeatherMap API.
- **`matplotlib`**: For creating and customizing the plot.
- **`seaborn`**: For adding advanced visual elements to the graph.

Install these dependencies using pip:
```bash
pip install requests matplotlib seaborn
```

---

#### **Usage**
1. Replace `"your_api_key_here"` with your OpenWeatherMap API key.
2. Set the desired city name in the `CITY` variable.
3. Run the script in a Python environment. It will fetch the forecast data for the specified city and display a line plot showing the temperature trend.

---

#### **Output**
The script generates a clean and well-annotated line plot displaying the forecasted temperature trends for the city of New York over a 5-day period. This visualization can be adapted for other cities by changing the `CITY` variable.

This script is ideal for users looking to understand short-term weather patterns or integrate weather forecasting into their projects.
