## MySQL-based forum functions

Originally published: 2007-06-08 08:43:19
Last updated: 2007-06-08 08:43:19
Author: Calder Coalson

This program provides the basic functions required to write a forum in MySQL and Python.  The way the class is structured allows it to be imported and used in any application, whether it's web based, command line, Tcl/Tk or wxPython.  It simply provides the helper functions to perform actions required to get, use and set different data in the database.\n\nHowever, I have not included the code to create the database yet.  Here's the structure:\nTABLE: users\n    INTEGER: id\n    STRING: name\n    STRING: signature\n    STRING: password\nTABLE: messages\n    INTEGER: id\n    LONGSTRING: content\n    DATE: created\n    TIME: createdtime\n    DATE: edited\n    TIME: editedtime\n    INTEGER: authorid\nTABLE: threads\n    INTEGER: id\n    STRING: title\n    STRING: messages\n    DATETIME: edited\n\nCreate that database, set up a user account, and change the arguments in ForumBase.__init__ to the user you want the program to log on as.