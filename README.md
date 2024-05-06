Download the zip file and extract.
Open the folder using Visual Studio Code. 
Download mysql on your system and download the extension on vs code.
Create a super user.
On the VS Code, type the command. Replace the *username* with your save username of super user.
  	**mysql -u *username* -p**
If required create a new user using
  **CREATE USER '*username*'@'localhost' IDENTIFIED BY '*password*';**
Create new database named 'reservations
  **CREATE DATABASE reservations;**
If database already exists, check using **SHOW DATABASES;**
Drop using **DROP DATABASE reservations;**
Or give new name for the table and change in the settings.py the *'NAME'* in DATABASES.
Now give the user, access to this database using
  **GRANT ALL PRIVILEGES ON reservations.\* TO '*username*'@'localhost';**
  **FLUSH PRIVILEGES;**
In the terminal now, make migrations using command
  **python manage.py makemigrations**
  **python manage.py migrate**
Run the command below to get to the website.
  **python manage.py runserver**
Follow the website at http://127.0.0.1:8000/
THANK YOU
