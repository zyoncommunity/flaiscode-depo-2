const Discord = require('discord.js');
const generator = require('generate-password');


exports.run = function(client, message, args) {
    var uzunluk = args.slice(0).join(' ');
   if (uzunluk.join(' ').length > 1) return message.channel.send(":no_entry: En fazla 1'den fazla karakterli şifre oluşturabilirsiniz.")
    if (!uzunluk) return message.reply('Bir uzunluk belirt. **Doğru Kullanım**: ins!şifre <uzunluk>')
    var password = generator.generate({
        length: uzunluk,
        numbers: true,
    })
    message.channel.send(password);
};  

exports.conf = {
  enabled: true, 
  guildOnly: true, 
  aliases: [],
  permLevel: 0 
};

exports.help = {
  name: 'şifre', 
  description: 'Rastgele bir şifre oluşturur.',
  usage: 'şifre <uzunluk>'
};