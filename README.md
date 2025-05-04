# Insurance Claim Predictions for Electric Vehicles

I’ve seen an increased amount of electric vehicles on the road in where I live, British Columbia, Canada, especially since the EV Rebate Program in BC initiated in 2011. Every vehicle must obtain at least a basic insurance through ICBC, the provincial corporation in BC providing vehicle insurance, and the insurance for EV has been traditionally operated and priced till now. Local residents, although enjoying government rebates, they suffer from higher than normal insurance premiums. 

The factors that make EV insurance premiums higher are their three-electrical systems: the battery management, motor control, and vehicle control. All of them contribute to the cutting-edge technology and convenience of EVs, but they make traditional insurance pricing extremely difficult. There are huge amounts of real-time risk that traditional insurance premium models won’t represent.

For example, for many Tesla owners, the risks are:
- Battery aging: Replacement costs of Tesla batteries typically range from $10,000–$20,000 (NimbleFins).
- Autopilot Accidents: Tesla reports 1 crash per 4.85M miles with Autopilot, although exact insurance claim percentages tied to Autopilot are not available (Tesla Safety Report).
- OTA Failures: Tesla recalled over 1.2 million cars for software issues, to offer OTA update fixes (CnEVPost).
  
Here is what's Limiting Traditional Insurance—and How We Plan to Make It Better:
- Static pricing model based on vehicle type and age, normally accessed once a year. We want to use real-time driver behavior, vehicle status and battery health data to set the premiums effectively. Those data can be updated at minute level.
- Risk factors only cover mechanical breakdown and collision. We need to include risks that arise from software, battery, charging and other new technologies. 
- The user interaction is limited to passive claims. We hope to introduce active warnings and suggestions based on real-time data to decrease the number of claims as well as enhancing safety experience for drivers.
  
Based on the above, I built a Dynamic Risk Assessment System for EV insurance based on Machine Learning techniques, to:
- Predict the probability of insurance claims over the next 12 months 
- Identify high-risk groups, and 
- Enable dynamic insurance pricing
  
And here are some highlights for Model Effectiveness, Value, and Interpretability:
1. Model Performance: Our machine learning model is highly accurate, with an AUC-ROC score above 0.82, verified using cross-time window validation to ensure consistency over time.
2. Business Value: It effectively identifies the users with highest risks—capturing over 65% of high-risk cases within the top 5% of predicted risk—using lift analysis to validate the model’s business impact.
3. Efficiency: The system delivers predictions in real time, with latency under 200 milliseconds, confirmed through rigorous stress testing to ensure fast response even under heavy load.
4. Interpretability: The model remains explainable, with over 80% of decision-making covered by key features, as validated using SHAP analysis.

Note: Due to the sensitivity of live EV data and limited access to company’s internal claims, the prototype was built using a Kaggle dataset sourced from Porto Seguro’s Safe Driver Prediction that reflects realistic insurance claim behaviors and demographic features without giving specific meanings of each variable. While not a direct feed from BC drivers, it provides a valuable foundation to validate the dynamic risk modeling framework.
In a real-world setting, the project could use data from Tesla’s vehicle logs, ICBC claim records, and sensor inputs from smart charging systems to support minute-level pricing adjustment and preventive warning systems for high-risk drivers.

