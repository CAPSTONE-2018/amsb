# Setting up Development Environment
Since there are configuration issues on our server which prevent us from using the CodeIgniter framework, you will need to use [Cloud9](https://c9.io/) for your development environment. I will send you an invitation to join my team, so that you are able to set-up an account without a credit card.  Be sure to use the Chrome browser when working with in Cloud9.

## Initial set up.
1. Create a new blank workspace.  
1. Clone the AMSB repository to the root directory: `git clone https://github.com/freeformradio/amsb.git`
1. Start Apache webserver `apachectl start`
1. Start the MySql database server `mysql-ctl start`

## Database set-up
1. You will work at the the MySQL command line.  You can access the command line with `mysql -u username` where `username` is your cloud9 username.

1. Create the database:  `CREATE DATABASE amsb_amsb;`

1. Use the mysql database:  `USE mysql`

1. Create the database user:  `CREATE USER  'bigGuy'@'localhost'  identified by 'mypassword';`

1. Give usage privileges to the database user:  `GRANT SELECT, INSERT, UPDATE, DELETE on amsb_amsb.* TO 'bigGuy'@'localhost';`

1. Use the AMSB database: `USE amsb_amsb`

1. Load the test data from the GitHub repository:
`SOURCE /home/ubuntu/workspace/amsb/MostRecentAMSB.sql`

1. Add a new user to the amsb_amsb.  This script creates a user with username *capstone* and password *mypassword*.<br/>
  `insert into admin_users values(null, "capstone","c858f97755cd5a6a6d23ae02cd140fcba0a07abb", 2,   0, 0, 1, 0 , 0 , 0 , 0 , 0 , 0 , "Capstone", "Student", ""  , ""  , "" , "capstone@lewisu.edu" ,""  , "" , "" ,"" , "" ,"" ,"" ,  0 ,  0 , "0000-00-00 00:00:00", CURRENT_TIMESTAMP , 1 , 1)`

1. Exit the MySQL command line: `exit`

## Run the application
1. Using the file tree on the right Navigate to the `/amsb/ci/index.php` and click to open the file.
1. Press the Run button at the top of the page.  This will open a console window at the bottom of the page.
1. Click on the URL in the console.  This should open another tab in your browser with the running application.
1. Log-in using *capstone* and *mypassword*
1. To stop the application, close the tab and then press the stop button above the console output in Cloud9

# Tutorial
Work through the CodeIgniter tutorial in the tutorial folder in the user_guide folder.  Double clicking on index.html should open the tutorial in your default browser.  
