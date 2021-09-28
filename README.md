# inst 
This is a Information Gathering tool 
this tool is special making for Instagram.

# Installation

git clone https://github.com/Khalidhusain786/inst.git

cd inst

python3 -m venv venv

pip install -r requirements.txt

Now seen carefully, open the config folder and  type ls

Remove  settings.json

Type ls and write nano credentials.ini

fill the any username and password and than click ctrl+x and save 

If you not use this option type of config folder json threw

Simply write make setup and fill username and password and save

Run the main.py script in one of two ways:

As an interactive prompt python3 main.py <target username>
  
Or execute your command straight away python3 main.py <target username> --command <command>
  
  
 # Docker Quick Start
  
This section will explain how you can quickly use this image with Docker or Docker-compose.

Prerequisites
Before you can use either Docker or Docker-compose, please ensure you do have the following prerequisites met.

Docker installed - link

  Docker-composed installed (if using Docker-compose) - link

  Credentials configured - This can be done manually or by running the make setup command from the root of this repo
Important: Your container will fail if you do not do step #3 and configure your credentials

  
  
  Download the latest version: git pull origin master

  
  
