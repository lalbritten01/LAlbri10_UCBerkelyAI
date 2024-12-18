Capstone Project: Internet Traffic Forecasting with the Hawkes Process

Introduction

This README file provides an overview of my Module 24.1 Capstone Final Project submission. The project centers on analyzing internet traffic data and applying various forecasting methods to determine if the data follows a predictable pattern. The primary focus is on the Hawkes self-exciting point process, an advanced forecasting method capable of real-time evaluation and assessment. Additional methods, including simple linear regression and Exponential Smoothing, are also employed for comparison.

The Jupyter Notebook containing the full analysis can be found in the following repository: https://github.com/lalbritten01/LAlbri10_UCBerkelyAI/blob/UC_Berkeley_Capstone_Final/HawkesProcessCapstoneFinal.ipynb.

Motivation and Context

Accurate forecasting of web traffic is crucial for large-scale internet companies to optimize infrastructure, improve service reliability, and reduce operational costs. Precise forecasts allow for proactive resource allocation, minimizing risks of over-investment or outages, and ensuring a seamless user experience. This project explores the challenges associated with internet traffic prediction and evaluates the strengths and weaknesses of different forecasting models, particularly the Hawkes Process.

Dataset Overview

The dataset used in this analysis spans 230 days of recorded internet traffic with an average of approximately 4,100 visits per day. This consistent trend serves as the foundation for exploring the feasibility of accurate forecasts.

Methods Evaluated

Hawkes Self-Exciting Point Process:

The Hawkes Process is notable for its ability to model events that influence future occurrences (self-excitation).

Forecast accuracy is evaluated using MAPE (Mean Absolute Percentage Error) and confidence assessments through the simulation distributions.

The associated compensator is used to further evaluate the Hawkes Process's goodness-of-fit.

Simple Linear Regression:

A traditional forecasting approach that assumes a linear relationship between time and internet traffic trends.

Exponential Smoothing:

A time series method that applies weighted averages of past observations to make forecasts.

Each model was trained on 7 rounds of 30 days of internet traffic data with the following 10 days serving as the holdout (OOT) dataset.

Key Findings

Hawkes Process Performance:

Across the 7 rounds of analysis, the Hawkes Process demonstrated a MAPE < 10% for predicting the next 10 days of traffic in nearly half the rounds.

When the Hawkes Process forecasts were evaluated through simulations, the distribution of simulation values provided additional insights:

In 10%-25% of simulations, predictions were within 10% error of the actual OOT data.

However, the simulation range often spanned from 0 to double the observed values, indicating variability in forecast confidence.

Model Comparisons:

No single model consistently outperformed the others across all 7 rounds.

Simple Linear Regression and Exponential Smoothing showed particular strength in months with clear linear trends.

The Hawkes Process, on the other hand, excelled in months where self-excitation patterns appeared to drive internet traffic dynamics.

Compensator Analysis:

The Hawkes Process compensator values, which evaluate the fit of the forecasted data to a Unit Rate Poisson Process, revealed that:

When compensator values displayed a linear trend, the Hawkes Process forecasts tended to be accurate.

In cases where the compensator did not follow a consistent trend, forecast accuracy was reduced.

Confidence Assessment

The Hawkes Process provides additional methods for evaluating forecast confidence beyond standard metrics like MAPE:

Empirical Probability: Derived from the distribution of simulation results, this metric estimates the likelihood of observing the actual OOT data.

Compensator-Based Analysis: By assessing the linearity of the compensator over time, researchers can validate the model's fit and identify deviations that may indicate forecast challenges.

Conclusion

This study highlights the potential of the Hawkes Process as a valuable forecasting method for internet traffic data, particularly when patterns exhibit self-excitation. The ability to evaluate model performance in real time through simulation distributions and compensator analysis provides unique advantages over traditional forecasting techniques.

While the simple linear regression and Exponential Smoothing models performed well in scenarios with clear linear trends, the Hawkes Process demonstrated its strength in capturing more complex, event-driven patterns. Future research could further refine Hawkes Process parameterization, particularly through methods like cross-validation or online learning, to optimize forecast accuracy over targeted time windows.

In conclusion, the Hawkes Process represents a promising area for ongoing research and development in forecasting applications. Its unique ability to assess model confidence and goodness-of-fit provides valuable insights that can inform infrastructure management strategies, ultimately contributing to improved efficiency and reliability for large-scale internet systems.

