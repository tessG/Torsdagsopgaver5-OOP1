### Exercises in  OOP 

Today's exercises should be performed in IntelliJ. 
You are to create a new project titled "OOP1". 
For each task below, you must create a new package in the project's src directory. Name it accordingly to the task, e.g. "Task1". 
In each package, create a Main.java with a static Main method which will be used to call the methods required to complete the tasks. 

Please note, that it is quite unusual to have a Main class in each package, yet this is done so for the sake of the exercise.

## Task 1: Cars and drivers
This task is excersice in the syntax of writing entity classes, and how to connect those by assigning instances of one class to instance fields of another.

1.a Create a Driver.java class with the following private fields (use appropriate types): 
- Name
- Age

1.b Create a constructor that populates all the fields above. 

1.c Create a Car.java class with the following private fields (use appropriate types):
- make
- model
- year
- bodyStyle
- driver

1.d Create a constructor, that populates all the fields above, except the Driver. 

1.e A car is not instantiated with a Driver, so we need another way to assign and un-assign a driver to a car: create getter and a getter methods for the Driver variable, of the Car class.

1.f override the toString method in the Car class, returning:
     "Make: "+make+". Model: "+model+ " ("+ year + "), BodyStyle: "+bodyStyle

   <details>
        <summary>
           Help:
        </summary>
         <a href="https://www.geeksforgeeks.org/overriding-tostring-method-in-java/">read about overriding the toString method</a>
    </details>  
     
1.g override the toString method in the Driver class, returning: 
    " is driven by "+name

1.h In the main method, instantiate a new Driver, populating the fields with your own name and age. 

1.i In the main method, instantiate a new car, populating the field with whatever values you see fit. 

1.j In the main method, assign the driver to the car created, using the setter method created in step 1.e

1.k print the toString method of the car you've created followed by the toString method of the driver. 

1.l In the main method, create yet another car and assign the same driver to this car. 

1.m repeat the step 1.k for the new car created in 1.l. 


## Task 2: Buildings and Rooms
This task i an excersice in accessing fields in objects within objects. You will create a building with some rooms. Each room will have some attributes which you will access(read the value of) in order to draw conclusions about the building in which the room is placed.

2.a Create a Room.java class with the following fields (use appropriate types and make them private): 
- numberOfDoors
- numberOfLamps
- numberOfWindows

2.b Create a constructor that populates all the fields above.

2.c As the fields of the Room class are private, create getters() for each of them, 

2.d Create a Building.java class with the following fields (use appropriate types):
- Rooms (make sure to use the \'final\' keyword here as this variable should never change once it has been assigned a value)
   <details>
        <summary>
          Hint  
        </summary>
        This should be a datatype that can hold multiple objects of type Room.
    </details>

   <details>
        <summary>never heard about  <code>final</code>?
        </summary>
         <a href="https://www.geeksforgeeks.org/final-keyword-in-java/">read about the final keyword</a>
    </details>
- numberOfBathrooms
- numberOfFloors
- isOfficeBuilding

2.e Create a constructor that populates all the fields above. 

2.f As the fields of the Building class are private, create getters() for each of them.
    
2.g In your main method, instantiate at least three different rooms. 

2.h Add the three rooms to a collection (preferably of the same data type used for the "Rooms" field in your Building.java class).

2.i In your main method, instantiate a new building.

2.j create a static method in Main, countLampsInBuilding, that takes an object of type Building, and returns the total number of lamps in the entire building.
 <details>
        <summary>
           Hint
        </summary>
         You will need to have a loop in the body of the method that looks at each room in the building to add the number of laps in each room.
    </details>

2.k create another static method in Main, isNormal, that takes an object of type Building. The method should return true if the Building's numberOfFloors is greater than its number of Rooms. If not it should print "This is an odd building" and return false.


## Task 3: (language switch alert) ArrayList og Objekter

3.a Lav en klasse, Customer, med attributterne:
String firstName
String lastName
String username
int id

3.b Klassen skal have en konstruktor der tager et parameter med kundens navn og brugernavn. Giv klassen en toString() metode, der printer kundens detaljer pænt ud. Gør alle klassens felter private, og tilføj getters().

3.c Skriv en Main klasse med en main metode, hvor der oprettes en beholder af typen ArrayList, som du kalder 'customers'. Denne skal være erklæret som static global variabel - dvs tilgængelig udenfor main metoden. I customers skal du placere 6 instanser af Customer typen. 
(Du kan oprette instanserne først, og så add'e dem til array'et. Du kan også adde og instantiere i samme linie.)

3.d Skriv en metode i Main kaldet printCustomers(), hvor du printer alle kunderne ud ved at gennemløbe 'customers' med et ’for each’ loop. Test metoden fra main ved at kalde den.


## Task 4: Dokumenter koden
Denne opgave forudsætter at du nu har kodet Task2 og Task3 og placeret koden til hver opgave i en folder under src med navne Task2 hhv. Task3

4.a Lav en ny folder i projektet - på samme niveau som src folderen - som du kalder "Documentation".  

4.b Opret en PlantUML fil i folderen, med navnet "CarsAndDrivers" - vælg diagramtypen 'object'.

4.c Du kan vælge helt at slette den skabelon kode der står i dokumentetet, eller rette det til. Skriv plantUML kode, der afspejler den kode du skrev i Task2, og som ligger i src/Task2. 
(Der bør være 3  klasser i folderen, Task2: Main, Car og Driver).
For hver klasse skal diagrammet vise en kasse med klassens navn samt klassens:
 -  felter: access modifyer, type, navn
 -  metoder: access modifyer, returtype, navn, parameterliste
 
4.d Få diagrammet til at vise relationer mellem klasserne ved at tegne linjer mellem kasserne:
 <details>
        <summary>
           Hint
        </summary>
         Et 'has-a' relationship vises sådan her:
          <code>Car *-- Engine</code> <br>
         <i>(En bil har en motor)</i>
    </details>

4.e Gentag processen fra step 4.b - 4-d, dog skal filen denne gang hedde "BuildingsAndRooms" og den kode der skal dokumenteres er den du har skrev i Task3


