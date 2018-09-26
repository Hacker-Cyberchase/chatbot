    // Required Applications
    var chef_bot = require('slackbots');
    var Botkit = require('botkit');
    var controller = Botkit.slackbot();
    var bot = new chef_bot({
        token: 'xoxb-TOKEN ID HERE', // Added chef bot token
        name: 'Chef Bot'
    });


    bot.on('start', function() {

        var params = {
        icon_emoji: ':male-cook:'
    };

    // my defined channel, where chef bot exists.
    bot.postMessageToChannel('chatbot_test_chat', 'Hi there. Lets cook something great today. Would you like to learn a new recipe      together? Reply with Yes or No.', params);



    });

    // trying to the bot something to listen for and reply with bot.reply message
            controller.hears('Yes', 'message_received',function(bot,message)  {
            bot.postMessageToChannel('Awesome! Lets get cooking...')


    });
