Data model
An application can be considered as layers of data model representations.
For example as a developer you will initially model ur problem solutions into objects, data structures and api that will manipulate these
when it comes to storing these data models, you will now consider which database, the developers of these database also 
have to provide a model to represent the data u want to store, which can tables or json in some nosql databases.
The hardware developer also helps the database developer by providing a way to model the data provided as electric pulses. 


This chapter is mostly about helping you deciding on which data model to choose in your application precisely when making a decision on how to store them.

# Why is this so important ?
Because the choice of the data model when storing comes with some set of assumptions which determines how fast you can query your data, how easily you can perform transformations and so on. 
So deciding on the wrong data model for application can have serious consequences.

Another thing is in a more complex application, the data model you choose can affect how different systems can interact with you. The data model serves as an abstraction for other people to interact with you, so it important you consider all the possible assumptions sorrounding it.

