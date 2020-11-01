# NodeJS Booking App
An appointment booking server application made using Node JS. This application makes use of the Google Calendar API to create appointment timeslots on Google Calender. The appointment timeslots are 40 minutes in length, and a 5 minute break between each timeslot exists. The timeslots are defined from Monday to Friday, 9AM to 6PM.

The full application requirements are given below.

For a video tutorial on how to setup this application, see this video: https://youtu.be/dWip8MLvEWw <br>
For a video demonstration of this application, see this video: https://youtu.be/IS-V0Xmv1mw

<h2>Requirements:</h2>
<ul> 
  <li>All appointments are 40 minutes long and have fixed times, starting from 9–9:40 am. :heavy_check_mark:</li>
  <li>Ensure there is always a 5 minute break in between each appointment. :heavy_check_mark:</li>
  <li>Appointments can only be booked during weekdays from 9 am to 6 pm. :heavy_check_mark:</li>
  <li>Bookings can only be made at least 24 hours in advance.  :heavy_check_mark:</li>
  <li>Appointments cannot be booked in the past.  :heavy_check_mark:</li>
  <li>For simplicity, use UTC time for all bookings and days. :heavy_check_mark:</li>
</ul>

<h2>Application contents:</h2>

<h3>ReqHandlers Directory</h3>
<ul> 
  <li><b>GET-Handlers</b> - A folder containing the GET handlers used in the app.</li>
  <li><b>POST-Handlers</b> - A folder containing the POST handlers used in the app.</li>
</ul>

<h3>Utility Directory</h3>
<ul>
  <li><b>appUtil.js</b> - Provides functionality used throughout the code base, such as date calculation functions.</li>
  <li><b>gcal.js</b> - Utilises the credentials.json file to generate a token.json file. If a token.json file already exists, then an oAuth2 Client is generated and returned.</li>
  <li><b>requirements-validator.js</b> - Used to validate requests sent to the server.</li>
  <li><b>credentials.json</b> - Your credentials.json file used to authenticate the Google Calendar API used by this app.</li>
  <li><b>token.json</b> - The token file generated by gcal.js after authenticating your credentials.json file.</li>
</ul>
  
<h3>App Working Directory</h3>
<ul>
  <li><b>Node-Modules</b> - Generated when running 'npm-install'. A folder containing the npm modules used throughout the app.</li>
  <li><b>server.js</b> - The main server file that utilises express to start a web server.</li>
  <li><b>package.json</b> - Package.json file used with npm.</li>
  <li><b>package-lock.json</b> - Package-lock.json file used with npm.</li>
</ul>

Installation and Usage
----------------------
<h3>Instructions:</h3>
<ol>
  <li>Clone this repository.</li>
  <li>Visit https://developers.google.com/calendar/quickstart/nodejs to activate Google Calander on your Google Account and to generate a credentials.json file if you haven't already done so. Place your credentials.json file into the 'Utility' directory of this application.</li>
  <li>In the newly cloned repository, open your command line and run the 'npm install' command to download the required modules.</li>
  <li>Run the 'node .' command to run the server.</li>
  <li>The booking app is now ready. Try out the following REST requests below.</li>
</ol>

<h2>HTTP REST Routes:</h2>

    GET  /days?year=yyyy&month=mm
    
    GET  /timeslots?year=yyyy&month=mm&day=dd
    
    POST /book?year=yyyy&month=MM&day=dd&hour=hh&minute=mm

## License

NodeJS-Booking-App is copyright (c) 2019, Aryan Nateghnia <38933061+aryannateq@users.noreply.github.com>.

NodeJS-Booking-App is free software, licensed under the GPL, Version 3.0. See the
`LICENSE` file for more details.
