The goal of this book is not to make a choice between one or other framework by two make you comfortable enough with Laravel so that you can choose the right tool for the job.

Throughout this book I will reference waves certain tasks are done in Drupal and then I will clearly outline how it can be done in larval. White with any of this stuff there is more than one way to do these things I'll be showing you my way in ways that I've seen from other professionals in the industry.
 
 what we will cover
 routing
 composer
 bottles
 views
 commandline
 deployment
 teamwork
 testing
 libraries building this way
 rest
 user authentication
 theme work
 angular JS
 hosting
 choose and crawl
 
By the end of the book I hope you will be comfortable in using Laravel. And then many of your Drupal paradigms will easily translate for you to Laravel. Is even know Drupal in many ways testings and away you need to the industry I think you will seal I was concerts can be carried over  

## about me

I started in the industry about 15 years ago. Basically I started working in a shop that fixed and builds Windows 3.1 entire PC. Your pack before USB pack when installing a printer needed a technician. From there came Wintex server administration and eventually PHP MySQL. About six or so years ago I decided to focus on building websites. It was then that I was choosing between a few different technologies to focus on because I figured I just could not learn everything. And at that time I chose Drupal when he was around 4.7.

Yeah that was before people even knew it Drupal was no it's a chance to nonprofits in the area and spa mistresses I needed a content management system to use Drupal Coursey would say when I use WordPress but anyways after having my own shop that was solely focus on Drupal I finally came to a point about two years ago we started really diving into other technologies. 

His first I was Ruby on rails. No still working at Drupal shop but for some reason started to learn Ruby on rails. The model view controller layout was really new to me especially coming from Drupal. After going through certain tutorials and building a project or two for nonprofits and then building my own blog started really get comfortable with it.

Then came in dinner Jess and this is where something really hit me these technologies in different people from different times with different goals shared workflows models for and I think it was at that moment I really understood how different Drupal is.

Now before long using MVC and rails and how easy the same system was how easy was getting your house pretty much ready to leave PHP. Then came Larave. Laravel like angular like Rails Pike express like so many other things out there is following in the MV Star approach to managing request and business logic. 

I think the creative Laravel even know what she was very influenced by reels as as well as other frameworks is he trying to bring together common concepts from the industry into his framework. I think you'll see Taylor well was not so concerned with building a new framework with new ways of doing things but more about bringing together some common tools and workflows into a single framework that is very very customizable. 

Since then I have built a handful of things, applications, websites, libraries, that are in Laravel were built in Laravel but then move to their own libraries. At the same time I've continued to working Drupal, angular, as well as billing restful APIs and Laravel and Drupal.

Again a lot of this will be around the tool for the job I think we all know is Drupal developers it's easy to think Drupal can do or should do everything. Has one person said it's not always about the right tool for the job it's a toy you know. What I am trying to say is it's not the tool as much as the concepts behind out we code now we build and engineer applications. And it still shared principles that help us to use the The right tool for the job.

For example if I had to choose between two Porelarr for content management system I was heavenly heavily reliant on revisions workflows rolls tagging simple data models in a simple scene and I would easily choose Drupal. But once the models got complex and content management system is not so much a priority as much as a smaller part of the job and I might start thinking Laravel. And that's what I hope this book will show is how to use either or not a comfortably switch between them.

For this book it won't matter what operating system using because wrong to be using vagrant in Homestead for these examples. Homstead is a vagrant billed by the creative Laravel know give us a unified system to work. So other than the struggles a common setting up vagrant for either my next Mac or PC windows which I will leave up to you these example should then work as there in the book on your computer.

Another thing you will see throughout this book is the commandline yeah. Drupal has a very powerful tool called Russian I like it a lot. But what you'll see Marvel's a twinkle Barneson in the library were to use called Waze generators which will allow us to use the commandline to build our application test our application the ploy our application in many other things. Again trash can do many of these things if not all but I am here to show how Laravel does them announce some ways in many ways you can transfer your Drupal knowledge over. So as we go through the trackers you'll see the commandline options available and how to use them.

Also realize that Laravel has a creep documentation website so I will not as much as possible repeat any of that reference it as. I will mostly be bridging the gap between the two frameworks and pointing you in the right direction is needed for giving you examples.
 

One thing to consider two in this book and then your mindset is that were going to be doing a lot of object-oriented program I will try and keep it basic I won't really going to explain why or what a good principles but that's just how things are what Laravel I think how things are more so with D8. Obviously a lot of great things of been dealt with procedural programming. But I think you will see in time then working this way really creates an application that is easier to maintain and extend.


So let's dig in to this really fun PHP framework as I try to help you as a Drupal developer not only see how Laravel but will carryover to two drupal 8, as well as frameworks. 


## Chapter Folder layout



   
## Chapter Routing

After working with some of the small micro-frameworks out there
I really begin to understand how key routing is too a good framework (yes I might be a little slow). In building numerous Drupal module the menu system becomes the entryway between the user's interaction with the browser and your application. Let's look at an example of a route in Drupal  

insert route here

As you see with the routes above your defining several actions get, put, host, and. Even if you were to consider a known you would still end up with several of these routes. In the first round you're saying let's get all of these items and that you must have these permissions to do this and that we are passing these arguments with it. Let's look at a similar routes in Laravel.

INSERT ROUTEResoucre

Example number one shows a resource that is the most simplest of is a dynamically generates common methods needed to interact with the model. I would only mean by model? Will go more into model views to control shortl but let's think about this for a moment sometimes your page that the user visits is going to render data from a model a model being and entity or object from the database for example a page model might have a title in the body or a user model might have a username email and password.These examples are given of the above models I'll show another example shortly where were maybe trying to render a more complex. With numerous models etc.now that show how this route would be written if we were to write each one as we did above for Drupal.

INSERT 5 ROUTE each listed

so as you see there are quite a few differences. First of all notice some of the routes are the same. What makes these rounds different is the method being used.  unlike resource route seen earlier we are defining each one, normally would not need to do this, just for this example I'm writing them out. You can also add other routes as needed.

Insert route for x

All the above examples of what we would call closures and only the resource one so far is going to controller. I will go over controller shortly but basically just want to see how easy it is to play around in the router.

For example see you want to just test on the phone of yours or an idea you could easily write this to closure, start up Laravel, visit the world, and see what you see.

Show results image

Sure with PHP to do all this is a commandline there a lot of benefits of doing things in a web browser especially happy things are some ideas are testing the aquarium or whatever that might be working on.

before we going to controllers was looking a couple more things and you normally do in the menu with Drupal and how we doing here.

##Passing arguments

Hey Drupal menu you may typically ass arguments like this

Insert example from example module

And then you would get the arguments in your particular function

Insert example from ex mod

And Laravel you could lay around write a route has such again this is just a closure will go into controller shortly,. And doing this you can see how you can access the arguments. 

And then of course there are other type of arguments not always in the get part of the URL. Let's use post man to show how we can get arguments are passed in the body of the request  

Show postman image

You'll see in this case I am sending Laravel some information via post and then I am calling to those parameters using the input method  

Before we go any further with stop and think for a moment about the route and the method they look like static methods. With a really façades. So they are easy to use but at the same time they're very easy to test and they are not static and that they are really instantiation of the object for you.
