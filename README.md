## Flask Application Design

### Problem Statement
Develop a Flask application that notifies the user when the temperature in Jindabyne, Australia falls below 5 degrees Celsius 

### HTML Files

**index.html**
- Base template for the application.
- Contains a placeholder for the temperature display.

**temperature.html**
- Template that displays the current temperature in Jindabyne.
- Contains a button to subscribe to temperature notifications.

### Routes

**index.html**
- The default route that renders the index.html template.

**temperature**
- Route that retrieves the current temperature in Jindabyne from an external API.
- Renders the temperature.html template with the retrieved temperature.

**subscribe**
- Route that handles the subscription request.
- Saves the user's subscription information to a database or a persistent storage mechanism.

**notify**
- Route that asynchronously checks the temperature in Jindabyne and sends a notification to subscribed users when it falls below 5 degrees Celsius.
- Can leverage a background task scheduler or a dedicated thread for temperature monitoring.

### Implementation Details

- The application will utilize the OpenWeatherMap API to retrieve the current temperature in Jindabyne.
- Users can subscribe to temperature notifications by providing their email or phone number.
- The application will periodically check the temperature and notify subscribers via email or SMS when it drops below 5 degrees Celsius.