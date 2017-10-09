# First-Bot
First one.  Tester.
var Discord = require('discord.io');
var logger = require('winston');
var auth = require('./auth.json');
// Configure logger settings
logger.remove(logger.transports.Console);
logger.add(logger.transports.Console, {
    colorize: true
});
logger.level = 'debug';
// Initialize Discord Bot
var bot = new Discord.Client({
   token:MzY2NzQxMTAwNDAyMDQ5MDQ1.DLxR4g.ycTCuniHAlHAtKbxEkSKpMtYrkA,
   autorun: true
});
bot.on('ready', function (evt) {
    logger.info('Connected');
    logger.info('Logged in as:  Bot1#3834');
    logger.info(Bot1#3834 + ' - (' + 366741100402049045 + ')');
});
bot.on('message', function (user, userID, channelID, message, evt) {
    // Our bot needs to know if it will execute a command
    // It will listen for messages that will start with `!`
    if (message.substring(0, 1) == '!') {
        var args = message.substring(1).split(' ');
        var cmd = args[0];
       
        args = args.splice(1);
        switch(cmd) {
            // !Hello, bot
            case 'Hello, bot':
                bot.sendMessage({
                    to: channelID,
                    message: 'Greetings, human'
                });
            break;
          args = args.splice(1);
        switch(cmd) {
            // !LOL
            case 'LOL':
                bot.sendMessage({
                    to: channelID,
                    message: 'Ha ha, that's funny. XD'
                });
            break; 
          args = args.splice(1);
        switch(cmd) {
            // !Switchlevel1
            case 'Switchlevel1':
                bot.sendMessage({
                    to: channelID,
                    message: 'The owner may be unavailable at the moment.  I will notify @Switchlevel1#5417'
                });
            break;
          
          // Just add any case commands if you want to..
         }
     }
});
