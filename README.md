# starbucks

A dataset of all Starbucks locations in NYC.

This repository aims to make this data available to open source location and map based projects and enrich it to make for a better user experience.

## How to contribute

1. Fork this repository and clone your fork onto your local machine
2. Select a Starbucks location from the ones available in `locations.json`
3. Make note of your selected location's `storeId` value
4. Navigate to <https://www.starbucks.com/store-locator/store/>`{storeId}` in your web browser of choice
5. In `locations.json`, create a storeHours key for your selected location with the value of a days of week object, and populate each day of the week with its opening hours according to the information in the location's page
6. Make a PR from your fork to this repository

Example:

```json
{
  "city": "Brooklyn",
  "name": "Target Brooklyn College",
  "country": "US",
  "longitude": -73.9472427368164,
  "latitude": 40.6312637329102,
  "storeId": 6551
}
```

Will become

```json
{
  "city": "Brooklyn",
  "name": "Target Brooklyn College",
  "country": "US",
  "longitude": -73.9472427368164,
  "latitude": 40.6312637329102,
  "storeId": 6551,
  "storeHours": {
    "sunday": "8:00 AM to 9:00 PM",
    "monday": "8:00 AM to 9:00 PM",
    "tuesday": "8:00 AM to 9:00 PM",
    "wednesday": "8:00 AM to 9:00 PM",
    "thursday": "8:00 AM to 9:00 PM",
    "friday": "8:00 AM to 9:00 PM",
    "saturday": "8:00 AM to 9:00 PM"
  }
}
```

## Attribution

This dataset is a lightly processed version of a [Socrata](https://dev.socrata.com) dataset originally scraped by Chris Meller. Underlying data is owned by [Starbucks](https://www.starbucks.com). Full dataset made available on GitHub by Michael McLoughlin.
