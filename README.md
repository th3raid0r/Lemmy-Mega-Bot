# Mega Bot (Aka the megaphone bot)
A lemmy bot that watches rss feeds and posts new posts from them in communities 

This bot is made for the https://programming.dev/ communities but the source code can be modified to accomodate any community

## Prerequisites
- You need to have installed node.js or Docker in order to run the bot

## Setup with Node.js (Option 1)
1. Clone the repository
2. Create an account in the instance you want the bot to have as its home (just make a regular user)
3. Create a file called .env in the bot folder and give it values in this format with the data in the quotes (dont add the slashes or the part after the slashes)
```
LEMMY_INSTANCE="" // The instance the bot account is in
LEMMY_USERNAME="" // The bot username
LEMMY_PASSWORD="" // The bot password
```
4. Change the data in config.yaml based on what you want set. Set the communities and feeds you want here
5. Open a terminal in the bot folder and run `npm install` to install dependendies and then `node main.js` to run the bot (whenever you want to start the bot again you can just do ctrl+c to interrupt the process and node main.js to start the bot)

I recommend installing something like [forever.js](https://www.npmjs.com/package/forever) which will make it start back up again if it errors at some point

If you run into issues feel free to dm me on Matrix [here](https://matrix.to/#/@ategon:matrix.org)

## Setup with Docker (Option 2)
1. Clone the repository
2. Create an account in the instance you want the bot to have as its home (just make a regular user)
3. Create a file called .env in the bot folder and give it values in this format with the data in the quotes (dont add the slashes or the part after the slashes)
```
LEMMY_INSTANCE="" // The instance the bot account is in
LEMMY_USERNAME="" // The bot username
LEMMY_PASSWORD="" // The bot password
```
4. Change the data in config.yaml based on what you want set. Set the communities and feeds you want here
5. In the project directory build the docker image by running `docker build -t <your name>/<desired_image_name>` and then launch a new container with `docker run <your name>/<desired_image_name>`
