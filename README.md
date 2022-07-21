
                 
Basic working of the application.
Basically the Starlink project has basic entities like ground stations,lower
earth satellites(LEO) and higher orbit satellites(GSO) . here we have 10
ground stations numbered 0 to 9 , 5 LEO numbered 0 to 4 and one GSO.
We are trying to get the shortest path for communication between two
ground stations.
We basically input few data from the user. First of all we need to get the
numer of messages to be communicated . Then the application asks for the
two ground stations ,the origin and the end ground station. Depending on
the inputs the program gives the output in a step by step manner for each
hop of the message. We have also handled all the cases of errors that are
posible using exception handling.
1)Classes

1) Starlink class : It is basically the driver class of the system. It nests all
other classes. It contains the global variables,other classes and
an interface.

2) Constellation class: It defines the arrays with list of ground stations and LEO
satellite.It also has a method called showConstellation that shows all the available LEO
satellites and ground stations

3) Satellite : Satellite class extends constellation class and has method
getNextId that can be used to add more layers to the application for further
use.

4)Communication interface: It is an interface that has a method called
sendMessage that acts an abstract function. This interface is implemented
in LEOSatellite class.

5)LEOSatellite class: This is the most important class of our application. It
implements the communication interface and also extends the satellite
class. It has overridden method send message and it finds out which LEO
satellite to send message from origin and which LEO to send messages for
end.


Then comes the main method which is the driver method of the entire
application. It takes input from the user for origin and end of the
message.The objects for the LEO satellite and constellation classes are
created here using which we have called their functions. We have handled
invalid inputs using error handling and also closed the scanner for
preventing memory leak.
Future work possible: This application can e extended for multiple
more layers of LEOs and also for interconnecting constellations to enable
interplanetary communication
