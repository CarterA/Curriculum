##Day One - Teacher's Guide  
Begin the class by posing the questions:  "Have you ever wondered how apps are created? How games are made?" Some students may know that it has something to do with code. Some may have already created games using game creation software. Next you should introduce them to a few iPhone apps (see the list in the "Model-View-Controller:  An Overview" section), try and get a bit of a "wow" factor in, or at the very least some amusement. Make sure you engage everyone during this early time, getting students excited is crucial to success.  

###Object-Oriented Programming:  An Overview
You will need to cover the following points:  

* An object is an abstract concept. The basic idea is that a program is layed out in a modular fashion, with different objects controlling different aspects of the program's behavior.
* Objects can talk to each other through methods or functions (terminology differs based on language).
* Objects have properties, which describe a characteristic of the object. These properties can be set by other objects.
* An object should always have a clear purpose:  keeping the modular design is crucial.  

An excellent way of demonstrating the concept of an object is to use the example of an army in a campaign. There are several different groups of soldiers, and each group has a specific function. For instance, one group is tasked with gathering intelligence and reporting it back. Another group is assigned to attacking to the West of their current location, and yet another group is responsible for protecting the Northern flank. A final group is stationed on the South coastline of the area, prepared to defend if necessary.  

In this example, each group of soldiers represents an object in an application, which is represented by the army as a whole. In this case, the application's purpose would be to win a war.  

###Model-View-Controller:  An Overview  
You will want to introduce MVC as a "paradigm", or a "design pattern". It is a way of laying out the code for a program so that it is organized, efficient, and modular. It is the standard design pattern for most object-oriented languages. You will need to cover the following points:  

* Every object must **either** be a Model, a View, or a Controller. Merging any of them defeats the purpose.  
* The Model represents data, the View is an interpretation of that data.  
* The Controller handles and interprets user input and updates the Model accordingly.  
* The View polls the Model for changes, and updates itself accordingly.  

To demonstrate MVC, you can use the following iPhone apps:  

* Bubblewrap (Model:  List of bubbles, their positions, and whether or not they are popped; View:  The image of bubbles on the screen; Controller:  The code that takes the position of a tap, figures out which bubble was hit, and then sets that bubble to popped in the model)  
* Mover (Model:  List of files on disk and available to user; View:  Flat view on screen with files displayed as small items; Controller:  The interpreter of taps and drags that tells the filesystem what to send where, and the receiver of files sent by other devices which are then stored in the model)  
* Notes (Model:  Database of notes made by the user; View:  A list of the titles of notes which can be tapped and expanded to show their full content; Controller:  The code that interprets taps on either a note or the plus sign button and updates the model accordingly)  
* Photos (Model:  Database of photos taken on the phone; View:  The expandable list of photos and their albums; Controller:  The code that tells the model when to provide a big version of a photo, a thumbnail, or other information)  

Students may try to call back to the army analogy in order to understand MVC. This may not be beneficial, as it is somewhat difficult to connect the two. The only thing to remember here is that every object has a very specific purpose, and shouldn't have functions that overlap others. This does **not** mean they are entirely independent:  each object should absolutely depend on other objects for extended functionality. The key is that it is a modular design, and can easily be broken down into pieces based on the different functions of the application.