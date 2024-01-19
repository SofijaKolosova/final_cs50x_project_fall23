# weather forecast
# Video Demo:
https://youtu.be/ay4kgskYyeM?si=Mx5n6s_ohT09v5yx 
# final_cs50x_project_fall23
Showing Example of Final Project ideas for Harvard CS50X
This Python program utilizes the `requests` library to fetch weather data from the Open Meteo API based on the latitude and longitude of a specified city. The program then extracts and writes the hourly temperature forecast to a CSV file.

Here's a breakdown of the key components:

1. City Coordinates and Default City:
   - The program defines a dictionary `cities` containing the coordinates (latitude, longitude) of various cities.
   - The `DEFAULT_CITY` variable is set to "Rīga."

2. API Request Function:
   - The `make_api_request` function constructs a URL and uses the `requests.get` method to fetch weather data from the Open Meteo API.

3. CSV Writing Function:
   - The `write_to_csv` function takes the city name and the API response as parameters.
   - It generates a timestamp for the file name and writes a CSV file containing the time and corresponding temperature for each hour.

4. Main Function:
   - The `main` function prompts the user to enter a city name.
   - If the entered city is in the predefined dictionary, it retrieves the corresponding coordinates. Otherwise, it defaults to the coordinates of "Rīga."
   - The program then makes an API request and, if successful (status code 200), writes the temperature data to a CSV file. If there is an error, it prints the status code.

5. Execution:
   - The script executes the `main` function if the script is run directly, allowing users to input a city name and obtain a temperature forecast CSV file.

6. Timestamped CSV Files:
   - The CSV files are timestamped with the city name and the current date and time to ensure uniqueness.

7. Printed Output:
   - During the CSV writing process, the program also prints the time and temperature for each hour.

8. Error Handling:
   - The program checks for a successful response (status code 200) from the API. If there is an error, it prints the status code.

In summary, this program provides a simple interface for users to input a city name, fetch weather data from the Open Meteo API, and save the hourly temperature forecast to a timestamped CSV file.
