# Discord Auth Bot V2

Discord Auth Bot V2 is a new and improved version of my original discord auth bot. This project is written with the Node.js framework and React as opposed to using java, making it much easier to setup.

My goals for this project:

- Easier to setup
- Nice, browser based UI to manage server (React)
- Easy to integrate with discord

## Prerequisites

- Make sure you have npm installed (https://www.npmjs.com/get-npm)
- Make sure you have yarn installed (https://yarnpkg.com/en/)
- Make sure you have gatsby installed (https://www.gatsbyjs.org/docs/)
- Make sure ports 8000 and 8001 are available

## Installation

Run the following commands to install

- Quick note: If you are on a mac or linux machine, you may need to run the npm install command with sudo in front of it (i.e. sudo npm install)

```sh
cd [file path of where this project is stored]
npm install
npm start
```

## Setup

- Go to https://discordapp.com/developers/applications/
- Create a new bot and name it what you want and give it an icon if you would like
- Go to Bot on the left panel and click create bot
- Click reveal token, copy this token and once you launch the program (follow instructions below) go to the settings page and save it in the field marked 'Token'

## Usage

The bot does not yet have all the functionality I would like it to have, but for the time being here is how to use it:

- Users can DM the bot with !help for how to activate a key with the bot
- Users can DM the bot with !activate <<key>> to activate a key with the bot
- Users can DM the bot with !deactivate <<key>> to deactivate a key with the bot

- To open the dashboard, open a browser with: http://127.0.0.1:8000/
- For the time being, you can not set the token, unbind user keys, nor generate keys from the dashboard, but in the meantime you can see in real time users activating and deactivating keys from the manage keys section of the dashboard

- To add a key, simply open the src/info/users.json file and add a key in the format: "THE KEY YOU WANT":"none"
  - Make sure that the value is none for the key to allow a user to bind to that key
- To deactivate a key just search for the key in the same json file and in the value section it should be the user's username. Replace that with "none" to deactivate it manually

- (Optional) In the settings page, you are able to set a role to add to authenticated users and a role to remove from authenticated users:
  - Role to add: When the user activates their key, this role will be applied to them (i.e. a role showing that they are authenticated)
  - Role to remove: When the user activates their key, this role will be removed from them (i.e. some sort of unauthenticated role)
  - Remember, when you enter these roles they are case sensitive and must match EXACTLY what they say on discord
  - Also, when you create these roles, go to your server settings and then the roles tab and make sure that the bot's role is higher than the roles you are trying to add and remove, if they are not simply drag them into the proper order

## TODO:

- [x] Finish key activating and deactivating through discord
- [x] Unbind keys through dashboard
- [x] Generate keys through dashboard
- [x] Add role updating functionality
- [ ] Add custom key creation
- [ ] Add credit card provider implementation
- [ ] Add keys that can expire at certain times

## Questions?

If you have any questions, feel free to message me on twitter @DynxSZN
