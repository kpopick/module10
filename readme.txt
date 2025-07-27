Name: Kristopher Popick kpopick1

Module Info: Module 10: Developer Operations (DevOps) | Assignment: Accessibility API | 27JUL2025

Approach:

wmata_api.py: Imports json, requests, and flask from Flask. Flasks is used to run the api.  Sets WMATA_API key and the URL to pull incident information from using the api key. Formats the headers and api to return data properly. The function is designed to retrieve incidents based on type (elevators or escalators), determining the difference by assigned unit type. First in the function is establishing a list named incidents to hold all incidents as they are pulled into the script. Next  a GET request is performed to pull in incident data using the wmata URL. These are returned in json format. The json data is then parsed into unit type from earlier and unit types are converted to lower case to prevent handling errors. A dictionary is then created so that each incident returned can store the station code, station name, unit type, and unit name. Each dictionary addition is the added to the incident list. The main executes and starts the api. 

test_wmata_api.py: imports app from wmata_api, json and unittest modules. Creates class WMATATest, setting up the unittest. the first function is to check for a 200 status code, ensuring connection was made to the server for each unit type (escalator and elevator). This uses the assertEqual to ensure the response equals 200. The next function checks to see if all necessary fields are returned to the script to feed the dictionary in the wmata_api.py script. The next function test the Flask app for escalators ensuring the server can be reached and tested to pull escalator information. The following function does the same except for elevators. The main runs the entire test. 



Known Bugs:  none