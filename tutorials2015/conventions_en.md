<!-- ---
layout: default
title: Conventions
--- -->

# Conventions 

There is a number of conventions that are used to format your `Python` code. I will briefly list them below. This document contains a combination of general purpose `Python` conventions, as well as `Flask` specific ones.

### 1. The PEPs

A __PEP__ is a “Python Enhancement Proposal”. Usually, PEPs are meant to guide the way we write our code. 

##### __1.1. PEP 8__

__PEP 8__ is the official style guide for Python code. Your code will be much more approachable when it starts growing to many files with hundreds, or thousands, of lines of code. I will not enumerate the conventions here, because it implies copy-pasting the PEP-8 documentation here, so here is a link to [official PEP-8](http://legacy.python.org/dev/peps/pep-0008/).


##### __1.2. PEP 257__

__PEP 257: Docstring Conventions__ covers another Python standard: __docstrings__. The aim of this PEP is to standardize the high-level structure of docstrings: what they should contain. Consider reading the official documentation of [PEP 257](http://legacy.python.org/dev/peps/pep-0257/).

### __2. Relative Imports__

Use relative imports rather than absolute ones. Using relative imports, you would indicate the location of the target module relative to the source. 

	
	# myapp/views.py

	# An absolute import gives us the User model
	from myapp.models import User

	# A relative import does the same thing
	from .models import User
	

For a more detailed description of this feature see [Guido's Decision](https://www.python.org/dev/peps/pep-0328/#guido-s-decision).

### __3. Project Structure__

`Flask` gives you absolute freedom at this chapter. You could put your entire application in one file, or have it spread across multiple packages. Still I'd consider the following patterns.

##### __3.0. Virtualenv__

The virtual env has to be situated inside the top project directory. The virtualenv will create a hardlink to the default python interpreter, I suggest in to be python2.7.

To create a virtualenv:
	
	mkdir myapp
	cd myapp
	virtualenv env

To activate the virtualenv, use the following:
	
	cd myapp
	source env/bin/activate

To deactivate the virtualenv:

	deactivate

I think that these commands are enough to run the summer camp. 

##### __3.1.1. Single Module__

If we're talking about a quick minimal project this is your best choice. 

	
	app.py
	config.py
	requirements.txt
	static/
	templates/
	

Application logic would sit in app.py, for the following example(you still can give any name that fits your considerations).


##### __3.1.2. Package__

For complex projects a single module can get messy, and this will not contribute the development process in a good way. To solve this problem, we can factor out the different components of our app into a group of inter-connected modules — a package.

	
	config.py
	requirements.txt
	run.py
	instance/
	    config.py
	yourapp/
	    __init__.py
	    views.py
	    models.py
	    forms.py
	    static/
	    templates/
	

The structure shown in this listing allows you to group the different components of your application in a logical way. The class definitions for models are together in `models.py`, the route definitions are in `views.py` and forms are defined in `forms.py`.


##### __3.2. Configuration file__

`Flask` is written in pure python, this allows us to create modules that can be imported so that we can separate the application parts logically. For simple projects keeping all the configuration settings in a `config.py`, while working on a large project, having `environment-based` config files will make your life much easier.

For decails consult the [Explore Flask Configuration](https://exploreflask.com/configuration.html) page.

However, I suggest that, during this summer camp, we stick to a single `config.py` file due to the simplicity of explaining the concepts of configuring your app.

##### __3.3. Run file__

Having a `run.py` file gives a meaningfull name to the process of starting the development server.

	
	python run.py
	

One of the reasons I use this approach rather than runing the `app.py` file, is that I can add some `args` to have a flexible environment, that gives me the possibility to switch between development and production in one command:
	
	
	# for development env
	python run.py --env=devel

	# for production env
	python run.py --env=prod 
	

Using a `run.py` is not an issue for the participants because, refering to point 2 of this document, they'll just copy the following lines of code:

	
	from .yourapp import app

	def run(host):
	    app.run(debug=True)

	if __name__ == '__main__':
	    run()
	


##### __3.4. Static files__

We’ll create a directory for our static files called `static` inside our application package. How you organize the files in `static/` is a matter of personal preference, however, I suggest having the following hierarchy:

	
	static/
    css/
        lib/
            bootstrap.css
        *.css
    js/
        lib/
            jquery.js
        *.js
    img/
        *.svg
        *.ico
        *.png
	

This is a simple way of keeping all the things separated, and easy to modify.

##### __3.5. Template files__

As you can see `Flask` is really flexible of where things are located, and the same works with `templates`, but keeping the templates in the package directory has its benefits, when having to route them.

	
	myapp/
	    __init__.py
	    models.py
	    views/
	    templates/
	    static/
	run.py
	

The structure of the templates directory parallels the structure of our routes. The template for the route myapp.com/admin/analytics is templates/admin/an-alytics.html. 

	
	templates/
	    layout.html
	    index.html
	    about.html
	    profile/
	        layout.html
	        index.html
	    photos.html
	    admin/
	        layout.html
	        index.html
	        analytics.html
	

There are also some extra templates in there that won’t be rendered directly. The layout.html files are meant to be inherited by the other templates.

##### __3.6. Requirements file__

The `requirments.txt` file stores the names and versions of all the packages that are needed to run the project well.
It is located at the upper most folder of the project.

To create a `requirements.txt` file use the following command:
	
	
	pip freeze > requirements.txt
	
__Note:__ __Make sure you have activatec your virtualenv for the project.__


