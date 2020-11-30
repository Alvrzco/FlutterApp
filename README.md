# FlutterApp

# ASSIGNMENT: PRACTICE 2 - GRAPHIC USER INTERFACES FOR MOBILE APPLICATIONS

## Presentation of the _assignment_

The following describes the mission (_assignment_).

### Objective

In this mission (_assignment_) you will have to develop an application
for mobile devices. To achieve your goal you will have to use the
knowledge acquired on the development of graphical interfaces of
user.

To carry out your task you will have the multiplatform toolkit
`flutter` and the associated programming language` dart`.



### Introduction to _assignment_

Our spies have discovered the existence of services capable of
analyze images and automatically obtain their characteristics
more relevant using modern A.I. techniques. Your mission is
develop an application that allows the user to perform a
photography and obtain its relevant characteristics.

As we have already said, there are already services capable of analyzing
images automatically, so your mission is focused on the
client part.



### Means

The application will be validated on the android platform for devices
mobiles.

You should procure the following tools:

* `android` version> = 8.0
* `flutter` version> = 1.22
* `Git`
* A repository at [github.com] (github.com). You can see the details
  in the corresponding appendix.

The rest of the necessary resources will be presented with each
committed (_task_), as needed.




### Background

We have currently identified different services based on the
most current _Machine Learning_ techniques applied to different
fields of the A.I .. Several of them include the recognition of
images and offer a remote API to access from our
client applications.

In general, these APIs offer one or more calls through the
which our application can send an image to the server and
obtain the extracted information as a response. Such information
can include data such as dominant colors, location of
faces within the image, labels for the objects contained in the image
image, etc.

As you might expect, the variety of information retrieved and the quality
it depends, in turn, on the quality of the service. However,
the criteria for selecting the service will be the following:

  * Simple REST API. We want to use it from our code with a
    simple http client, without the need for extra libraries.
  * Free plan. Although it has a limit of requests.



### The server

The selected server is (** imagga **) [https://imagga.com]. The
API documentation for it is available at (imagine
api) [https://docs.imagga.com]

In order to use the imagga API services, it is necessary to create a
account and obtain the usage keys.

The api documentation provides several examples that can be
test even from command line using app like
`curl`.

Also in the documentation you can see the different
categories of information that the server is capable of providing:
labels, categories, faces, colors, text, ...



## Planning

Below are the _tasks_ to perform. Remember that the
mission success depends in large part on your carrying out the
_tasks_ in the planned order.


### TASK 1: Retrieve information (Model-View-Presenter)

Your first task (_task_) in this mission is to develop a first
version of the application. This first version will implement the
Next steps:

  * Take a picture.
  * Upload the image to the _endpoint_ of the selected API.
  * Show the result.

> Attention: The application will use a single _endpoint_. Study the
> _endpoints_ available and select the one you consider appropriate.

Start by selecting an _endpoint_ among those offered by the API of the
server. Next design the interface and create a _wireframe_ with
the necessary screens. Include the wireframes in a file
`wireframe.pdf`.

> Attention: The optimal way to present the results to the user
> depends on their nature, that is, it depends on the
> _endpoint_ selected. It is not the same to present the information of the
> _endpoint_ `/ faces`,` / colors`

> Attention: The `flutter create` tool creates a file
> `.gitignore`. Stick to their rules.

Once the design is done, implement it using the library
`flutter`. The resulting application has to be functional in a
android platform (8.0 or later).

Do not forget to make requests to the server concurrently and
manage errors. A major network errors, in a
mobile device may appear other errors such as:
 
  * The application does not have permission to use the network.
  * The app does not have permission to use the camera.

Consider the following resources during the
carrying out this task:

  * There are two libraries to use the device's camera:
    (Take a picture using flutter camera) [https://medium.com/@navinkumar0118/take-a-picture-using-flutter-camera-a9c11d282632]
    
  * The _cookbooks_ section of the _flutter_ documentation includes a
    set apart from
    (_networking_) [https://flutter.dev/docs/cookbook#networking],
    where to find examples of http requests.
  
  
  
Before this task can be considered complete you must
make sure you have reached the following conditions
(_requirements_):

  * [There are no files pending commit] (check :)
  * [The last commit has the tag "task_MVP"] (check :)
  * [The remote repository is updated] (check :)




### Task 2: Design sw

Your next task is to apply a suitable software design pattern
to the type of library used. The task includes creating the layout
software and modify the implementation to follow the design.

The task begins by analyzing the different models available. In
the _flutter_ documentation the section dedicated to state management
(_state managment_) has a section that describes some
(options) [https://flutter.dev/docs/development/data-and-backend/state-mgmt/options]
, as in the web (fluttersamples) [https://fluttersamples.com/].

Then select a different model of the Model View Controller
(MVC) or its variants, make the design of your application following the
model you have chosen and expressing the model in UML. Includes views
static and dynamic design.

Once the design is done, adapt the implementation of the app to the
design.


Before this task can be considered complete you must
make sure you have reached the following conditions
(_requirements_):

  * [There are no files pending commit] (check :)
  * [The last commit is tagged "task_sw_design"] (check :)
  * [The remote repository is updated] (check :)



### Task 3: Adaptability

After a brief observation, we know that the screens of the
devices can vary their configuration: horizontal or vertical, and
that the screen size can vary substantially between
devices that we normally categorize as mobile phones or tablets.

Improve your application so that it detects different configurations
(vertical vs horizontal screen) and different devices (mobile vs
tablet), and use the most appropriate result view layout
for each case.

It begins by designing an appropriate results view for each case and
ends the mission by implementing device discovery and
configurations and different layouts of the view.

Remember that once again in the _flutter_ documentation you can
find relevant examples for this purpose.

Before this task can be considered complete you must
make sure you have reached the following conditions
(_requirements_):

  * [There are no files pending commit] (check :)
  * [The last commit is tagged "task_response"] (check :)
  * [The remote repository is updated] (check :)


### Task 4: Material

For your app to be integrated into the android app ecosystem is
need to follow its same design system (_design system_). East
system, created by google, is (_material_) [https://material.io/].

_Flutter_ `material.dart` library already does a great job
to adapt the interface to the _material_ guides. However, to
Even though you have used this library, there may still be discrepancies.

Review the _material_ guides and change those aspects of your app
that do not conform to what is established by the design system. Note in
a `material.md` file all the changes you make.

Before this task can be considered complete you must
make sure you have reached the following conditions
(_requirements_):

  * [There are no files pending commit] (check :)
  * [The last commit has the tag "task_material"] (check :)
  * [The remote repository is updated] (check :)


