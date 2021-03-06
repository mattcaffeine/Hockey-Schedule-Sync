# Sharks Ice Schedule Sync Tool

A quick and dirty sync tool that will pull in all the games scheduled for your hockey teams at Sharks Ice San Jose,
Sharks Ice Fremont, and the NCWHL and add them to a Google calendar.

## Dependencies / Setup

Requires python 2.x and [pip](https://pypi.python.org/pypi/pip)

Run the following command (may need to use sudo depending on your system).
> pip install --upgrade BeautifulSoup google-api-python-client pytz argparse

Open the _config.cfg_ file and edit the teams property for your particular rink (comma separated, as they appear on the stat page)

## Running

You'll need to obtain client credentials for the app -- [follow the instructions provided by Google](https://developers.google.com/api-client-library/python/auth/installed-app#creatingcred)
and put the credentials (renamed to client_secret.json) in the root of the project

Then just run
> python ScheduleRipper.py

The first run will prompt you for authorization to your google account and ask which calendar you'd like to sync the
events to.  Every run afterwards will use the stored credentials and settings to run without intervention (making it
usable for cron jobs)

## To do:

- Add a connector for Ice Oasis' Google Calendar