<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cronômetro</title>
    <style>
        body {
            background-color: black;
        }
        h1 {
            color: white;
        }
        div {
            text-align: center;
        }
        button {
            height: 3.0em;
            width: 5.5em;
            border: none;
            color: white;
        }
        button:hover {
            cursor: pointer;
        }
        .start-btn {
            background-color: green;
        }
        .pause-btn {
            background-color: grey;
        }
        .stop-btn {
            background-color: red;
        }
    </style>
</head>
<body>
    <div>
        <h1 id="watch">00:00:00</h1>
        <button class="start-btn" onclick="start()">Iniciar</button>
        <button class="pause-btn" onclick="pause()">Pausar</button>
        <button class="stop-btn" onclick="stop()">Parar</button>
    </div>
    <script>
        var sec = 0;
        var min = 0;
        var hr = 0;
        var interval;

        function start() {
            clearInterval(interval); // Clear any existing intervals
            interval = setInterval(watch, 1000);
        }

        function pause() {
            clearInterval(interval);
        }

        function stop() {
            clearInterval(interval);
            sec = 0;
            min = 0;
            hr = 0;
            document.getElementById('watch').innerText = '00:00:00';
        }

        function twoDigits(digit) {
            return digit < 10 ? '0' + digit : digit;
        }

        function watch() {
            sec++;
            if (sec == 60) {
                sec = 0;
                min++;
                if (min == 60) {
                    min = 0;
                    hr++;
                }
            }
            document.getElementById('watch').innerText = twoDigits(hr) + ':' + twoDigits(min) + ':' + twoDigits(sec);
        }
    </script>
</body>
</html>
