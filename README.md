
# OVERVIEW

## Business Problem

Your company is expanding in to new industries to diversify its portfolio. Specifically, they are interested in purchasing and operating airplanes for commercial and private enterprises, but do not know anything about the potential risks of aircraft. You are charged with determining which aircraft are the lowest risk for the company to start this new business endeavor. You must then translate your findings into actionable insights that the head of the new aviation division can use to help decide which aircraft to purchase.

# Business Understanding
As we expand into the aviation industry, I recognize the importance of thoroughly understanding the risks associated with purchasing and operating aircraft for both commercial and private enterprises. To ensure our success and minimize potential hazards, I will use the CRISP-DM methodology to systematically analyze aviation risks. My focus will be on identifying the aircraft with the lowest risk, predicting which models are more likely to be involved in accidents, and examining the environmental and operational factors that contribute to these risks.

To achieve this, I will gather and analyze data on aircraft specifications, safety records, incident reports, and more. By applying advanced modeling techniques, I’ll be able to provide actionable insights that will guide our decisions on which aircraft to purchase and how to operate them safely. Ultimately, my goal is to deliver clear, data-driven recommendations that will help us confidently enter the aviation industry while ensuring the highest level of safety and operational efficiency.

## Objectives
- To assess which aircraft makes present the least risk for our business operations.
- To determine the aircraft models that are more prone to accidents.
- To identify regions or environmental conditions where accidents occur more frequently, helping to inform our operational strategies.
- To evaluate whether it is wise to invest in amateur-built aircraft.
- To analyze the data and identify aircraft types with the lowest accident and incident rates.
- To uncover the major factors that contribute to aviation risks, such as weather conditions, flight phases, and aircraft age.
- To examine how the purpose of a flight impacts the overall risk level.

# Questions To Consider
* What specific criteria define "low risk" for aircraft, and how should these criteria be prioritized.
* How do environmental factors like weather and geography influence the likelihood of an accident for certain aircraft types?
* What impact does the purpose of the flight (e.g., commercial, cargo, private) have on the overall risk profile of different aircraft models?

# Sources of Data
I sourced the aviation accident dataset from Kaggle, specifically from the **Aviation Accident Database Synopses** by khsamaha. The dataset contains comprehensive records of aviation incidents and accidents, providing details like the aircraft make and model, injury severities, environmental conditions, and more. This dataset was selected because of its extensive coverage of aviation data, which allowed me to analyze patterns in accidents, evaluate risks associated with specific aircraft types, and assess environmental and operational factors. The dataset is publicly available and well-structured, making it an ideal choice for this project focused on aviation risk assessment. 



### Data Understanding and Analysis Overview

In this project, I focused on analyzing a dataset related to aircraft accidents, with various attributes such as aircraft make, model, accident location, weather conditions, and injury severity. My approach to understanding and analyzing the data involved the following steps:

1. **Data Cleaning**:
   - I addressed missing values in key columns like `Make`, `Model`, `Weather.Condition`, `Aircraft.Category`, and `Injury.Severity`.
   - I standardized specific values (e.g., converting "Unk" to "UNK") for consistency in columns such as `Weather.Condition`.
   - I replaced nulls with appropriate values (e.g., `Unknown`, `UNK`, or mode values) to prepare the data for further analysis.

2. **Feature Engineering**:
   - I simplified and standardized aircraft makes, focusing on the core manufacturer by cleaning up entries in the `Make` column (e.g., reducing entries like "CESSNA 172" to just "CESSNA").
   - I ensured that injury severity and fatality reporting were consistent, making clear distinctions between `Fatal` and `Non-Fatal` incidents for more accurate analysis.

3. **Exploratory Data Analysis (EDA)**:
   - I conducted descriptive statistics to explore the distribution of important variables like accident frequency, injury severity, and aircraft categories.
   - I visualized the distribution of injuries and accident severity using bar plots and other graphs to identify common patterns in the data.
   - I analyzed environmental factors such as weather conditions and flight phase to determine their contribution to accident likelihood.
   - I examined accident frequencies by `Make` and `Model` to identify high- and low-risk aircraft types.
   - I also looked into how the purpose of the flight impacts accident risk, helping me to evaluate safety considerations for different operations.

This analysis helped me build a foundation for predictive modeling and risk assessment, which will assist in identifying the safest aircraft for potential investment and operational decisions.


### Visualization Overview

Throughout the analysis, I created several visualizations to better understand the trends in the dataset and support the decision-making process. Here's a summary of the visualizations and how they contribute to making informed choices:

1. **Accident Frequency by Make and Model**:
   - I plotted bar charts to visualize the number of accidents by aircraft `Make` and `Model`. This helped me identify which aircraft are involved in the most accidents, which is crucial for determining high-risk models and potentially steering away from them.
  
  ![Top 20 Aircraft Makes by Number of Incidents](image-3.png)

2. **Accident Frequency by Purpose of Flight**:
   - This bar chart helped assess which flight purposes (e.g., commercial, private, training) have higher accident frequencies. By understanding which types of operations are riskier, I can make recommendations on whether certain aircraft should be avoided or specifically tailored for less risky flight purposes.

![Accident Frequency by Purpose of Flight](image-2.png)

3. **Weather and Environmental Conditions**:
   - I plotted the distribution of accidents across different weather conditions and flight phases. These visualizations highlighted how certain conditions (like `Adverse` weather) and flight phases (like `Landing` or `Takeoff`) contribute to higher accident rates, enabling me to assess environmental risks when selecting aircraft.

Each of these visualizations provided crucial insights into accident risk factors, helping narrow down which aircraft are best suited for investment, which operational environments need more caution, and how certain factors like weather and flight purpose contribute to risks.