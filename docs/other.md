# Welcome to MkDocs

For full documentation visit [mkdocs.org](http://mkdocs.org).

##Installation
In order to install MkDocs you'll need Python installed on your system, as well as the Python package manager, pip. You can check if you have these already installed like so:

	$ python --version
	Python 2.7.2
	$ pip --version
	pip 1.5.2
MkDocs supports Python 2.6, 2.7, 3.3, 3.4 and 3.5.

On Windows we recommend that you install Python and pip with [Chocolatey](https://chocolatey.org/) .

Install the mkdocs package using pip:

	pip install mkdocs
You should now have the mkdocs command installed on your system. Run mkdocs --version to check that everything worked okay.

	$ mkdocs --version
	mkdocs, version 0.15.2
	
------------------------------------
##Getting started
Getting started is super easy.

	mkdocs new my-project
	cd my-project

or you can do this .

	git clone https://github.com/ETENG-WIKI/ETENG-WIKI.git
	cd  	ETENG-WIKI
Let's take a moment to review the initial project that's been created for us.

The initial MkDocs layout

There's a single configuration file named mkdocs.yml, and a folder named docs that will contain our documentation source files. Right now the docs folder just contains a single documentation page, named index.md.

MkDocs comes with a built-in webserver that lets you preview your documentation as you work on it. We start the webserver by making sure we're in the same directory as the mkdocs.yml config file, and then running the mkdocs serve command:

	$ mkdocs serve
Running at: http://127.0.0.1:8000/
Open up http://127.0.0.1:8000/ in your browser, and you'll see the index page being displayed:

---------------------------------

##Adding pages
Go ahead and edit the docs/index.md document, and change the initial heading to MkLorum, then reload the site in your browser, and you should see the change take effect immediately.

Let's also add a second page to our documentation:

	curl 'jaspervdj.be/lorem-markdownum/markdown.txt' > docs/about.md
We'd like our documentation site to include some navigation headers, so we'll edit the configuration file and add some information about the order and title to use for out headers:

	site_name: MkLorum
	pages:

#	- Home: index.md
	- About: about.md
Refresh the browser and you'll now see a navigation bar with Home and About headers.

--------------------------------------------

##Theming our documentation
While we're here can also change the configuration file to alter how the documentation is displayed. Let's go ahead and change the theme. Edit the mkdocs.yml file to the following:

site_name: MkLorum
pages:
- Home: index.md
- About: about.md
theme: readthedocs
Refresh the browser again, and you'll now see the ReadTheDocs theme being used.

--------------------------------------
## Building the site
That's looking good. We're ready to deploy the first pass of our MkLorum documentation now. Let's build the documentation.

	mkdocs build
This will create a new directory, named site. Let's take a look inside the directory:

	ls site
	about css fonts img index.html js
Notice that our source documentation has been output as two HTML files named index.html and about/index.html. We also have various other media that's been copied into the site directory as part of the documentation theme.

If you're using source code control such as git you probably don't want to check your documentation builds into the repository. Add a line containing site/ to your .gitignore file.

	echo "site/" >> .gitignore
If you're using another source code control you'll want to check it's documentation on how to ignore specific directories.

After some time, files may be removed from the documentation but they will still reside in the site directory. To remove those stale files, just run mkdocs with the --clean switch.

	mkdocs build --clean
---------------------------------------

## Deploying
The documentation site that we've just built only uses static files so you'll be able to host it from pretty much anywhere. [GitHub project](https://help.github.com/articles/creating-project-pages-manually/) pages and Amazon S3 are good hosting options. Upload the contents of the entire site directory to wherever you're hosting your website from and you're done. For specific instructions for a number of common hosts, see the [Deploying your Docs](http://www.mkdocs.org/user-guide/deploying-your-docs/) page.

--------------------------------

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs help` - Print this help message.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.