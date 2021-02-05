# Our objective

In this tutorial, I will be showing you how to create your very own “Hello, World!” application with Swift. It’s super simple and also can be kinda fun for those of you new to iOS programming.

You’ll learn how to create a project in Xcode and create an application that shows a “Hello World” greeting. When a user taps a button, the app will show a message. We will define a function and the function will be invoked when a button is clicked.

# Coding environment

If you want to develop and make iOS apps, you will need to download Xcode 10. Xcode is the IDE created by Apple that includes the tools, interface builder, editor, simulator, and test driven development we need to create our application in Swift. It’s great, powerful, minimalistic, and best part is we don’t really need anything else.

You do, however, you will need a Mac or computer running OS X to download the IDE. I would advise making sure you have enough space on your hardrive, as the only bummer is that it weighs in at a hefty 6 GB.
If you haven’t already, feel free to download it on iTunes or here on the developer site to follow along.

# Let’s get started!


Now that you have Xcode downloaded, let’s go ahead and open it up.



![xcode Install](https://user-images.githubusercontent.com/14343387/106898596-67031d00-671a-11eb-8170-44267c224a93.png)



Once the welcome message prompts up, click on “Create a new Xcode project.” Our Xcode project is the source for an app and it’s the entire collection of files and settings needed to create it properly.
Xcode provides us with many templates with built in methods for constructing different types of apps. For now, click on “Single View App.”




Make sure your options are left unchecked, and that the language is Swift.

# Navigating Xcode

The four main sections we will be working in are the Navigator, Editor, Debug Area and Utility Area.







As you can see, our project files are in the Navigation Area. Our interface buttons for our app will be designed in the Storyboard.swift file and our Swift code will be held in the ViewController.swift. Xcode already provided us with a View Controller project file to get started. For now, don’t worry about the AppDelegate.swift or other files.
# Creating the UI Design

Although you can code the interface programatically, I think working in storyboards is a way more visual and fun way to learn what’s going on. So we’ll be working in storyboards, Xcode’s visual editor for storing the user interface.
While still in the Navigation Area, and under the HelloWorldApp folder, click on Storyboard.swift.


# Adding Object Elements


Go ahead and click on the Object Library as seen in the picture below, or (Shift + Command + L).




Go ahead and add a “button” and a “label” to the canvas. Place and drag the Button and Label objects from the above Object library. With the Show the Attributes inspector icon at the top of right panel, change the button text, size, and font to “Display Greeting”, add a background color, and rename the label to “Hello World”.




# Connecting the UI elements to the Code
Now that we completed our UI, let’s write our code to establish a connection to the UI.
To view both files side by side, click the Assistant Editor to open the ViewController.swift file in the project navigator.



