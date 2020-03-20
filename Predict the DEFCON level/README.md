# Predict the DEFCON level

  Military conflict is an intense state of violence. In such situations, it is crucial for a nation to stay alert, cope with it, 
  and mitigate its implications. A country has set up the DEFCON (Defense Readiness Condition) warning system. This alert system is used
  to gauge the level of alertness of the defense forces. It consists of five levels of readiness for the military forces to be prepared   for the consequences of the conflict. The DEFCON system allows the nation’s forces to be a step ahead of its rivals.
  
  Given a synthesized data that can be used to build a model that can accurately predict the DEFCON level raised as a 
  result of the conflict. 
  
### Data Files:
  * train.csv - Contains the training data; 10001 x 12 (includes headers)
  * test.csv -  Contains the test data; 2501 x 11 (includes headers)
  * sample_submission.csv - example for submission format of Results.csv
  
### Data Description
  * Allied_Nations: The number of nations that have joined together as allies
  * Diplomatic_Meetings_Set: The number of meetings with the intent to resolve the conflict that is planned
  * Percent_Of_Forces_Mobilized: Same as the name of the variable
  * Hostile_Nations: The number of enemy nations that have allied together
  * Active_Threats: The number of situations or threats that require immediate attention
  * Inactive_Threats: The number of situations or threats being monitored for activity or escalation
  * Citizen_Fear_Index:	The percentage of citizens who fear catastrophic military conflicts
  * Closest_Threat_Distance(km): The closest threat to the border of the country in question
  * Aircraft_Carriers_Responding:	The number of aircraft carriers actively traveling towards a threat to neutralize it
  * Troops_Mobilized(thousands): The number of troops that are activated and responding to the threats
  * DEFCON_Level(target variable): A numeric scale of conflict 'seriousness' with 1 being the least serious and 5 being the most
  * ID:	An ID to aid a checker script
