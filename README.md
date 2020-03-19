# Corona Virus Data Scraper API (COVID-19)
A simple API code that scrapes data from [Worldometers](https://www.worldometers.info/coronavirus/) website. It is useful to be used with other visualization tools.

# How to Run?

Clone this repo and go to the cloned folder
```bash
git clone https://github.com/farisalasmary/coronavirus-data-api.git
cd coronavirus-data-api/
```

Run the script

```bash 
python corona_api.py
```

# How to Use?

There are two API calls:

1- Get statistics for all countries
```html
http://0.0.0.0:1111/get_stats/
```
**Output**

```json
{
  "main_table_countries_today": {
    "Afghanistan": {
      "ActiveCases": "21", 
      "NewCases": "0", 
      "NewDeaths": "0", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "0.6", 
      "TotalCases": "22", 
      "TotalDeaths": "0", 
      "TotalRecovered": "1"
    }, 
    "Albania": {
      "ActiveCases": "57", 
      "NewCases": "0", 
      "NewDeaths": "0", 
      "Serious,Critical": "2", 
      "Tot Cases/1M pop": "21", 
      "TotalCases": "59", 
      "TotalDeaths": "2", 
      "TotalRecovered": "0"
    }, 
    "Algeria": {
      "ActiveCases": "42", 
      "NewCases": "7", 
      "NewDeaths": "1", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "2", 
      "TotalCases": "82", 
      "TotalDeaths": "8", 
      "TotalRecovered": "32"
    }
  },
  "main_table_countries_yesterday": {
    "Afghanistan": {
      "ActiveCases": "21", 
      "NewCases": "0", 
      "NewDeaths": "0", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "0.6", 
      "TotalCases": "22", 
      "TotalDeaths": "0", 
      "TotalRecovered": "1"
    }, 
    "Albania": {
      "ActiveCases": "57", 
      "NewCases": "4", 
      "NewDeaths": "1", 
      "Serious,Critical": "2", 
      "Tot Cases/1M pop": "21", 
      "TotalCases": "59", 
      "TotalDeaths": "2", 
      "TotalRecovered": "0"
    }, 
    "Algeria": {
      "ActiveCases": "36", 
      "NewCases": "14", 
      "NewDeaths": "2", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "2", 
      "TotalCases": "75", 
      "TotalDeaths": "7", 
      "TotalRecovered": "32"
    }
  }
}
```

2- Get statistics for a specific country

**Example:** get statistics of Saudi Arabia

```html
http://0.0.0.0:1111/get_stats/Saudi%20Arabia
```

**Output**
```json
{
  "main_table_countries_today": {
    "Saudi Arabia": {
      "ActiveCases": "232", 
      "NewCases": "0", 
      "NewDeaths": "0", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "7", 
      "TotalCases": "238", 
      "TotalDeaths": "0", 
      "TotalRecovered": "6"
    }
  }, 
  "main_table_countries_yesterday": {
    "Saudi Arabia": {
      "ActiveCases": "232", 
      "NewCases": "67", 
      "NewDeaths": "0", 
      "Serious,Critical": "0", 
      "Tot Cases/1M pop": "7", 
      "TotalCases": "238", 
      "TotalDeaths": "0", 
      "TotalRecovered": "6"
    }
  }
}
```
