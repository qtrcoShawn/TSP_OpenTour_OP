# TSP_OpenTour_OP
I do long distance motorcycle rallies.  Finding the best route from a list of GPS coordinates with point values FAST is part of the game.  This script takes the list of gps coords and pitches out to Google Maps API to make a Distance_Matrix.  Then this DM is run through Google ORTools to find a series of routes.

The first run through, we calculate the absolute minimum tour in any long distance rally.  That is, to run straight from the Start to the Finish and neglect picking up the reward/prize from any of the other nodes in the field available. This gives the min distance possible to travel.  

Then we run our first request through ORTools and we use a Max_Travel_Distance of 1,000,000 miles.  This pretty much guarantees we will have enough miles to visit 100% of the nodes from the field available.  

Then we iterate from the Max Distance to the Min Distance in 100 steps and ORTools generates all of the best routes from Max to Min.  

Then, as a long distance motorcycle rally rider, you have to decide based on your skillset and energy, how many miles you can physically ride.  Choose that route and you're well on your way to a Podium Iron Butt Rally finish.
