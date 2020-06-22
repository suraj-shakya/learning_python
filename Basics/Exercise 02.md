# Exercise 02  
Create a python `RiskPredictor.py` file having followings: 

 1. function : prepareData
	 - Parameters
		 - Parameter 1 :
			 - Type : Positional 
			 - Name : PersonName
		 - Parameter 2 : 
			 - Type : Positional / Keyword
			 - Name : Natinonality
		 - Parameter 3 : 
			 - Type : Arbitary Keyword Arguments
			 - Name : place_visited
	 - Returns : Dictionary from the above information  
     
2. function : predictRisk
	- Parameters :
		- 1 : 
			- positional  / keyword 
			- type dicitionary 
			- Note : return value of function prepareData
		- 2 : 
			- Risk Zones
			- Type : lists
	- returns riskiness of that person based on the places s/he has visited. If a person has visited a place which is identified to be in risk zones, then the person should be quarantined for at least 14 days.


Create another file ```TestResult.py``` and import`RiskPredictor.py` and call the functions in this file and predict result.
