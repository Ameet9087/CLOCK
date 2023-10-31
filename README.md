<!DOCTYPE html>
<html>

    <head>
        <meta charset="UTF-8" />
        <title>CLOCK</title>
        <style>
            #bd {
                background-image: url(clock3.jpg);
                height: 100vh;
                width: 100%;
                padding-top: 100px;
                margin-top: -120px;
            }

            h1 {

                margin-top: 250px;
                margin-left: 460px;
                width: 150px;
                color: rgb(68, 230, 4);
                font-size: 100px;

            }
        </style>
    </head>


    <body>
        <div id="bd">
            <h1><span id="hr"></span>:<span id="mn"></span>:<span id="sec"></span></h1>

        </div>

        <script>
            let hour = document.getElementById("hr");
            let min = document.getElementById("mn");
            let sc = document.getElementById("sec");

            function updateTime() {
                let tm = new Date();
                let hr = tm.getHours();
                let mn = tm.getMinutes();
                let sec = tm.getSeconds();
                hour.innerHTML = hr - 12;
                min.innerHTML = mn;
                sc.innerHTML = sec;
            }
            setInterval(updateTime, 1000);
        </script>
    </body>

</html>
