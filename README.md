# API-INTEGRATION-Weather-app-

* COMPANY *: CODTECH IT SOLUTIONS

* NAME * : GADDAM RAKSHITH REDDY

* INTERN ID * : CT08QVI

* DOMAIN * : FULL STACK DEVELOPMENT

* DURATION * : 4 WEEEKS

* MENTOR *: NEELA SANTOSH KUMAR

*DESCRIPTION :*

An API-integrated weather app is a dynamic and interactive application designed to provide users with real-time weather information by leveraging data from external weather services through Application Programming Interfaces (APIs). This type of app is typically built using fundamental web development technologies such as HTML, CSS, and JavaScript, making it accessible and easy to develop for beginners and experienced developers alike. The app fetches weather data such as temperature, humidity, wind speed, precipitation, and forecasts for specific locations, and presents it in a user-friendly interface. The development process is streamlined using tools like Visual Studio Code (VSCode) as the primary platform for writing and compiling code, and the Live Server extension to preview and test the app in real-time.

### Key Features of an API-Integrated Weather App 

1. *Real-Time Weather Data*:

 The app connects to weather APIs like OpenWeatherMap, Weatherstack, or AccuWeather to fetch up-to-date weather information for any location.

2. *User-Friendly Interface*:

 The app displays weather data in a clean and intuitive layout, often including icons, graphs, and maps to enhance readability.

3. *Location-Based Services*:

Users can search for weather information by entering a city name or using GPS to automatically detect their location.

5. *Interactive Elements*:

 Features like dynamic backgrounds, animations, and responsive designs improve user engagement.

5. *Customizable Alerts*:

Users can set notifications for specific weather conditions, such as rain, storms, or extreme temperatures.

6. *Cross-Platform Compatibility*:

Built using web technologies, the app can run on both desktop and mobile browsers.

### Development Process

The development of an API-integrated weather app involves several steps, starting with setting up the project in VSCode, a popular code editor known for its versatility and extensive library of extensions. The Live Server extension is particularly useful for testing the app, as it allows developers to see changes in real-time without manually refreshing the browser.

#### 1. *HTML (Structure)*

HTML is used to create the basic structure of the app, including elements like input fields for location search, containers for displaying weather data, and placeholders for icons and images. For example:
```html

        <input type="text" placeholder="Enter City Name" spellcheck="false">
        <button><img src="images/search.png" alt="search"></button>
    </div>
    <div class="error">
        <p>Invalid City name</p>
    </div>
    <div class="weather">
        <img src="images/clear.png" class="weather-icon">
        <h1 class="temp">22°C</h1>
        <h2 class="city">Hyderabad</h2>
        <div class="details">
            <div class="col">
                <img src="images/humidity.png" alt="humidity">
                <div>
                    <p class="humidity">50%</p>
                    <p>Humidity</p>
                </div>
            </div>
            <div class="col">
                <img src="images/wind.png" alt="wind">
                <div>
                    <p class="wind">15 km/h</p>
                    <p>Wind Speed</p>
                </div>
            </div>
        </div>
```

#### 2. *CSS (Styling)* 

CSS is used to style the app, making it visually appealing and responsive. This includes designing layouts, adding animations, and ensuring the app looks good on different screen sizes. For example:
```css

.weather-icon{
    width: 170px;
    margin-top: 30px;
}
.weather h1{
    font-size: 80px;
    font-weight: 500;
}
.weather h2{
    font-size: 45px;
    font-weight: 400;
    margin-top: -10px;
}
.details{
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 20px;
    margin-top: 50px;
}
```

#### 3. *JavaScript (Functionality)*

JavaScript is the backbone of the app, handling the logic for fetching data from the weather API, processing it, and dynamically updating the HTML content. The fetch API is commonly used to make HTTP requests to the weather service. For example:
```javascript

 const apikey = "4e5e5de002a27697386048244a7232d9";
 const apiurl = "https://api.openweathermap.org/data/2.5/weather?&units=metric&q=";

 const searchBox = document.querySelector(".search input");
 const searchBtn = document.querySelector(".search button");
 const weathericon = document.querySelector(".weather-icon");


 async function checkWeather(city){
    const response = await fetch(apiurl + city + `&appid=${apikey}`);

if(response.status == 404){
    document.querySelector(".error").style.display = "block";
    document.querySelector(".weather").style.display = "none";
}
else{
var data = await response.json();
    
document.querySelector(".city").innerHTML = data.name;
document.querySelector(".temp").innerHTML = Math.round(data.main.temp) + "°C";
document.querySelector(".humidity").innerHTML = data.main.humidity + "%";
document.querySelector(".wind").innerHTML = data.wind.speed + " km/h";

if(data.weather[0].main == "Clear"){
    weathericon.src = "images/clear.png";
}else if(data.weather[0].main == "Clouds"){
    weathericon.src = "images/clouds.png";
}else if(data.weather[0].main == "Rain"){
    weathericon.src = "images/rain.png";
}else if(data.weather[0].main == "Snow"){
    weathericon.src = "images/snow.png";
}else if(data.weather[0].main == "Drizzle"){
    weathericon.src = "images/drizzle.png";
}else if(data.weather[0].main == "mist"){
    weathericon.src = "images/clear.png";
}

    document.querySelector(".weather").style.display = "block";
    document.querySelector(".error").style.display = "none";
}
}

 searchBtn.addEventListener("click", ()=>{
    checkWeather(searchBox.value);
 });
```
### Tools and Platforms

- *VSCode*:

 A powerful code editor with built-in support for HTML, CSS, and JavaScript, along with extensions like Live Server for real-time testing.
 
- *Live Server*:

 A VSCode extension that launches a local development server, enabling developers to see changes instantly as they code.
 
- *Weather APIs*:

 Services like OpenWeatherMap provide free and paid APIs for accessing weather data.

### Conclusion

An API-integrated weather app is a practical and engaging project for developers to hone their skills in web development. By combining HTML, CSS, and JavaScript, developers can create a functional and visually appealing app that delivers real-time weather updates. Using tools like VSCode and Live Server streamlines the development process, making it easier to build, test, and deploy the app. This project not only demonstrates the power of APIs but also showcases the versatility of web technologies in creating modern, interactive applications.

# output screens :

