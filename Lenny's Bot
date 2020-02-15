const Discord = require("discord.js");
const config = require("../config.json");
module.exports.run = async(bot, message, args) => {
    message.delete();
    // let args = message.content.toLowerCase().substring(prefix.length).split(" ");
    let user = message.mentions.members.first() || message.guild.members.get(args[0]);
    const why = args.slice(1).join(' ');

    if(!message.member.hasPermission(["BAN_MEMBERS", "ADMINISTRATOR"])) return message.channel.send("You do not have permission to perform this command!")
    if (!user) {
        message.channel.send('Wen möchtest du denn erinnern? Gebe es an.')
    } else {
        if (!why) {
            message.channel.send('Du musst einen Grund angeben, ohne wäre es sinnlos.')
        }
        
        const embed = new Discord.RichEmbed()
        .setColor('#cfc607')
        .setTitle('**Verwarnung Stufe 1 [Erinnerung] :notepad_spiral: **')
        .setDescription(`
Du hast soeben eine Erinnerung erhalten.
Beachte den Grund, achte auf dein Auftreten und wende dich **notfalls** an den Moderator.
 
 __Was ist eine Erinnerung?__
> Eine Erinnerung macht eigentlich das was der Name sagt: Dich an Regeln erinnern.
> Erinnerungen sind unter einer Verwarnung und können beliebig oft angewendet werden. 
> Du brauchst keine Angst haben, Fehler passieren jedem also auch dir. 
  
            ___Informationen über die Erinnerung___

 __Moderator__
 ${message.author}

 __Grund:__         
 ${why}`)

  

.setColor('#cfc607')
.setThumbnail(`https://cdn.discordapp.com/attachments/655736154687275014/677548210419662848/emoji.png`)
.setFooter(`Eine freundliche Erinnerung für dich`)
.setTimestamp()
.setThumbnail ('')
let channel = message.guild.channels.find(`name`, "🔓-ban-gründe");
channel.send(embed)
        user.send(embed)
    }
}

module.exports.help = {
    name: 'v1'
}
