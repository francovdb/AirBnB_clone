AirBnB_clone Group project

# CONCEPTS LEARNT

    How to create a Python package
    How to create a command interpreter in Python using the cmd module
    What is Unit testing and how to implement it in a large project
    How to serialize and deserialize a Class
    How to write and read a JSON file
    How to manage datetime
    What is an UUID
    What is *args and how to use it
    What is **kwargs and how to use it
    How to handle named arguments in a function

#Introduction

This project is the first part ongoing Airbnb Clone.

In this project we are building the backend of the Airbnb. We created a Command Line Interpreter (CLI). This is similiar the the Shell project in C, but with Python's high level cmd framwork makes this as simple as importing cmd and beginning each function with do_*.

The command intepreter is written in the console.py file. It has several methods which allow us to manage the objects of the project:

    Create a new object (ex: a new User or * a new Place)
    Retrieve an object from a file, a database etc…
    Do operations on objects (count, compute stats, etc…)
    Update attributes of an object
    Destroy an object

The CLI is linked to several other classes:

    BaseModel, User, FileStorage, amenity, City, State, Place, Review

BaseModel is the parent class. It takes care of initiliazing, serializing and deserializing each instance.

The flow of the serialization and deserialization is: instantce <-> Dictionary <-> JSON string <-> file

In file_storage.py we created a storage engine for the project. The methods for creating a new instance, saving and reloading it are in the FileStorage class.

The following is a tree diagram of this projects folders and files:

packagemodels
┣ open_file_folderengine
┃ ┗ scrollfile_storage.py
┣ scrollamenity.py
┣ scrollbase_model.py
┣ scrollcity.py
┣ scrollplace.py
┣ scrollreview.py
┣ scrollstate.py
┗ scrolluser.py

The Unit Tests are:

packagetests
┣ open_file_foldertest_models
┃ ┣ open_file_foldertest_engine
┃ ┃ ┗scrolltest_file_storage.py
┃ ┣ scrolltest_amenity.py
┃ ┣ scrolltest_base_model.py
┃ ┣ scrolltest_city.py
┃ ┣ scrolltest_place.py
┃ ┣ scrolltest_review.py
┃ ┣ scrolltest_state.py
┃ ┗ scrolltest_user.py
