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



![1_s2JiotFapGxEnkxgSp5YXQ (1)](https://user-images.githubusercontent.com/14343387/106994097-20f19c00-67a2-11eb-9eba-bb001b9ac093.png)



As you can see, our project files are in the Navigation Area. Our interface buttons for our app will be designed in the Storyboard.swift file and our Swift code will be held in the ViewController.swift. Xcode already provided us with a View Controller project file to get started. For now, don’t worry about the AppDelegate.swift or other files.
# Creating the UI Design

Although you can code the interface programatically, I think working in storyboards is a way more visual and fun way to learn what’s going on. So we’ll be working in storyboards, Xcode’s visual editor for storing the user interface.
While still in the Navigation Area, and under the HelloWorldApp folder, click on Storyboard.swift.


# Adding Object Elements


Go ahead and click on the Object Library as seen in the picture below, or (Shift + Command + L).

![1_6dH55pBJgRBWbjIOfy0wOA (1)](https://user-images.githubusercontent.com/14343387/106994108-251db980-67a2-11eb-9e15-6a1477136aff.png)



Go ahead and add a “button” and a “label” to the canvas. Place and drag the Button and Label objects from the above Object library. With the Show the Attributes inspector icon at the top of right panel, change the button text, size, and font to “Display Greeting”, add a background color, and rename the label to “Hello World”.

![1_JKPySBUnp7Ph_85dbICq7A](https://user-images.githubusercontent.com/14343387/106994111-264ee680-67a2-11eb-949d-4c1ffb919f3b.png)


## Adding Constraints
We need to add constraints so that it stays in place when rotating the device or using on different screen sizes. With the element selected, you will want to click on the icon below to add constraints.

![1_pmkOF17VOWpY7HZ2qd4ygQ](https://user-images.githubusercontent.com/14343387/106994115-2818aa00-67a2-11eb-96e8-89eae644ed42.png)



# Connecting the UI elements to the Code

Now that we completed our UI, let’s write our code to establish a connection to the UI.
To view both files side by side, click the Assistant Editor to open the ViewController.swift file in the project navigator.


![1_JidIaUbBnRGuaEpaugucSg](https://user-images.githubusercontent.com/14343387/106994120-2a7b0400-67a2-11eb-8354-fbd0b1cfb38f.png)



We now need to establish our connection between the “Display Greeting” button to the View Controller.swift file.
In the Storyboard.swift file, click on the “Hello World!” label. While clicking on the CTRL button on your keyboard, click and drag the label to the ViewController.swift file. Make sure the label is a Connection Outlet and labeled “helloWorld”. Do the same with the “Display Greeting” button, except make sure that you change the connection to Action.
It will look something like this:


Completing the code
One last step before testing the app is to place the following code in the toggleGreeting(_ sender: Any) method you’ve just added, which will hide the “Hello World!” greeting when untapped:helloLabel.isHidden = !helloLabel.isHidden .
You’re finished code should look like this:


```
import UIKit

class ViewController: UIViewController {
//  Connecting HelloWord text label
      @IBOutlet weak var helloLabel: UILabel!
//  Connecting "Display Greeting" button   
      @IBAction func toggleGreeting(_ sender: Any) {
        helloLabel.isHidden = !helloLabel.isHidden
    }
    
    override func viewDidLoad() {
        super.viewDidLoad()
        
    }

   
}
```


The iOS simulator… Let’s test this bad boy out!
One of the best things about XCode and iOS development in general is seeing your creation come to life instantly via the simulator. You can even plug your iPhone in and test it on multiple devices. Once loaded, press the button and you will see “Hello World!” Sweet!






