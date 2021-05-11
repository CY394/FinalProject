# FinalProject
FinalProject
#################################################################
#                                                               #
#                                                               #
#             WELCOME TO BARBER SHOP AS A SERVICE               #
#                                                               #
#                                                               #
#################################################################

To Run this program on your local machine, follow the below steps.

All of the follwing commands are executed on a Virtual Machine
running the Ubuntu Linux Distribution. This is recommended. These
commands will be run in the Command Line Interface.

# Begin by getting the postgres dependencies installed
# Get Postgres Server
# In your command line at the root directory, execute:

sudo apt-get install postgresql postgresql-contrib
sudo -i -u postgres

# This commands enters the psql terminal environment
psql

# create a user in the database
CREATE user docker with password ‘docker’;

# create the go barber database
CREATE database gobarber;

# Exit the psql terminal environment
Exit

###### CREATE SERVER FOR WEB APP #######
# Create your server to host your NodeJS App
# Run the following commands

# Installs Nodejs
Sudo apt install nodejs

# clone the repository for the project
Git clone https://github.com/CY394/FinalProject.git

# change directory to the cloned repo
cd go-barber-app

# download necessary packages with npm
npm i

# migrate packages to database
npx sequelize db:migrate

# start server to run web app
npm start