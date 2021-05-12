# Sample demonstration of an Air Traffic Control

![image](https://user-images.githubusercontent.com/66550230/118014948-61e4e800-b371-11eb-98bd-6b5754cc02d3.png)

![image](https://user-images.githubusercontent.com/66550230/118015018-71643100-b371-11eb-8fb0-31a44f4c94a6.png)


This project is purely implemented using HTML5, Javascript and static JSON data holding a list flight schedules. Project uses

HTML5 audio
JSON array containing flight schedules
Standard Javascript and to add loops for continues execution it uses windows.setInterval
CSS for styling flight parking gates and runways.

Project shows how much we can achieve just with plain Javascript itself without using any third party frameworks.

Fundamentally windows.setInterval is used to continuesly parse the flight schedule and allocate Gates and Runways to the flights based on their schedule. there are multiple setIntervals to handle allocation and deallocation of runways and gates to the flights. Also it is used to move the planes from parking gates to runways.

This sample project demonstrate a sample implementation of Air traffic Control where flights are scheduled for a particular date and time and based on the schedule are allocated a gate for standby and a runway to take off.

There are parking 5 parking gates and 4 runways in the airport. Gate and Runway is allocated to a flight on first come first serve basis.

For a given flight, allocated Runway and Parking gate are shown in same color to make UI clear and explain whats happenning.

After a runway is allocated to a flight it is made next available after 2 minutes for simulation. After flight has departed and 2 minutes are over runway is made available again to next scheduled flight.

Total of 8-9 flights are set in JSON array and is made part of same HTML file ie flights are part of the HTML file itself and are not kept in separate JS file (just for demonstration)

## What is covered in the implementation

a. There are total of 8 to 9 flights , 5 parking gates and 4 runways. Each flight has a schedule ie date and time of departure, flight number, Begin and end destination etc.

b. When flight schedule is reached, planes are allocated to gates and Gates show the flight details and status.

c. If any runway is free , it is allocated to each ready flight on first come first serve basis. once runway is allocated , Gate and Runway are shown in same color coding so that UI reflect allocation clearly. Also runways are allocated for next 2 minutes for simulation.

d. When flights are ready for departure, planes are physically shown moving towards runways and then running for departure and ultimately flying away. After flight has departed runways are set free and are ready for allocation for next available flight.

This can be extended to any level where data can be fed to UI in realtime from backend services and UI can continuesly run. Also we can add flight arrival logic and any emergency landings as well. Feel free to clone repo and extend if you would like to for fun.
