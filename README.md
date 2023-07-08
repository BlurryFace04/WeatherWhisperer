# WeatherWhisperer
### This was my submission for the Fastest-Coder-First Hackathon hosted by Microsoft, in which I had the opportunity to participate live from their Gurgaon Headquarters.
Well for the description, WeatherWhisperer is a Python application that fetches weather data from the OpenWeatherMap API and generates a creative description of the weather using OpenAI's GPT-3.5-turbo language model.
<br>

## Streamlit Web App:

![web-app](https://github.com/BlurryFace04/WeatherWhisperer/blob/main/web-app.png)

<br>

## Data Stored In JSON File:

![json-file](https://github.com/BlurryFace04/WeatherWhisperer/blob/main/json-file.png)

# Install Dependencies:
To install the libraries required for this project use this command:
```
pip install -r requirements.txt
```

# How it Works:
1. The application starts by getting the city name from the user.
2. It then fetches the latitude and longitude of the city using the OpenWeatherMap API.
3. The application fetches the weather data for the city using the latitude and longitude obtained.
4. For each weather forecast, it generates a creative description using the GPT-3.5-turbo model from OpenAI.
5. The weather data along with the generated descriptions are then displayed to the user.

# Usage
To run the application, use the following command:
```
streamlit run main.py
```

In the Streamlit application, in the text box, enter the command in this format:
```
python main.py <city name>
```

Replace <city name> with the name of the city you want to fetch the weather data for. The application will then display the weather data and the generated description.

**Note:** The command python main.py <city name> is a simulation of how the command would be run in a terminal, but it is supposed to be entered in the streamlit application's text box. The actual command to run the Streamlit application is streamlit run main.py.

# Output
The application outputs the weather data and the generated description to the Streamlit interface. It also saves this data to a data.json file in the same directory as the script.

# Error Handling
The application includes error handling for various types of errors that can occur during the API calls to OpenWeatherMap and OpenAI.

# Architectural Flow
The application follows a clear architectural flow for fetching and generating a creative description of the weather. Here's how it works:
1. **Input:** The user provides a city name.
2. **Fetching Geographic Coordinates:** The application uses the OpenWeatherMap GeoCoding API to fetch the latitude and longitude of the city specified by the user. This is done using the get_latitude_longitude(city) function.
3. **Fetching Weather Data:** The latitude and longitude obtained in the previous step are then used to fetch the weather forecast data for that location using the OpenWeatherMap One Call API. This is achieved using the get_weather(lat, lon) function.
4. **Generating Creative Description:** The application then generates a creative description of the weather forecast data using OpenAI's GPT-3.5-turbo model. This is done in the generate_description(forecast_data) function. The generated description is more engaging and appealing to read than the raw weather data.
5. **Output:** The application finally presents the creatively described weather data to the user.

# Usage of Github Co-Pilot:
In the development of the WeatherWhisperer project, GitHub Copilot was utilized in several ways:
1. **Writing Boilerplate Code:** GitHub Copilot was able to provide quick snippets of boilerplate code for common tasks such as making HTTP requests with the requests library, handling exceptions, and formatting dates with the datetime library.
2. **API Calls:** Copilot provided guidance on how to structure API calls to the OpenWeatherMap API and OpenAI API. It suggested the endpoints to use, how to pass parameters, and how to handle the responses.
3. **Error Handling:** GitHub Copilot assisted in writing comprehensive error handling for the API calls. It suggested the different types of exceptions that could be raised during an API request and how to handle each one.
4. **Code Documentation:** Copilot provided useful suggestions for documenting the code with comments and docstrings. These make the code easier to understand and maintain.
5. **Streamlit UI:** Copilot provided suggestions for building a user-friendly interface with Streamlit. It offered suggestions on how to take user input and display the output in a readable format.
6. **Data Manipulation:** Copilot provided assistance in manipulating and formatting the weather data for both display and storage purposes.
<br>
Overall, GitHub Copilot served as an AI-powered pair programmer that helped speed up the development process, reduce the chance of errors, and improve the quality of the code. It was particularly helpful for developers who are not familiar with certain libraries, APIs, or coding patterns. By suggesting completions, it can provide valuable learning opportunities and insights into best practices.

# Contributions
Contributions to the WeatherWhisperer project are welcome. Please ensure that you test the application thoroughly before making a pull request.
