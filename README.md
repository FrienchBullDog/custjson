# CustJSON
A python package that makes its own little custom variant of JSON. Still easy to read, just no nested values (yet)

## WARNING
By using this package, the code writer does not take responsibility if you use this package and data gets leaked or stolen due to the CustJSON format being <u>*plain text*</u>.

<br/><br/><br/>

# Usage
## Opening, Closing, Deleting and Creating files

To start using the package, make an initialization object using this code:

    i = custjson.Init()

This line of code initializes the package's features, which by proxy means you have to run CustJSON's functions via *i.function(foo,bar)*

To create a file directly and load it into the package's memory, type:
    
    i.create_file("filename-without-extension")
    
Replace "filename-without-extension" with the filename of your choice WITHOUT THE EXTENSION. It automatically assigns the file a <u>*.jn*</u> extension.

To load a file that already exists to the package's memory, type:

    i.open_file("path/to/file/filename.jn")
    
Again, replace "path/to/file/filename.jn" with the path to your file (including your file AND the .jn extension.)

To delete a file, make sure it's loaded in memory, and then type:

    i.delete_file()
    
To close a file, it's the same process, but with a different command.
Type:

    i.close_file()
    
## Reading and Writing to files

To read and write to .JN files, you first have to load them into CustJSON's memory as shown before, then you can simply use the commands
    
    i.read_value_from_name("valueNameHere")
    i.read_line(lineNumber)
    
Replace each placeholder with its respective value, for example if you wanted to get the value of the key "space", you'd do:

    i.read_value_from_name("space")
    
and replace *lineNumber* with... the line number you want to read from the current file...

##  &rlm;&lrm;

You have now learned how to use CustJSON. Yaaay!

# Changelog

v. 0.1.1:
    Fixed a bug with the value reader not being coded properly. Woops!
