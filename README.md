ProgramExecution

$ sh ExecuteProgram.sh


Architecture and High-Level Design:-
--------------------------------------
This project is based on MVC architecture where controllers are named as services. There are basically three layers namely the business Layer which handle the queries and other action from the command line interface,  Second Layer is the Service Layer which interacts with the Third Layer which is also known as Data Layer. This architecture is mostly preferred when we need to incorporate a client-server system in the project. Also developed the Data Transfer Objects to communicate between the layers. Designed Custom Exceptions to handle the layer-wise Exceptions. Created Enums for imposing the constraints on the values entered by the user. 

Database and File Handling :-
--------------------------------------
For the database part, I have used File Handling to store the data of the spot and vehicle details into a CSV(ParkingReport.csv) file and update it accordingly. Another important aspect of storing the details of Occupied and Unoccupied Spot is to load the existing Parking Lot, so that in case of any system or external faults the application should be able to retain its previous state. Another file  (TicketCounter.txt) holds the value of the last ticket number generated and this helps in keeping the unique TicketNumber.


Nearest Parking Position : 
--------------------------------------
The Nearest Parking Spot is been achieved by implementing the feature of minHeap. To find the nearest parking spot, I have to create a Node that holds the parking id and distance from the entry point. The rearrangement of the tree structure in the MinHeap is done based on the distance attribute of the Node and when we extract the min distance spot it returns a Node which contains the ID of the Spot, complexity of extracting records becomes O(1). If we have N entry points then we need to create N min Heap to track the nearest position of the spot. Although In this particular project I have considered a single entry point therefore I have used a single minHeap to find the nearest Spot.

Use of Gradle : 
-------------------------------------
I have also used Gradle in order to create jar and class and to build the entire project.  

Menu System: 
---------------------------------------
In order to make the command line user-friendly, I have designed a menu system that lets you choose the operations to perform. Users will be able to move forward and backward into menus.
