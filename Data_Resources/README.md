# Dataset Section

## Overview
This section of the repository focuses on the **Monthly Horoscope Dataset** created for the SoulBuddy project: "Personalized Astrology and Numerology Insights." The dataset is designed to simulate real-world astrological trends and personalized horoscope data, providing a robust foundation for meaningful analysis using LangFlow and DataStax Astra DB

---

## Python Script: `horoscope_dataset_gen.py`

### **Purpose**
The Python script `horoscope_dataset_gen.py` generates a realistic dataset of 300 samples simulating monthly horoscope data for different zodiac signs. 
The script ensures:
- Adequate dataset size for comprehensive predictions.
- Trends and biases reflecting real-world astrological themes.
- Clean and structured output in both CSV and JSON formats for ease of use.

### **How It Works**
1. **Zodiac Signs and Horoscope Attributes:**
   - **Zodiac Signs**: Aries, Taurus, Gemini, etc., covering all 12 signs.
   - Horoscope metrics include:
      - **Career Insight**s: Predictions about professional growth.
      - **Relationship Insights**: Guidance on love and family.
      - **Health Tips**: Recommendations for well-being.

2. **Dataset Attributes:**
   - **Sign_ID**: Unique identifier for each zodiac sign.
   - **Zodiac_Sign**: Name of the zodiac sign (e.g., Aries, Taurus).
   - **Month**: Month for which the horoscope applies.
   - **Flower, Gemstone**: Corresponding flower and gemstone for the zodiac sign and month.
   - **Predictions**: Detailed horoscope covering career, relationships, and health.   

3. **Output:**
   - A structured dataset saved as `monthly_horoscope_data.csv` and `monthly_horoscope_data.json`.

### **Key Trends Introduced**
   **Zodiac Sign-Specific Bias**: Certain signs (e.g., Leo, Scorpio) may have predictions emphasizing particular strengths or challenges.
   **Monthly Themes**: Each month aligns with general astrological trends, such as eclipses or retrogrades.
   **Personalized Elements**: Flower and gemstone recommendations are tailored to the sign and month.

---

## Expected Insights
When the dataset is analyzed, these insights are expected:

1) **Horoscope Trends by Zodiac Sign:**

   - Leos may exhibit themes of leadership and social success in specific months.
   - Pisces predictions often emphasize intuition and emotional balance.
2) **Monthly Guidance:**

   - Certain months align with higher energy for career advancements (e.g., January, August).
   - Romantic opportunities may peak during months like February and July.
3) **Gemstone and Flower Relevance:**

   - Gemstones such as Ruby for July and Emerald for May offer unique spiritual benefits.
   - Monthly flower recommendations add a symbolic touch to horoscope insights.


---

## Real-World Alignment Efforts
To ensure the dataset aligns with real-world astrological practices:

1) **Astrological Patterns:**

   - Predictions incorporate planetary movements and significant events (e.g., Mercury retrograde).
   - Seasonal themes are reflected in career and relationship guidance.

2) **Personalized Accuracy:**

   - Flowers and gemstones are mapped according to traditional astrological associations.
   - Predictions are generated within the scope of widely accepted astrological interpretations.

3) **Comprehensive Dataset:**

   - 300 samples ensure broad coverage across zodiac signs and months for statistical significance.
---

## File Outputs
- `monthly_horoscope_data.csv`: A CSV file containing the dataset.
- `monthly_horoscope_data.json`: A JSON file containing the same dataset for flexibility in usage.

---

## Conclusion
This dataset forms the foundation for meaningful insights into personalized astrological and numerological predictions. By embedding traditional astrological practices and realistic biases, it ensures alignment with actual horoscope interpretations, making it an effective tool for analysis and personalization in the SoulBuddy project.

