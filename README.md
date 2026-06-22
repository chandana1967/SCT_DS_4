import pandas as pd
import matplotlib.pyplot as plt

# Sample accident dataset
data = {
    "Weather": ["Clear", "Rain", "Clear", "Fog", "Rain", "Clear", "Fog", "Rain"],
    "Severity": ["Low", "High", "Medium", "High", "Medium", "Low", "High", "Medium"],
    "Road_Condition": ["Dry", "Wet", "Dry", "Wet", "Wet", "Dry", "Wet", "Wet"]
}

df = pd.DataFrame(data)

# Weather distribution
df["Weather"].value_counts().plot(kind="bar")
plt.title("Accidents by Weather Condition")
plt.xlabel("Weather")
plt.ylabel("Number of Accidents")
plt.tight_layout()
plt.savefig("weather_accidents.png")
plt.show()

# Severity distribution
df["Severity"].value_counts().plot(kind="bar")
plt.title("Accident Severity Distribution")
plt.xlabel("Severity")
plt.ylabel("Count")
plt.tight_layout()
plt.savefig("severity_distribution.png")
plt.show()

print("Charts saved successfully!")