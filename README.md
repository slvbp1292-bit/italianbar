<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# EspressoPredict: Smart Coffee Consumption Forecast for Italian Bars

Building AI course project

## Summary

EspressoPredict uses Machine Learning to forecast the daily number of coffee cups sold in an Italian bar. By evaluating key external variables—including weekly routines, weather conditions, and local events—the system provides bar owners with actionable sales predictions to optimize staff shifts and raw material inventory.


## Background

Running an Italian bar efficiently is notoriously tricky due to unpredictable, fluctuating crowds. 
 **Over-staffing and Waste:** Preparing fresh pastries and sizing staff for a slow, rainy day wastes money. Conversely, being under-staffed during a surprise city festival ruins customer experience.
 **Perishable Management:** Fresh milk and premium coffee beans must be managed carefully to preserve aroma and prevent waste.
 **Personal Motivation:** Hospitality is a cornerstone of the Italian culture and economy. Empowering traditional bar owners with simple, low-cost AI tools bridges the gap between historical craftsmanship and modern data-driven management.


## How is it used?

The solution is integrated directly into the bar’s digital point-of-sale (POS) system or opened daily as a predictive dashboard by the bar manager. 

**The Process:** Every Sunday evening, the manager updates the local weekly outlook (upcoming concerts, soccer matches, and weather forecasts). 
**Context:** The system outputs exact target counts for upcoming days, helping the owner order the correct kilograms of coffee beans and schedule barista shifts accordingly.
**Users:** Traditional café owners, bar managers, and supply chain operators. 

<img src="https://images.unsplash.com/photo-1514432324607-a09d9b4aefdd?q=80&w=600" width="400" alt="Espresso Machine">

### Code Example (Predictive Pipeline)
```python
import pandas as pd
from sklearn.ensemble import RandomForestRegressor

def predict_coffee_demand(weather, day_of_week, city_event):
    # Load previously trained model data structure
    # Dummy representation of the core prediction logic
    base_cups = 150
    if day_of_week in ['Saturday', 'Sunday']:
        base_cups += 60
    if weather == 'Sunny':
        base_cups += 15
    if city_event != 'None':
        base_cups += 45
    return base_cups

print(f"Predicted Cups: {predict_coffee_demand('Sunny', 'Saturday', 'Football Match')}")

## Data sources and AI methods
Feature Variables,Type,Example Values
Day_of_Week,Categorical,"Monday, Saturday, Sunday"
Weather,Categorical,"Sunny, Cloudy, Rainy"
City_Event,Categorical,"None, Concert, Football Match"
Coffee_Cups_Sold (Target),Numerical,"150, 215, 127"


## Challenges
Challenges
What it does NOT solve: The model cannot account for sudden internal business anomalies, such as a broken espresso machine, sudden staff sickness, or unprecedented economic strikes.

Limitations: Weather data relies heavily on forecast accuracy, which degrades beyond 3-5 days.

Ethical Considerations: The system must strictly be used to optimize operations and relieve workload pressure, never as an aggressive tool to unjustifiably cut employee hours or compromise fair hospitality labor contracts.

## What next?
What next?
The project could evolve by integrating live third-party APIs (e.g., automatically scraping local ticket sales, real-time weather feeds, and public transit schedules). To scale this into a commercial SaaS tool for small businesses, collaboration with UI/UX designers and POS (Point of Sale) system developers would be needed.

## Acknowledgments
Acknowledgments
Formatted following the official University of Helsinki Building AI course guidelines.

Machine Learning implementation inspired by the open-source community benchmarks on scikit-learn.

Cover image placeholder via Unsplash.
