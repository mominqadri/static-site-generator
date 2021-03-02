# Utils/html_checker.py
Useful Resources: 

- HTML.Parser python doc(https://docs.python.org/3/library/html.parser.html)

- Understanding Super (https://realpython.com/python-super/)

- Argeparse - (https://docs.python.org/3/library/argparse.html)

-

Understanding Sections of code:


**from html.parser import HTMLparser**

This module defines a class HTMLParser which serves as the basis for parsing text files formatted in HTML

An HTMLParser instance is fed HTML data and calls handler methods when start tags, end tags, text, comments, and other markup elements are encountered. The user should subclass HTMLParser and override its methods to implement the desired behavior


**from html_content_spec import content_spec, _ANY_CONTENT, _NO_CONTENT**

This import receives the content_spec dictionary from html_content_spec.py which maps the tags to categories and content models.


**import argparse**

argpars essentially reads command-line arguments and can put them in your program. It is a command-line parsing module.


**Class OurHTMLParser**    

Class OurHTMLParser is the descendant of HTMLParser and only overrides necessary methods

    def __init__(self):  # type: () -> None

        super(OurHTMLParser, self).__init__(convert_charrefs=False)


super() gives you access to methods in a superclass from the subclass that inherits from it. super() alone returns a temporary object of the superclass that then allows you to call that superclass's methods.

super() can also take two parameters: the first is the subclass, and the second parameter is an object that is an instance of that subclass.

super() works in single and multiple inheritance.

# Utils/create_menu.py
Creates a menu from a tab-delimited text file

Useful Resources:

- sys module: https://docs.python.org/3/library/sys.html

Understanding Sections of Code:

**from pylib.parse_site import parse_site, InputError**

This import receives the parse_site function from /pylib/parse_site.py which breaks down an input file.


**from pylib.html_tags import sidebar, sidebar_links**

This import receives the sidebar and side_bar link functions from /pylib/html_tags.py that generate differing sidebars given different inputs.

    def process_menu(topics, level):
    
This function generates a menu level given topic objects and a level integer.







