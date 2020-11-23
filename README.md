# Backend Challenge	

Hi,
Your challenge, if you accept, is to design and implement a place recommender service that would infer the N most likely places a user would like to get a wine recommendation from.

For this exercise you’ll have full ownership of a Google Cloud Project to help you in your development.

You can use any JVM language you want and use any library you want to complete this project

## Requirements

* All places must be queried from Google places API. Google Places have a type property. For this exercise, we’re only interested in `restaurant` and `liquor_store` types
* Each route has to be secured with authentication, you can use Firebase authentication to simplify development.
* The solution MUST be containerized and launchable using docker compose
* The data does not need to be persisted across restart.

### Build the following HTTP Api :

* 1 route to save a place a user visited

* 1 route to get a list of recommended place for a specific user based on current location
	* input: latitude, longitude, number of expected recommendations (N)
	* output: a list of recommended place to visit containing at least the name and the address of the place
		* if there are no visited places available, return a list of the closest restaurants and liquor store from the given location
		* if there is at least N-1 visited places in the history, return the (N - 1) last visited places and the closest restaurant or liquor store from the given location
		* else return all the visited places available and complete with the closest restaurant or liquor store from the given location

	* 1 route to get an ordered list of the number of visites per place accross all users. Each item contains the number of visits, the name and and the address of the place, and the list of items is ordered such that the most frequent visited place is listed first.

## What will you be evaluated on?

For us, quality matters more than quantity. We respect your time, so please only complete as much as you can in a reasonable time frame and we will continue our discussion should you be selected to come in for an interview.

## You’ll be evaluated on the following:

* Components have a single and clear responsibility
* Components are unit tested
* Code is easy to read
* Challenge does NOT have to be entirely finished
