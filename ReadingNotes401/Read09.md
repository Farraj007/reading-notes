[Main Page](../README.md)
# Reading Notes 09  

## Articles  
### Dunder Methods
* [Dunder](https://dbader.org/blog/python-dunder-methods) 

dunder = 'double under'

Object initialization = To construct account objects from the Account class I need a constructor which in Python is the __init__ dunder:

Object representation = It’s common practice in Python to provide a string representation of your object for the consumer of your class (a bit like API documentation.) There are two ways to do this using dunder methods:

__repr__: The “official” string representation of an object. This is how you would make an object of the class. The goal of __repr__ is to be unambiguous.

__str__: The “informal” or nicely printable string representation of an object. This is for the enduser.

Object Iteration = __len__, __getitem__, __reversed__, __contains__

Operator Overloading for Comparing Accounts = __eq__
__lt__

Operator Overloading for Merging Accounts = __add__

Callable Python Objects = __call__

Context Manager Support and The With Statement = __enter__, __exit__
### Statistics - Probability  
* [Statistics](https://www.dataquest.io/blog/basic-statistics-in-python-probability/)  

What is probability?  
- An event is some outcome of interest. The odds, when flipping a coin.  
- For all the possible outcomes, they will create what is called the sample space.  

From statistics to probability  
- We generate data from flipping a coin 10 times. This could be referred to a set, and a trial. In this trail we know what the probability is suppose to be , 50/50 for heads and tails.  
- We can keep track of trials and compare each set of trials to each other and get an accurate average. This is keeping track of the stats or statistics of that probability.  

The data and the distribution  
- Normal distribution: refers to a particularly important phenomenon in the realm of probability and statistic.  
- Normal distribution has a unique symmetry and shape when tracked on a graph.  

Three Sigma Rule  
- Also known as the empirical rule or 68-95-99.7
- Dictates that given a normal distribution, 68% of your observations will fall between one standard deviation of the mean. 95% will fall within two, and 99.7% will fall within three.  
- Also refered as the rarity of extreme values.  

Key Notes  
- Statistics is not field relegated to just statisticians, we as data scientists and developers know how to comprehend and read this data.  
- Statistics and Probability are connected.  
- Statistics can determine if one value is from setA or setB of data when dealing with outcomes.
