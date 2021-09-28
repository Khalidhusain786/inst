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

  
  # Docker

  If docker is installed you can build an image and run this as a container.

# Build:

docker build -t osintgram .

# Run:

docker run --rm -it -v "$PWD/output:/home/osintgram/output" osintgram <target>

  The <target> is the Instagram account you wish to use as your target for recon.

  The required -i flag enables an interactive terminal to use commands within the container. docs

  The required -v flag mounts a volume between your local filesystem and the container to save to the ./output/ folder. docs

  The optional --rm flag removes the container filesystem on completion to prevent cruft build-up. docs

  The optional -t flag allocates a pseudo-TTY which allows colored output. docs

# Using docker-compose

  You can use the docker-compose.yml file this single command:

docker-compose run osintgram <target>

  Where target is the Instagram target for recon.

Alternatively you may run docker-compose with the Makefile:

make run - Builds and Runs with compose. Prompts for a target before running.

  # Makefile (easy mode)

  For ease of use with Docker-compose, a Makefile has been provided.

Here is a sample work flow to spin up a container and run osintgram with just two commands!

make setup - Sets up your Instagram credentials

  make run - Builds and Runs a osintgram container and prompts for a target

  Sample workflow for development:

make setup - Sets up your Instagram credentials

  make build-run-testing - Builds an Runs a container without invoking the main.py script. Useful for an it Docker session for development

  make cleanup-testing - Cleans up the testing container created from build-run-testing

  Development version computer

  To use the development version with the latest feature and fixes just switch to development branch using Git:

git checkout development

and update to last version using:

git pull origin development

Updating arrow_down

  To update Osintgram with the stable release just pull the latest commit using Git.

Make sure you are in the master branch running: git checkout master

  Download the latest version: git pull origin master

  
  
