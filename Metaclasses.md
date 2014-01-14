[Home](README.md)

Real World Use for Metaclasses in Python
========================================

So you learn what a metaclass is and how to implement it but you have no idea where to use it? 
I hope that this article will help you to understand a read user case, maybe not the most interesting one,
but at least a useful example of how to use metaclasses to augment your classes.

I'm working on a web UI that use Angularjs (awsome!) to read and write some data on a database (MySQL, less awesome...) 
and I'm using ngTable to show the data. Since ngTable automate some of the common tasks that you usually have to do when dealing
with data (pagination, filtering, sorting, etc.) I decide that was a good choice. The only downside is that I have to write
a restful API for every model, since ngTable has is own way to send urls attributes for filters etc.
So I decided to write my own RestfulAPI for Flask and SQLAlchemy, and to use Metaclasses to manage some data that
otherwise the class would be force to calculate every time I send a request. I'm also using descriptors for the various fields
type, but this is probably a topic for another article.

[ This is a work in progress ]
