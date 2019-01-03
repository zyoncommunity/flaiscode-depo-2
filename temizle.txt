if (message.content.toLowerCase() === prefix + 'temizle') {
 if (!message.member.hasPermission('MANAGE_MESSAGES')) return message.channel.send('Mesajları Yönet yetkin yok!')
if (!args[0]) return message.channel.send('Bir sayı gir!')
if (isNaN(args[0])) return message.channel.send('Geçerli bir sayı gir!')
if (args[0] > 99) return message.channel.send('99 da fazla mesaj silemem!')
message.channel.bulkDelete(args[0]).then(() => {
message.channel.send(`${args[0]} kadar mesaj silindi!`).then(nmsg => {
nmsg.delete(3000)
})
})
} 