---
title: "Before/After Examples: Weather App Improvements"
author: "Trisha"
format: 
  pdf:
    toc: false
    colorlinks: true
  docx:
    toc: false
    highlight-style: github
  html:
    toc: true
    toc-expand: 2
    embed-resources: true
---

# Before/After Example 1: Weather Data Retrieval Function

## Initial Prompt

```
Write a function to retrieve weather data from the wttr.in API for a given location.
```

## Initial AI-Generated Code (Before)

```python
def get_weather(location):
    import requests
    
    url = f"https://wttr.in/{location}?format=j1"
    response = requests.get(url)
    data = response.json()
    
    return data
```

## My Analysis of the Initial Code

- No error handling
- No input validation
- Raw response returned
- No timeout
- No documentation

## My Follow-up Prompt

```
Thanks for the starting point. I'd like to improve this function with:

1. Error handling for API failures and bad responses
2. Location input validation
3. A timeout parameter to prevent hanging
4. A way to process the response to return only essential weather information
5. Proper documentation with parameters and return values explained
```

## Improved AI-Generated Code (After)

```python
def get_weather_data(location, forecast_days=5, timeout=10):
    # See previous full version (omitted for brevity)
    pass
```

## Why This Prompting Strategy Was Effective

- Specific requests
- Introduced new functionality
- Asked for better documentation

---