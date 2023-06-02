# Class-in-python
We are going to learn everything about classes in python.

# What is a python class?
A Python `class` is like an outline for creating a new object. An `object` is anything that you wish to manipulate or change while working through the code. Every time a class object is `instantiated`, which is when we declare a variable, a new object is initiated from scratch. Class objects can be used over and over again whenever needed.


To begin, in order to create a class object, all you have to do is type the following:
```python 
class CreateProfile:
```
The name of the class is subjective but the general rule regarding the format of the name is to follow something called [camelCase](https://en.wikipedia.org/wiki/Camel_case#:~:text=Camel%20case%20(stylized%20as%20camelCase,iPhone%22%20and%20%22eBay%22)).

Usually, when creating a class, you will have to define a function called `__init__` with `self` as the initial argument.


# What is an “`__init__`” function?
An `__init__` function is called when a class is instantiated. By instantiate, we mean when you declare the class, which can happen either by itself or by assigning it to a variable. Here are some quick examples of instantiating a class object:

```python
CreateProfile()
# OR
profile = CreateProfile()
```

Here we are instantiating the class object and by doing so, we are implicitly calling the `__init__` function. Any arguments within the `__init__`function will also be the same arguments when instantiating the class object. These initial arguments can be the data we wish to manipulate throughout the class object. But in regards to the `self` argument, it will not be necessary to replace when instantiating the class object.


# What is “self”?
The `self` argument is an implicit argument that will always be called when instantiating the class or when you use a custom function within that class. The `self` refers to the object it is manipulating. In our case, the new dating profile we want to create.

To further understand the usage of `self`, we will continue constructing our class. Let’s fill in some other arguments that our `__init__`function will take:

```python
class CreateProfile:
    def __init__(self, dataset, profile):
        self.dataset = dataset
        self.profile = profile
 ```
 
As you can see here, we are adding some arguments after `self`. These arguments are empty for now but in order to be used throughout the class, we must assign them to the object or self that we will manipulate with functions later on.


# Class attributes
When assigning these DFs in our __init__ we are effectively creating class attributes. They can be called upon after instantiating the class and they will return whatever variable we assigned to the object (`self`):
```python
# Instantiating the class
new_profile = CreateProfile()
# Calling the class attribute
new_profile.dataset 
```
In this case, running this code will return error because we have to give our attributes some values. We can give them None value and in this case it returns None.


# Class Methods (Functions)
Functions that we create within a class are called methods. Functions and methods are essentially the same thing but in the context of class objects, functions are referred to as methods. We will need to create some methods for our class in order to manipulate and utilize the data given.


## Running the Class method
We wrote the below code and we want to use our second method:
```python
class createProfile:
    def __init__(self, 
                 dataset=None,
                 profile=None):
        self.dataset = dataset
        self.profile = profile
    # Here we add another function
    def enter_info(self):
        # Code goes here
```
All we have to do after instantiating the class object we have to call our method like below:
```python
# Instantiating with the data from the DF of synthetic profiles
new_profile = createProfile(dataset=data)
# Running the method
new_profile.enter_info()
```


# Using our class in other python files
One thing that is also really useful when creating a class is that we can import the class we create into other Python files or notebooks. Just save the Python class in a `.py` file and you can import it later on. Just make sure it is in the same directory. You can import the class like any other Python library:
```python
from your_file_name import CreateProfile
```
