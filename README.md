# SPlus Parser

The [Ostfalia SPlus lecture schedule](http://splus.ostfalia.de) is complicated to use, due to the lacking responsiveness especially on smartphones. However there are some really good and easy to use calendar programs/apps. This project serves as a bridge between SPlus and those programs.

## Setup

### General

Run `npm install` to install the necessary dependencies.

### Google

Follow the steps provided by Google: https://developers.google.com/calendar/auth#OAuth2Authorizing
You will receive a `client_secret.json` file which contains your Google API credentials. Save this file as `etc/google/client_secret.json`.

Adjust `config.ts` so that it uses the `sinks/GoogleCalendarSink`. Then run `npm start` in a terminal, visit the printed link and paste the code that will be provided there into the terminal window. This will also store an access token in `etc/google/credentials.json` which consecutive runs will use instead of asking to visit any links or pasting a code.

### ICS

Adjust `config.ts` so that it uses the `sinks/IcalSink`. Run `npm start` to generate the calendar file.
