  var oyun = [
        "?yardım ?davet",
        "?yardım Yeni özellikler",
        "?yardım ?panel"
    ];

    setInterval(function() {

        var random = Math.floor(Math.random()*(oyun.length-0+1)+0);

        client.user.setGame(oyun[random], "https://www.twitch.tv/flaiscode");
        }, 2 * 2500);