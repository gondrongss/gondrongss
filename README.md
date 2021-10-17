- 👋 Hi, I’m @gondrongss
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
gondrongss/gondrongss is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
const http = require('http');
const express = require('express');
const app = express();
app.get("/", (request, response) => {
  console.log('Pinging');
  response.sendStatus(200);
});
app.listen(process.env.PORT);
setInterval(() => {
  http.get(`http://${process.env.PROJECT_DOMAIN}.glitch.me/`);
}, 280000);

const Discord = require('discord.js');
const client = new Discord.Client();

client.on('ready', () => {
  console.log("saya telah online");
});

client.on('message', async  message => {
  if (message.content === "Terserah mau isi apa") {
message.channel.send('Terserah mau isi apa');
  }
});

client.login(process.env.BOT)

//package.json copy yang dibawah ini!

{
  "name": "Vins",
  "version": "1.0.0",
  "main": "bot.js",
  "scripts": {
    "start": "node bot.js"
  },
  "dependencies": {  
    "discord.js": "^12.2.0",
    "request": "2.81.0",
    "express": "^4.16.3",
    "https": "^1.0.0",
    "foreach-timeout": "2.0.2",
    "express": "^4.16.3",
    "map": "^1.0.1"
  } 
}
