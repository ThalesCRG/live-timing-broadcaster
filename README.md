# live-timing-broadcaster

#telemetry
The telemetry app uses data the 2021 F1 Game sends via UDP. It parses it and serves it on a WebSocket connection. 
The telemetry app is based on typescript.

#frontend
The frontend connects to the WS connection and displays data. There are two different views to the data. One View is for every viewer to get non-classified data like times or pitstopps.
The other view is for commentators of league races (or Engineers) to get a more detailed look on the race. There is information for damage or ERS left for every car.

If you want to ensure that only commentators can look into this data, you can use a Login. Users can be enabled, disabled, created or deleted on the /config route. 

#auth server
The auth server is used to ensure that only logged in users can see certain data. There is an REST API (Express) that connects to a mongoDB.

