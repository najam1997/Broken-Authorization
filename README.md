# Vulnerability: Weak / Broken Authentication

## Pre-Requisites
1. Basic understanding of Web Apps and authentication is a must.
2. Make sure you have Node JS installed.
3. For Windows, you'll have to download and install **node** as well as **npm** from browser. For Linux, following command would do:
```
sudo apt-get install nodejs
sudo apt-get install npm
```
4. Download and install mongodb using the following [link](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-ubuntu/#std-label-install-mdb-community-ubuntu).
## Steps for setup

1. Open CMD/Terminal on your desktop.
2. Run the following command: 
```
git clone https://gitlab.com/nusk-labs/ctf/broken-authorization.git
```
3. This will clone the Repo.
4. Then we need to install required libraries and start our Node JS App, for that run:
```
cd broken-authorization
npm install
```
5. Run the following command to start and check whether DB is active:
```
sudo systemctl start mongod
sudo systemctl status mongod
```
If mongo has started, run the following command:
```
mongosh
```
6. Note the link the DB is connected on, it'll look like this: `mongodb://127.0.0.1:27017/`
then paste it in [dbURI](https://gitlab.com/nusk-labs/ctf/broken-authentication/-/blame/main/app.js?ref_type=heads#L18) variable in the app.js file (Note: Change it only if it isn't connecting on default link).

7. Afterwards, run the following command:
```
node app.js
```
8. Start the challenge thereafter, for which you'll have to go on the link http://127.0.0.1:3000 on a browser.

## Vulnerability difficulty and Exploitation details
1. Difficulty: Easy
2. Exploitation: Signup 2 users, first with the email of admin@admin.com and second with your own email. Login with your own email and perform account takeover of the admin user.
