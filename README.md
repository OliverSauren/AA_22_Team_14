**# AA_22_Team_14

Description of tasks
  1.	Data Collection and Preparation
      Task: Clean the dataset for later use. Briefly describe how you proceeded and how you dealt with possible           missing/erroneous data.

      -	Dataset Boston 2017
      -	Clean:
          o	No missing values (search for blanks) → check for impact, but should be fine
          o	Check for correct formats
          o	Start time has to be smaller than end time
          o	IDs (bikes and stations) have to be numerical
          o	Station name has to be a string and a proper name for a station (check for irritating values)
      - Report (Patrick)
      - Consolidation of cleaning codes (Patrick)
      - Check for NaN values (Oliver)
      - Check for count of station id < 10 -> Check for usefulness (Oliver)
      - Pricing data (Oliver)
      - What to do with data from January and February 2017 (Season open was on the 27th February 2017
      
      -	Weather dataset should be fine
      -	Hint: additional data, such as the locations of individual bike stations may be available from the operator               websites. You can incorporate those in your analyses (e.g., for visualization purposes) for extra                   marks but it is not a requirement.

  2.	Descriptive analytics
      Steps to follow:
        a. Temporal Demand Patterns and Seasonality: Demonstrate how fleet usage varies during a day, a week and                the year. What patterns do you observe? Explain.
                -	Filter for (1) daytime, for (2) weekday and for (3) weeks and months
                -	Check for demand/usage on holidays and during typical vacation times
                -	Check for Boston-specific tourist data

        b.	Geographical Demand Patterns: Which stations are particularly popular and which are not? Provide a                   rationale as to why you observe these patterns.
                -	Map of Boston: For the rationale, use a map check where the stations are placed to find 			reasons
                -	Check for differences between the two groups of the 20 most popular and the 20 least popular
                -	Check for similarities within the two groups and identify/make assumptions regarding                                 characteristics
                -	Cumulative demand/usage of the two groups
                -	Check for frequently connections between two stations (are bikes used to cover missing 				public transportation or even instead of public transportation?)

        c.	Key Performance Indicators (KPIs): Define at least (!) three KPIs that you would include in a dashboard             for a fleet operator. These KPIs must provide an immediate overview of the current fleet operations and             how well the fleet is doing in terms of utilization, revenue, coverage and/or other business-related                 aspects. Briefly explain the rationale behind selecting each KPI, explain why you have chosen it and                 where needed provide references. Calculate hourly values for the selected KPIs for the city/year in your             dataset and visualize them over time. Which trends do you observe? How do you explain them?
                1)	Average usage/utilization rate
                2)	Total / absolute number of rides
                3)	Ratio of customers and subscribers / Shares of customers and subscribers
                4)	Weather data as an indicator (explanation of usefulness for the overall business, e.g.                               implementing bike service periods)

                - Long-term KPI for the part “limitations”: Check for differences/time between end and start time to                   predict when a bike is broken /needs fixing
                - Pricing data to add as an extension of the dataset
                - Distances between stations to calculate revenue per mile

    3.	Cluster analysis
        Based on the bike rental demand patterns, can you identify clusters of trip types and/or customer types? How         would you label these clusters? Can you cluster the locations based on their demand pattern?
          - Commuting people
          - Locations used for commuting
          - Day trips
          - Differentiate between living and working areas
                •	Limitation: No more detailed information on these areas because of lack of knowledge of the                         city/its infrastructure or a lack of data on this topic
          - “Overused” and “underused” locations: Check for (average) utilization rates → Could indicate an increase             or decrease of bikes needed

    4.	Predictive Analytics
        Future demand is a key factor that will steer operational decision making of a shared rental network. As a           data scientist it is your responsibility to facilitate this type of decision support. For the purpose of             this assignment we will be interested in forecasting total system-level demand in the next hour. To do so,           develop a prediction model that predicts bike rental demand as a function of suitable features available in         or derived from the datasets (incl. the weather data).
        
         – Feature Engineering: 
         Develop a rich set of features that you expect to be correlated with your target. In this process you can            draw on your domain knowledge and/or conduct additional research around the topic of demand prediction in            vehicle rental networks. Justify your selection of features.
          
            o	Precipitation
            o	Temperature
            o	Daytime
            o	Week day
            o	...

        – Model Building: Select three regression algorithms that are suitable for the prediction task at hand.               Explain and justify why you selected the three algorithms and describe their respective advantages and               drawbacks.
        
        → Everybody checks the lecture slides (and maybe required/additional readings)

        o	Briefly explaining why we might not use other algorithms than the selected (especially if they’re used               quite often / if they’re quite popular)
        o	Linear regression
        o	Check for more…
	
        – Model Evaluation: How well do the models perform? Evaluate and benchmark your models’ performance using             suitable evaluation metrics. Which model would you select for deployment?
            
              Possible evaluation metrics:
                - To be looked up in the lecture slides

        – Outlook: How could the selected model be improved further? Explain some of the improvement levers that you                    might focus on in a follow-up project.
                    
                      - Long-term KPI for the part “limitations”: Check for differences/time between end and start                           time to predict when a bike is broken /needs fixing
                      - Pricing data to add as an extension of the dataset
                      - Distances between stations to calculate revenue per mile
                      - Differentiate between living and working areas (Limitation: No more detailed information on                         these areas because of lack of knowledge of the city/its infrastructure or a lack of data on                         this topic)
                      - Data of previous years to be included (even though this limitation is just due to the task)
                      - Personal user data like age, gender etc.
                      - Data on the subscription type
                      - Data on customers (to calculate e.g., number of rides during the year)
                      - Reason/Kind of usage (commuting, trips etc.) (if reliable and useful because provided by                             customers → checking for correctness necessary) 
                      - Data on how much bikes are available/placed at a certain station to predict “Overused” and                           “underused” locations: Check for (average) utilization rates → Could indicate an increase or                         decrease of bikes needed
                      - More and more detailed weather data (amount of rain, speed of wind)
                      
Notes and tips
    1.	Make generous use of visualization techniques to clearly illustrate your findings and present them in an appealing fashion.
    2.	Evaluate your methodology and clearly state why you have opted for a specific approach in your analysis.
    3.	Relate your findings to the real world and interpret them for non-technical audiences (e.g. What do the coefficients in your regression model mean? What does the achieved error mean for your model?, etc.)
    4.	Make sure to clearly state the implications (i.e. the ”so what?”) of your findings for managers/decision makers.
 
Main deliverable of this group project you are expected to submit the following documents:
    1.	A 5-page report (excl. figures, tables, cover page, executive summary, references and appendices) in pdf-format detailing your answers to task 1-4 as well as any additional findings. The report should include:
            o	Cover page with informative title, team number and member names
            o	One-page executive summary: summarizes the entire report for a non-technical manager (the business problem, data, the analytics solution, implications and recommendations)
            o	Problem description (business goal and data mining goal)
            o	Data description
            o	Brief data preparation details (how your data were created from the raw data) and key charts. Details               can be provided in an Appendix.
            o	Data analytics: Analytical methods applied (with sufficient detail and screenshots; use Appendix if                 needed) and appropriate performance evaluation (proper choice of measures, benchmarking).
            o	Conclusions (advantages and limitations) and business recommendations
    2.	A well-structured git repository including your coding work in the form of annotated Jupyter notebooks               (.ipynb format) detailing your analysis and including executable Python code. 
        To share the github repository please include the link in your report. Also make sure to set the visibility         of your repository to private while you are working on your code and only publish it shortly prior to your           submission.

    3.	A 1-page supplementary document (not counting toward the page limit) detailing the individual contributions         of each team member (i.e. who did what).

![grafik](https://user-images.githubusercontent.com/104833634/211152755-afb1810e-4b5d-4494-9c22-a141ed284643.png)



**
