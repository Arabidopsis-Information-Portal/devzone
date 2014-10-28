## Acquire necessary accounts
You must have two functioning sets of credentials to develop AIP content. Please sign up for and activate these accounts now.

   * [Araport.org](https://www.araport.org/user/register)
   * [Github.com](https://github.com/join)


## Dependencies
The list of requirements to start AIP development is relatively minimal, but you do need access to and familiarity with a few things on your local system. We assume that you are developing in Linux or Mac OS X (because they are UNIX-like), but all of these tools are also available and usable under Windows 7 (or better). 

   * Git
   * Agave CLI
   * Dependency stack for the App SDK
   * Python + virtual environment, pip
   * cURL
   * Decent text editor: Sublime (emacs for the brave)
   * Optional: an in-browser REST client

### Step 1. git

### Step 2. Node.js and other Apps SDK dependencies

### Step 3. AgaveAPI command line

### Step 4. Python + virtual environments and pip
(http://docs.python-guide.org/en/latest/starting/install/linux/)

### Step 5. Choosing a text editor

## Brush up on the basics

* HTML/Javascript/CSS
    * [Learn jQuery](http://learn.jquery.com/) - At least read JavaScript 101 :-)
    * [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
* Git and Github
    * [Pro Git](http://git-scm.com/book/en/v2) - Read Chapters 1, 2, 3, and 6
* cURL
    * [cURL Tutorial](http://curl.haxx.se/docs/httpscripting.html) - Read up on at least the followings flags -s -k -u -L -X -F and -H
* Python
    * [virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/) - Manage dependency chaos with virtualenvs
    * [pip](https://pip.pypa.io/en/latest/) - Installing dependencies
* REST
    * [M. Elkstein's unparalleled REST Tutorial](http://rest.elkstein.org/)
* JSON
    * [Introducing JSON](http://json.org/) - Make sure you understand JSON syntax 
* Markdown
    * [Original Markdown spec](http://daringfireball.net/projects/markdown/) - Learn at least the basic tags here
    * [GitHub flavored Markdown](https://help.github.com/articles/github-flavored-markdown/) - AIP uses this dialect for integration with Github

## More Resources
* [Simple Daily Git Workflow](https://www.sonassi.com/wp-content/uploads/2012/07/simple_git_daily_workflow.pdf) - Print it out. Tape it up over your desk. 
* [OAuth2 Simplified](http://aaronparecki.com/articles/2012/07/29/1/oauth2-simplified) - AIP uses OAuth2 for authentication. In addition to our specific documentation, here's a n overview.
* [JSON Schema](http://json-schema.org/) - AIP will soon publish and adopt JSON schemas for its server responses. Here's a primer.  
* [JSONlint.com](http://jsonlint.com) - An online JSON Validator
* [Roy Fielding's REST Dissertation](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm)
* [Dillinger Markdown Editor](http://dillinger.io/) - Handy if you're learning Markdown for the first time
* [About Cross-Origin Resource Sharing](http://enable-cors.org/) - AIP provides CORS for all data services, including ones you build with us
* [Switching to HTTPS](https://www.eff.org/https-everywhere/deploying-https) - AIP uses only strong HTTPS for data transfer. Here's how and why we do this.