# NextLabs-Assignment

## Problem Set I - Regex :
Write a regex to extract all the numbers with orange color background from the below text in italics (Output should be a list).<br>
{"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}

### Solution :
import re <br>
text = '{"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],
"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}' <br>
numbers = re.findall(r'(?<=:)\d+', text)<br>
print(numbers)

### Output : 
['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '648', '649', '650', '651', '652', '653', '3']


## Problem Set 2 - A functioning web app with API :
1. [Frontend Repository Link](https://github.com/Rose-Grace-Jacob/NextLabs-Frontend.git) <br>
2. [Backend Repository Link](https://github.com/Rose-Grace-Jacob/NextLabs-Backend.git)<br>
3. [Project](https://github.com/Rose-Grace-Jacob/NextLabs-Backend.git)


## Problem Set 3 - Questions :
### 1. Write and share a small note about your choice of system to schedule periodic tasks (such as downloading a list of ISINs every 24 hours). Why did you choose it? Is it reliable enough; Or will it scale? If not, what are the problems with it? And, what else would you recommend to fix this problem at scale in production?


### 2. In what circumstances would you use Flask instead of Django and vice versa?

Each framework has its own unique features, so we can use it in accordance with the requirements of a particular project. As a full-stack web framework, Django is best suited for developing large and complex web applications, while Flask is a lightweight, extensible framework that allows you to develop small web applications. <br>

Django is a full-stack web framework that follows an object-oriented approach. It is suitable for multiple page applications. Django supports the most popular relational database management systems like MySQL, Oracle etc.
Django is less flexible. Developers do not have full control over the modules and functions of Django because of built-in libraries.Django framework supports the mapping of URL to views through a request.
Django supports dynamic HTML pages.Open-Source, Great Community,Fast Development, Easy to learn, Secure. <br>

Flask is a lightweight framework that gives abundant features without external libraries. It is suitable for only single-page applications and does not support the basic database management system and uses SQLAlchemy for database requirements. Flask is a micro-based framework with extensible libraries making itself a flexible framework for developers.
Flask allows developers full control over the creation of applications.Flask web framework allows mapping of URL to class-based view with Werkzeug. It does not support dynamic HTML pages. Extensive Documentation,Lightweight, Minimal Features, Open-Source.<br>

In short, if we are building a small application that doesn't require many built-in features, Flask is a good choice. If you are building a more complex application that requires a lot of built-in features, Django is a better choice.

It's worth mentioning that we can use both frameworks together in the same project, where Django could be used for handling the more complex functionality and Flask could be used to build a RESTful API.
