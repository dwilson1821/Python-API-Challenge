# Python API Challenge: Weather and Vacation Analysis  

## Background  

The power of data lies in its ability to answer critical questions. In this project, you’ll analyze global weather data and identify ideal vacation spots based on user-defined preferences. This challenge is divided into two parts:  

1. **WeatherPy**: Visualize weather data across hundreds of cities to uncover relationships between latitude and weather variables.  
2. **VacationPy**: Plan vacations by filtering cities for ideal weather conditions and identifying nearby hotels using API calls and geospatial visualizations.  

This project utilizes the **OpenWeatherMap API**, **Geoapify API**, **citipy**, and **geoViews** libraries, alongside Python's data analysis and visualization tools.  

---

## Repository Structure  

The repository is organized as follows:  

```  
python-api-challenge/  
│  
├── WeatherPy/  
│   ├── WeatherPy.ipynb           # Jupyter Notebook for WeatherPy analysis  
│   ├── Resources/                # Folder for input/output files (e.g., CSVs)  
│   ├── api_keys.py               # File for storing API keys (excluded from GitHub)  
│   └── .gitignore                # File to exclude sensitive information  
│  
├── VacationPy/  
│   ├── VacationPy.ipynb          # Jupyter Notebook for VacationPy analysis  
│   └── Resources/                # Folder for input/output files  
│  
└── README.md                     # This README file  
```  

---

## Objectives  

### Part 1: WeatherPy  

Using a dataset of over 500 randomly selected cities across the globe:  

1. **Retrieve Weather Data**  
   - Use the **OpenWeatherMap API** to extract temperature, humidity, cloudiness, and wind speed data.  

2. **Visualize Relationships**  
   - Generate scatter plots for:  
     - Latitude vs. Temperature  
     - Latitude vs. Humidity  
     - Latitude vs. Cloudiness  
     - Latitude vs. Wind Speed  
   - Analyze relationships and trends.  

3. **Perform Linear Regression Analysis**  
   - Separate data into Northern and Southern Hemispheres.  
   - Perform linear regression for each variable (e.g., Temperature vs. Latitude) for both hemispheres.  
   - Visualize results with regression lines, formulas, and r² values.  
   - Summarize findings for each relationship.  

### Part 2: VacationPy  

Using the weather data generated in **WeatherPy**:  

1. **Filter for Ideal Conditions**  
   - Define parameters for ideal vacation weather (e.g., temperature range, wind speed, cloudiness).  
   - Narrow down the dataset to cities meeting these criteria.  

2. **Identify Nearby Hotels**  
   - Use the **Geoapify API** to find hotels within 10,000 meters of each city’s coordinates.  
   - Create a new DataFrame to store city, country, coordinates, humidity, and hotel names.  

3. **Create Interactive Maps**  
   - Plot all cities on a map, with the point size corresponding to humidity.  
   - Generate a second map showing hotels in filtered vacation cities with hover functionality for additional details (e.g., hotel name and country).  

---

## Installation and Usage  

### Prerequisites  
- Python 3.x  
- Jupyter Notebook  
- Required Libraries: Pandas, NumPy, Matplotlib, SciPy, citipy, requests, geoViews  

### Setup Instructions  

1. **Clone the Repository**  
   ```bash  
   git clone https://github.com/your-username/python-api-challenge.git  
   cd python-api-challenge  
   ```  

2. **Install Required Libraries**  
   ```bash  
   pip install pandas numpy matplotlib scipy citipy requests geoviews  
   ```  

3. **Add Your API Keys**  
   - Create an `api_keys.py` file in the project folder.  
   - Add your **OpenWeatherMap API** and **Geoapify API** keys as variables:  
     ```python  
     weather_api_key = "your_openweathermap_api_key"  
     geoapify_key = "your_geoapify_api_key"  
     ```  

4. **Run the Jupyter Notebooks**  
   - Navigate to the project folder and launch Jupyter Notebook:  
     ```bash  
     jupyter notebook  
     ```  
   - Open and run `WeatherPy.ipynb` and `VacationPy.ipynb`.  

---

## Data Sources  

1. **OpenWeatherMap API**  
   - Provides weather data (e.g., temperature, humidity, cloudiness, wind speed) for cities worldwide.  

2. **Geoapify API**  
   - Used for geocoding and identifying nearby hotels for filtered vacation cities.  

3. **citipy Library**  
   - Identifies the nearest city for a set of random latitude and longitude coordinates.  

---

## Key Features  

### WeatherPy  
- **Scatter Plots**: Highlight relationships between latitude and weather variables.  
- **Linear Regression**: Visualizes trends and computes statistical relationships between hemispheric data.  

### VacationPy  
- **City Filtering**: Finds cities with ideal weather conditions based on user preferences.  
- **Hotel Mapping**: Displays vacation cities and nearby hotels on an interactive map.  

---

## Observations  

1. **Temperature vs. Latitude**  
   - As expected, temperatures increase as latitude approaches the equator (0°).  
   - Northern and Southern Hemisphere trends mirror each other.  

2. **Humidity, Cloudiness, and Wind Speed**  
   - No strong correlations with latitude, though regional patterns may exist.  

3. **Vacation Planning**  
   - The filtering process provides customizable options for narrowing down ideal destinations based on weather.  
   - Interactive maps offer a clear visualization of potential vacation spots and accommodations.  
