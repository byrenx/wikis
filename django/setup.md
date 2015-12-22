## Setup django in Linux Environment:

premise: pip must be install first to install type in the terminal
         sudo apt-get install python-pip

To install django and other db connector and etc.

1. Install python-dev to enable MySQLdb: apt-get install python-dev

2. You can install through pip, write these contents in requirements.txt
   Django or Django == <version> if you want to be specific with the version u want to install
   MySQL-python : for mysql-python connector
   Psycopg : for postgresql
   
   so the content of your requirements.txt:

   Django
   MySQL-python
   Psycopg
   #...any libraries you want here

3. then, install
   sudo pip install -r requirements.txt

4. then, your good to go
