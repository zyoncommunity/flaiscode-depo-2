  if (message.channel.type !== 'dm') {
    const ozelmesajkontrol = new Discord.RichEmbed()
    .setColor(0x36393E)
    .setAuthor(message.author.username, message.author.avatarURL)
    .setFooter(`${client.user.username} - Tüm hakları saklıdır.`, client.user.avatarURL)
    .setDescription('DM kutuna bilgileri yolladım.');
    message.channel.sendEmbed(ozelmesajkontrol) }
    const pingozel = new Discord.RichEmbed()
    .setColor(0x36393E) 
    .setAuthor(message.author.username, message.author.avatarURL)
    .setFooter(`${client.user.username} - Tüm hakları saklıdır.`, client.user.avatarURL)
    .addField("BAŞLIK", 'YAZI');  
    console.log(`LOG: ${message.author.username} tarafından !özelmesaj komudu kullanıldı.`)
    return message.author.sendEmbed(pingozel)
};