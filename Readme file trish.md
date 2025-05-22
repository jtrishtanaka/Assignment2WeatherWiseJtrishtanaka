
# Trisha's Weather Advisor

Welcome to **Trisha’s Weather Advisor** — a smart, interactive weather forecast terminal app built in Python. It combines the power of live API data, visualisations, and motivational energy to help you check and understand the weather clearly.

---

## Requirements & Installation

Before you run the app, make sure you have Python 3.7+ installed.

### Step 1: Install Required Packages

Open your terminal or command prompt and run:

```bash
pip install pyinputplus matplotlib requests
```

---

## How to Run

Save the script as a Python file (e.g. `trisha_weather_app.py`) and run it using:

```bash
python trisha_weather_app.py
```

You'll be greeted by an interactive command-line menu.

---

## Features

Here’s what this app can do:

- Check today’s weather for any city worldwide
- Visualise the 3-day forecast (temperature & rainfall graphs)
- Ask natural questions, like:
  - "What's the weather in Port Louis tomorrow?"
  - "Is it going to rain in Curepipe the day after tomorrow?"
- Motivational quotes to brighten your day, no matter the weather

---

## How It Works

### 1. Weather API Integration
The app fetches real-time and 3-day forecast weather data using the **wttr.in** API.

### 2. Data Visualisation
With **Matplotlib**, the app graphs:
- Daily high and low temperatures
- Midday rainfall predictions

### 3. Natural Language Parsing
The app uses simple regex to understand questions like:
> “What’s the weather in Paris tomorrow?”

It figures out:
- The city
- The day (today, tomorrow, day after)

And gives you a clear forecast.

---

## App Demo Menu

Once running, you'll see this menu:

```
Welcome to Trisha’s Weather Advisor

1. Check today’s weather
2. Visualise 3-day forecast
3. Ask a natural question (e.g. "What's the weather in Curepipe tomorrow?")
4. Exit
```

---

## Example Questions You Can Ask

- "What's the weather in Curepipe?"
- "Will it rain in Flic-en-Flac tomorrow?"
- "Is it hot in Port Louis the day after tomorrow?"

---

## Motivational Mode

Every time you check the weather or view a forecast, you’ll receive a random, feel-good quote just for you. A little boost goes a long way.

---

## Troubleshooting

- **API Timeout/Error**  
  Check your internet connection or try again later.  
- **Missing Data**  
  wttr.in might not return forecast data for small towns. Try a nearby city.

---

## Behind the Scenes

Key Python Libraries Used:
- `requests` – To fetch weather data
- `matplotlib.pyplot` – To create visual graphs
- `pyinputplus` – To build clean, interactive CLI menus
- `re` – For parsing natural language queries

---

## Created by

**Tanaka “Trish” Jera**  
Curtin University, Mauritius
