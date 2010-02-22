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

#Notes from my Interview w/Doug  

* To answer my first question, the curriculum should be loosely targeted at Sophomores in High School. Programming requires you to think in logical sequences, and have a good grasp of basic math. Sophomores are less distracted then Freshmen and will be easier to teach as well.  
* Because these are high school students, the curriculum needs to have a hook. Something displayed on the first day to gain interest and motivate the students to stay engaged in the class. The idea we came up with was a demonstration of 3 to 5 iPhone apps (because of their widespread popularity and implementation of the MVC paradigm).  
* The take-away from this class is the ability to layout a program using properly organized object-oriented paradigms. The students should also have a good understanding the the concepts of OOP, and how it can be applied. **Important Note:**  This curriculum will not attempt to teach the syntax of any particular programming language, as that is beyond the scope of a one-week intensive course.  
* We also layed out the week-long course, which is in the next section.  

#Course Schedule (Rough)  

* **Day One:**  The class will jump straight to displaying simple examples of iPhone apps using MVC. Some examples to use include:  
	* Bubblewrap (Model:  List of bubbles, their positions, and whether or not they are popped; View:  The image of bubbles on the screen; Controller:  The code that takes the position of a tap, figures out which bubble was hit, and then sets that bubble to popped in the model)  
	* Mover (Model:  List of files on disk and available to user; View:  Flat view on screen with files displayed as small items; Controller:  The interpreter of taps and drags that tells the filesystem what to send where, and the receiver of files sent by other devices which are then stored in the model)  
	* Notes (Model:  Database of notes made by the user; View:  A list of the titles of notes which can be tapped and expanded to show their full content; Controller:  The code that interprets taps on either a note or the plus sign button an d updates the model accordingly)  

	The rest of the class should be spent (time permitting) making sure that everyone understands MVC, and doing a worksheet where you are given an application example and three elements of the application's code, and the assignment is to label each element as model, view, or controller. A bonus problem might have an example with more pieces of code, to show that there are multiple types of each object. This should be homework if it isn't completed in class.  

* **Day Two:**  This class should begin by reviewing the homework (if any was assigned) and then move on to brainstorming ideas of apps the students would like to lay out. Each student will pick a single idea for an iPhone app and begin to flesh out the concept with their peers through collaboration. Students should be encouraged to choose a small, focused function for the app to perform. It can be made clear to them that the bigger their idea, the bigger their workload will be. This class should be spent with continued brainstorming and the filling out of the next worksheet, where their idea will be recorded. This worksheet *should* be finished in class, but can be assigned as homework if necessary.  

* **Day Three:**  On this day the students will begin the process of storyboarding their application idea. Each major screen that appears in the app should be diagrammed on the worksheets provided, and it is very important that for each one, they describe the model and controller's behavior. Help from the teacher during this process will probably be necessary, though collaboration between peers should also be encouraged as that is a major part of programming as a whole. Students should get as far on this as possible, and then complete it for homework.  

* **Day Four:**  This class will be a "think tank", involving all of the students. Each student will present their storyboard to the class, describing how the app feels to use and its core functionality. After each presentation students are invited to ask questions and push each other's thinking to better everyone's applications. Edits can and should be made to the storyboard during this class. A final product will be due at the end of the class. After class, the teacher must review the presented ideas and discard concepts that are too broad to easily create in a short timeframe. The remaining concepts will be used the next day.  

* **Day Five:**  The class will vote on their favorite app idea and that app will be developed (more on this later). The app can be reviewed one last time by the class and any last-minute changes can be made. After that is complete, or when there is an hour of class time left, the final assessment should be given. This should be timed and should not take longer than an hour. The grade the student gets on the final assessment is their grade for the whole class, unless the teacher chooses otherwise.