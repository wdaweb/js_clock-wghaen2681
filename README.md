# 泰山職訓前端班時鐘作業
發揮創意美化你上課完成的時鐘，並試著加入更多功能  

## 注意
請盡量使用上課教的 GUI 工具或 git 指令繳交作業  
若使用 GitHub 網頁進行 commit 會依次數扣分



<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        #box {
            width: 100vh;
            height: 100vh;
            background: grey;
        }




        #clock {
            width: 200px;
            height: 200px;
            background: blue;
            border-radius: 50%;
            margin: auto;
            position: relative;
        }

        #hour {
            width: 20%;
            height: 5px;
            border-radius: 5px;
            background: green;
            position: absolute;
            top: calc(50% - 2px);
            left: 50%;
            transform-origin: left center;
        }

        #minute {
            width: 40%;
            height: 3px;
            border-radius: 5px;
            background: orange;
            position: absolute;
            top: calc(50% - 1.5px);
            left: 50%;
            transform-origin: left center;
        }

        #second {
            width: 45%;
            height: 2px;
            border-radius: 5px;
            background: pink;
            position: absolute;
            top: calc(50% - 1px);
            left: 50%;
            transform-origin: left center;
            ];
        }
    </style>



</head>

<body>
    <div id="box">
        <div id="clock">
            <div id="hour"></div>
            <div id="minute"></div>
            <div id="second"></div>
        </div>
    </div>

    <script>
        const hour = document.getElementById('hour')
        const minute = document.getElementById('minute')
        const second = document.getElementById('second')

        const update = () => {
            const now = new Date()
            hour.style.transform = `rotate(${now.getHours() * 30 - 90}deg)`
            minute.style.transform = `rotate(${now.getMinutes() * 6 - 90}deg)`
            second.style.transform = `rotate(${now.getSeconds() * 6 - 90}deg)`
        }


        setInterval(update, 1000)
        update()
    </script>
</body>

</html>