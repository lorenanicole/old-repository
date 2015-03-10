### Take Aways from Learn Python the Hard Way (1-18ish)

[When to use %s vs. %r?](http://stackoverflow.com/questions/6005159/when-to-use-r-instead-of-s-in-python)s

```
>>> import datetime
>>> datetime.datetime.now()
datetime.datetime(2015, 3, 10, 16, 2, 16, 153941)
>>> str(datetime.datetime(2015, 3, 10, 16, 2, 16, 153941))
'2015-03-10 16:02:28.417096'
>>> repr(datetime.datetime(2015, 3, 10, 16, 2, 16, 153941))
datetime.datetime(2015, 3, 10, 16, 2, 23, 193465)'
```

%r uses the repr() function to interpolate a value 

%s uses the str() function to interpolate a value

####What's the diff?

Use Python's nifty built in help to learn how to use a function, what it does, etc.

```
>>> help(repr)
>>> help(str)
```

repr() = "canonical" representation

str() = "Return a nice string representation of the object."


###Formatting Strings

```
>>> print "hello\nworld"
hello
world
>>> print "hello\tworld"
hello	world
>>> print 'I\'m a cool lady!'
I'm a cool lady!
>>> print "She said, \"I'm a cool lady!\""
She said, "I'm a cool lady!"
```

Contain strings always within same type of quotes - single, double, or triple. 

[Single vs. double quotes?](http://stackoverflow.com/questions/56011/single-quotes-vs-double-quotes-in-python)


###Python Scripts That Take Arguments

sample_script.py
```
from sys import argv
one, two, three = argv
print type(argv)
print argv
print one
print two
```

```
$ python sample_script.py "hello world" True
<type 'list'>
['argv.py', 'hello world', 'True']
argv.py
hello world
```

argv stores the arguments you pass in with script as string elements in a list


###Opening Files to Read

sample_script2.py
```
test = open("../test.txt")
print test.read()
```

Where is test defined?

Other actions -
```
ex = open(filename, 'w') #write into file
ex.truncate() #Not really needed
ex.write("Fancy things")
ex.close()
```
Truncating is not necessary since when open file in write mode it already [overwrites the file](http://stackoverflow.com/questions/4562100/why-truncate-when-we-open-a-file-in-w-mode-in-python).

Writing is different vs. [appending](http://stackoverflow.com/questions/4706499/how-do-you-append-to-a-file-in-python).


