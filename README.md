# Vulnerability: Weak / Broken Authentication

## Pre-Requisites
1. Basic understanding of Web Apps and authentication is a must.
2. Make sure you have Node JS installed.
3. For Windows, you'll have to download and install **node** as well as **npm** from browser. For Linux, following command would do:
```
sudo apt-get install nodejs
sudo apt-get install npm
sudo apt-get install mongodb
sudo apt-get install mongoose
```

## Steps for setup

1. Open CMD/Terminal on your desktop.
2. Run the following command: 
```
git clone https://gitlab.com/nusk-labs/ctf/broken-authentication.git
```
3. This will clone the Repo.
4. Then we need to install required libraries and start our Node JS App, for that run:
```
cd broken-authentication
npm install
```
5. Run the following command to check whether DB is active:
```
mongosh
```
6. Note the link the DB is connected on and paste it in **dbURI** variable in the app.js file.
7. Then run the following command:
```
node app.js
```
10. Start the challenge thereafter, for which you'll have to go on the link http://127.0.0.1:3000 on a browser.

## Vulnerability difficulty and Exploitation details
1. Difficulty: Easy
2. Exploitation: Register a user through the email admin@admin.com and perform account takeover.
