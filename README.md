# Travel Price Alert System

This Python script is designed to alert users about low prices for flights to various destinations. It utilizes data from a spreadsheet, checks for flight prices, and sends notifications to users if a lower price is found.

## Requirements

- Python 3.x
- `data_manager.py`: Module for managing destination data.
- `flight_search.py`: Module for searching flight prices.
- `notification_manager.py`: Module for sending notifications.

## Usage

1. Set the `ORIGIN_CITY_IATA` variable to the IATA code of the origin city (e.g., "LON" for London).
2. Ensure the required modules (`data_manager`, `flight_search`, `notification_manager`) are available and properly configured.
3. Ensure there is a google sheet with columns `City`, `IATA Code` and `Lowest Price` and the sheet is connected to `sheety` for api calls
4. Run the script.

## Overview

1. Retrieves destination data from a spreadsheet using `data_manager`.
2. If IATA codes are missing, obtains them using `flight_search` and updates the spreadsheet.
3. Checks flight prices for each destination within a specified timeframe.
4. Sends email notifications to users if a lower price is found.

## Code Structure

- `data_manager`: Manages destination data and user information.
- `flight_search`: Searches for flight prices using an API.
- `notification_manager`: Sends email notifications.
- Main Script:
    - Retrieves destination data.
    - Checks and updates IATA codes if necessary.
    - Defines destinations with their IDs, cities, and lowest prices.
    - Checks flight prices for each destination.
    - Sends email notifications if a lower price is found.

## Example Usage

```python
python travel_alert_system.py
```

## Note
- Ensure API keys and necessary configurations are set up for flight_search and notification_manager.
- The script uses the datetime module to calculate the timeframe for checking flight prices.
- Adjust the timeframe and other parameters based on specific requirements.
