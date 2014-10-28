# Getting Started with AIP Development

Welcome aboard. We're so happy you are interested in joining the community of [AIP](https://www.araport.org) developers. We've tried to make it reasonably straightforward for you to get in and start contributing right away. Please work through this 'getting started' guide and consider also joining the [Araport-Developers Google Group](https://groups.google.com/forum/#!forum/araport-developers). 

## Acquire necessary accounts
You need two sets of credentials to develop AIP content. Please sign up for and activate these accounts now.

   * [Araport.org](https://www.araport.org/user/register)
   * [Github.com](https://github.com/join)

## Install and configure dependencies
The list of requirements to start AIP development is relatively minimal, but you do need a few things installed. You also need to be comfortable using them! We assume that you are developing in Linux or Mac OS X (because they are UNIX-like), but all of these tools are also available and usable under Windows 7 (or better). 

   * Git
   * Agave CLI
   * Node.js and npm
   * Python + virtual environment, pip
   * cURL
   * A good text editor
   * Optional: an in-browser REST client

### Step 1. git

1. [Installation](http://git-scm.com/book/en/v2/Getting-Started-Installing-Git) - Follow the instructions!
2. [Configuration](http://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup) - Make sure to run through the setup, too
3. Ensure that git is accessible in your $PATH

### Step 2. Node.js and npm

* [Download an installer](http://www.nodejs.org/download/)
* Or, [use a package manager](https://github.com/joyent/node/wiki/Installing-Node.js-via-package-manager)

### Step 3. AgaveAPI command line

Installation
```
git clone https://bitbucket.org/taccaci/foundation-cli
# then, add foundation-cli/bin to your PATH
```

Initialize the Agave CLI tools. You only need to do this once!
```
tenants-init
Please select a tenant from the following list:
[0] araport.org
[1] iplantc.org
[2] irec
[3] vdjserver.org
[4] wso2.agave.staging
[5] xsede.org
[6] xsede.org.staging
Your choice [2]: 0
You are now configured to interact with the APIs at https://api.araport.org/
```

Create an OAuth2 client and cache its key and secret locally. You only need to do this once!
```
clients-create -S -N araport_cli
API username : YOUR_ARAPORT_USERNAME
API password:
Successfully created client araport_cli
key: Q23DP_OASIsWxzwa5Ijh_5tUYw_H
secret: pDDGdirnNTsOuW4Yh6EwaCMsU6ga
```

### Step 4. Python + virtual environments and pip

Follow all the steps in the guide for your operating system. After installing virtualenv and pip, install virtualenvwrapper

* [Installing Python on Mac OS X](http://docs.python-guide.org/en/latest/starting/install/osx/)
* [Installing Python  on Linux](http://docs.python-guide.org/en/latest/starting/install/linux/)
* [Installing Python  on Windows](http://docs.python-guide.org/en/latest/starting/install/win/)
* [Installing virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/install.html)

### Step 5. Install cURL

Check to see if cURL is on your system already. If it's not, install it using a package manager or by [downloading it from the cURL web site](http://curl.haxx.se/download.html). Make sure it's in your $PATH after installation.

### Step 6. Choose a text editor
You have many to choose from! If you don't have a favorite yet, might we suggest
* [Atom](https://atom.io/) - Free, powerful, extensible, and open source
* [Sublime Text](http://www.sublimetext.com/) - It's 70 bucks but hey, you're on a $2000 laptop, right?
* [TextWrangler](http://www.barebones.com/products/textwrangler/) - Free-as-in-beer and awesome, but Mac OS X only.
* EMACS or vim - Non-GUI editors but extremely flexible

### Step 6. Optional REST client

* [Google Chrome: Advanced REST Client](https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo?hl=en-US)
* [Mozilla Firefox: RESTClient](https://addons.mozilla.org/en-US/firefox/addon/restclient/)

## Brush up on the basics
We've tried to distill down the bare minimum you will need to be productive developing AIP apps and data services. Depending on your experience, your mileage may vary.

* HTML/Javascript/CSS
    * [Learn jQuery](http://learn.jquery.com/) - At least read JavaScript 101 :-)
    * [Mozilla Developer Network (MDN)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
* Git and Github
    * [Pro Git](http://git-scm.com/book/en/v2) - Read Chapters 1, 2, 3, and 6
* cURL
    * [cURL Tutorial](http://curl.haxx.se/docs/httpscripting.html) - Read up on at least the followings flags -s -k -u -L -X -F and -H
* Python
    * [virtualenv](http://docs.python-guide.org/en/latest/dev/virtualenvs/) - Manage dependency chaos with virtualenvs
    * [virtualenvwrapper](http://virtualenvwrapper.readthedocs.org/en/latest/) - Swap between virtual environments. Very handy!
    * [pip](https://pip.pypa.io/en/latest/) - Installing dependencies
* REST
    * [M. Elkstein's unparalleled REST Tutorial](http://rest.elkstein.org/)
* JSON
    * [Introducing JSON](http://json.org/) - Make sure you understand JSON syntax 
* Markdown
    * [Original Markdown spec](http://daringfireball.net/projects/markdown/) - Learn at least the basic tags here
    * [GitHub flavored Markdown](https://help.github.com/articles/github-flavored-markdown/) - AIP uses this dialect for integration with Github

## More Resources 
* [AIP Developer Zone](https://www.araport.org/devzone/) - Developer HQ for creating AIP apps and services. Home of SDKs, tutorials, examples, and more
* [AIP Project Github](https://github.com/Arabidopsis-Information-Portal) - For better or worse, it's all out there
* [Thalemine User Guide](https://www.araport.org/thalemine/user-guide) - Start here if you're new to Intermine. API documentation coming soon!
* [Jbrowse documentation](http://jbrowse.org/) - Our genome browser of choice
* [Simple Daily Git Workflow](https://www.sonassi.com/wp-content/uploads/2012/07/simple_git_daily_workflow.pdf) - Print it out. Tape it up over your desk. 
* [OAuth2 Simplified](http://aaronparecki.com/articles/2012/07/29/1/oauth2-simplified) - AIP uses OAuth2 for authentication. In addition to our specific documentation, here's an overview.
* [JSON Schema](http://json-schema.org/) - AIP will soon publish and adopt JSON schemas for its data service responses. Here's a primer.  
* [JSONlint.com](http://jsonlint.com) - An online JSON Validator
* [Roy Fielding's REST Dissertation](http://www.ics.uci.edu/~fielding/pubs/dissertation/top.htm)
* [Dillinger Markdown Editor](http://dillinger.io/) - Handy if you're learning Markdown for the first time
* [About Cross-Origin Resource Sharing](http://enable-cors.org/) - AIP provides CORS for all data services, including ones you build with us
* [Switching to HTTPS](https://www.eff.org/https-everywhere/deploying-https) - AIP uses only strong HTTPS for data transfer. Here's how and why we do this.
