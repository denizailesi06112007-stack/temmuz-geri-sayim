<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Temmuz Ayı Geri Sayımı</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            padding-top: 50px;
        }
        #countdown {
            font-size: 4em;
            font-weight: bold;
            color: #333;
        }
    </style>
</head>
<body>

    <h1>Temmuz Ayına Geri Sayım</h1>
    <p id="countdown"></p>

    <script>
        var countDownDate = new Date("Jul 1, 2026 00:00:00").getTime();
        var x = setInterval(function() {
            var now = new Date().getTime();
            var distance = countDownDate - now;

            var days = Math.floor(distance / (1000 * 60 * 60 * 24));
            var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
            var seconds = Math.floor((distance % (1000 * 60)) / 1000);

            document.getElementById("countdown").innerHTML = days + " Gün " + hours + " Saat "
            + minutes + " Dakika " + seconds + " Saniye ";

            if (distance < 0) {
                clearInterval(x);
                document.getElementById("countdown").innerHTML = "TEMMUZ AYI GELDİ!";
            }
        }, 1000);
    </script>

</body>
</html>
