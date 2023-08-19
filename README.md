# esp8266-gcal-worker

An ESP8266 with LEDs that show upcoming meetings.

This project consists of:

- an ESP8266 with some LEDs and resistors
- a cloudflare worker that reads your calendar events

## Setup

### Cloudflare Worker

See [cf-worker/README.md](cf-worker/README.md).

### Google Cloud

For each account that you want to access calendars for, you need to:

- Create a new project
- Enable Calendar API at https://console.cloud.google.com/apis/library/calendar-json.googleapis.com?project=$PROJECT_ID
- Create API credentials at https://console.cloud.google.com/apis/credentials/wizard?api=calendar-json.googleapis.com&project=$PROJECT_ID
- Add scope `/auth/calendar.events.readonly`
