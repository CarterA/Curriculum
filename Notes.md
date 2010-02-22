#Important Notes about Object-Oriented Programming  
This document is going to serve as a reference for all of the topics I would like to cover in my curriculum. It will be added to and edited.  
##Object Basics  
An object is an abstract concept. The basic idea is that a program is layed out in a modular fashion, with different objects controlling different aspects of the program's behavior. Objects can talk to each other through methods or functions (terminology differs based on language). Objects have properties, which describe a characteristic of the object. These properties can be set by other objects. An object should always have a clear purpose:  keeping the modular design is crucial.  
##Model-View-Controller (MVC)  
MVC is a design pattern adopted by most modern object-oriented languages/APIs. It dictates what objects perform what tasks, and how they communicate with each other. Each language/API has specific guidelines relating to MVC, but the general rules are always present. These are the basic rules that it contains:  

* Every object must **either** be a Model, a View, or a Controller. Merging any of them defeats the purpose.   
* The Model represents knowledge, the View is a representation of that knowledge.  

###Smalltalk Interpretation of MVC  

* The Controller handles and interprets user input and updates the View and Model accordingly.
* The View **can** talk directly to the Model in order to update the displayed information.

###Cocoa Interpretation of MVC  

* The Model objects provide raw data, the Controller interprets it and readies it for the user, and the View displays the data to the user.  
* User interaction occurs in the View objects, never anything else. View objects communicate with the controller and tell it that interaction has occurred, and the View is then given information on how to update accordingly.  
* The Model objects must never directly communicate with the View objects. All communication must go through the controller.  

###Observers and Dependencies  
One important piece of the Smalltalk interpretation of MVC is the way that the Model and the View communicate. It is widely accepted that the Controller should only update the Model, and the View should "observe" changes in the Model. That means that whenever a change is made, the View will automatically update to display the changes. In languages where this isn't supported, dependencies are used. Each Model object would have a list of dependent objects, and sends a message to each one every time a change is made. The basic idea is that of a notification sent whenever something changes.  

#Questions for Doug  

* What age should this be targeted for? A student will need to be able to think in logical sequences, and math knowledge is definitely required if you want to actually apply what you learn. Programming also requires the adoption of a very strict writing syntax, which may or may not be more difficult for younger age groups.  
* As you can see in the above description of MVC, there are two different interpretations of the meaning of the C. How should I go about teaching that?  
* What activities should I have for the students to do in order to grasp the concept, and how should I test them?