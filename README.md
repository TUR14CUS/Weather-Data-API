# Readme for Weather Data API

This Flask web application provides a simple API to retrieve weather data from meteorological stations. The data is stored in text files, and the application serves endpoints to retrieve specific information, such as temperature for a given date, all data for a particular station, and yearly data for a specific station and year.

## Getting Started

1. Clone the repository to your local machine:

```bash
git clone https://github.com/TUR14CUS/Weather-Data-API.git
cd Weather-Data-API.git
```

2. Install the required dependencies:

```bash
pip install Flask pandas
```

3. Run the Flask application:

```bash
python main.py
```

The application will start running on `http://127.0.0.1:5000/`. You can access the different API endpoints described below.

## API Endpoints

### 1. Get Home Page

- **Endpoint:** `/`
- **Method:** GET
- **Description:** Displays the home page with a table of meteorological station data.
- **Example:** [http://127.0.0.1:5000/](http://127.0.0.1:5000/)

### 2. Get Temperature for a Specific Date

- **Endpoint:** `/api/v1/<station>/<date>`
- **Method:** GET
- **Parameters:**
  - `<station>`: Meteorological station ID.
  - `<date>`: Date in the format YYYY-MM-DD.
- **Description:** Retrieves the temperature for a specific station on a given date.
- **Example:** [http://127.0.0.1:5000/api/v1/123456/2022-01-27](http://127.0.0.1:5000/api/v1/123456/2022-01-27)

### 3. Get All Data for a Specific Station

- **Endpoint:** `/api/v1/<station>`
- **Method:** GET
- **Parameters:**
  - `<station>`: Meteorological station ID.
- **Description:** Retrieves all data for a specific station.
- **Example:** [http://127.0.0.1:5000/api/v1/123456](http://127.0.0.1:5000/api/v1/123456)

### 4. Get Yearly Data for a Specific Station and Year

- **Endpoint:** `/api/v1/yearly/<station>/<year>`
- **Method:** GET
- **Parameters:**
  - `<station>`: Meteorological station ID.
  - `<year>`: Year in the format YYYY.
- **Description:** Retrieves yearly data for a specific station and year.
- **Example:** [http://127.0.0.1:5000/api/v1/yearly/123456/2022](http://127.0.0.1:5000/api/v1/yearly/123456/2022)

## Notes

- Make sure to replace the station ID and date in the examples with actual data from your dataset.
- The application uses pandas for data manipulation and Flask for web serving. Ensure that you have the necessary dependencies installed.
- The data files are assumed to be in a specific format. Adjust the code accordingly if your data format is different.

Feel free to customize and extend this Flask application based on your specific requirements!
