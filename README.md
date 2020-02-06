# CSQ-Project
CSQ System: A System to Support Constrained Skyline Queries on Transportation Networks

For the CSQ system, we preload the points of interest and the public transportation networks in three cities, including New York (NY), Los Angeles (LA), and San Francisco (SF). The city is a place where the query point resides in

We provide 4 different ways to let users input a query point. 

In the first way, a user can type the address of the query point, the second way, a user can select the object from the list of POIs, which are already loaded, the third way, the system directly utilizes the current location of the user. The user just needs to click the GPS logo and the last approach, a user selects a query point by directly clicking a place on the Google map. 

After a user selects a query point, the user can choose different methods to find the CSQ solutions. The system implements three approaches that we proposed earlier this year. 

The first two methods, namely Mixed Approximate Method and Ranged Approximate search, are heuristic methods to return approximate solutions. The Ranged Approximate search finds approximate solutions by limiting the distances from the query point to the starting network node and the distance from the ending network node to the skyline solutions to be within a given threshold. The Mixed Approximate Method further limits the graph paths in the skyline answers. 

The last method is an exact search method. It can find all the skyline answers. However, it is very slow, and the result set is huge. Thus, it is not practical to be used in real life. 

For all three methods, we can limit the number of bus stops in the network path. 

After selecting a query point and the search method, a user needs to specify the values for 3 optional parameters.  
1)	The first parameter is a distance threshold denoting the maximum distance that the user’s willingness to walk from the query point to the bus stop and from the bus stop to the CSQ answer. 
2)	The second parameter is the number of bus stops or metro stations denoting the maximum number of stops that a user is willing to accommodate. 
3)	the third parameter is the POI type of the CSQ answer. 
