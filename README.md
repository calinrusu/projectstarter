# Simple web project starter

A simple script to create a starting structure for a web project.

## Requirements

- PHP 8.0+

## Project structure

	/myproject
		starter
		/app
			bootstrap.php
			/config
				app.php
				database.php
			/includes
				db.php
				functions.php
				csrf.php
				validation.php
			/lib
			/views
				/layouts
					head.php
					footer.php
				/partials
					navbar.php
				/pages
					index.php
		/public
			index.php
			/assets
				/css
					app.css
				/js
					app.js
				/img

## Usage

Create an empty directory for your new project. E.g. "mkdir ~/myproject".
Copy the starter php script into your new project directory.
cd into your new project directory and run the php starter script.
- To list available arguments:
	php starter help
- To install the project structure:
	php starter install
	It will prompt to install PHPMailer for sending emails via SMTP. Type "yes" to confirm or just press Enter to skip PHPMailer.
	After the project structure has been created you will have to edit the config files: /app/config/app.php and /app/config/database.php to define your own global variables. Set DB_USE to 0 if you don't plan to use a MySQL database (by default it's set to 1 and that will require a database connection when bootstraping the app).
- To delete an existing project installation:
	php starter delete
	It will prompt if you are sure, type "yes" to confirm deletion or press Enter to skip.
- To create a new web page (with html output):
	php starter makeview "yourpagename"
	This will create yourpagename.php in the /public directory and the corresponding file in the /app/views/pages directory.
- To create a new php page (script, no html output):
	php starter makepage "yourscriptname"
	This will create yourscriptname.php in the /public directory with all the requires but without including the /app/views component. It will only do php processing with no html output.
