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
        html,body {
            clear: both; 
        }

        html {
            position: relative; 
        }

        #bg-img {
            width: 1200px;
            height: 700px;
            position: absolute; 
            left: 50vw; 
            top: 50vh; 
            transform: translate(-50%, -50%); 
            margin: auto; 
            background-image: url(./atomicbomb.jpeg);
            background-repeat: no-repeat;
        }

        #clock {
            width: 299px; 
            height: 450px; 
            position: absolute; 
            left: 50vw; 
            top: 50vh; 
            transform: translate(-50%, -60%); 
            margin: auto; 
            background-image: url(./homework_clock3拷貝.png);
            background-repeat: no-repeat;
        }

        #hour {
            width: 12px; 
            height: 57px; 
            position: absolute; 
            left: 143.3px; 
            top: 275.3px; 
            background-image: url(./時針物件2.png); 
            background-repeat: no-repeat;
            transform-origin: center bottom;
        }

        #minute {
            width: 10px; 
            height: 71px; 
            position: absolute; 
            left: 143.5px; 
            top: 260px; 
            background-image: url(./分針物件2.png); 
            background-repeat: no-repeat;
            transform-origin: center bottom;
        }

        #second {
            width: 12px; 
            height: 57px; 
            position: absolute; 
            left: 146.85px; 
            top: 272.3px; 
            background-image: url(./秒針物件2.png); 
            background-repeat: no-repeat;
            transform-origin: center bottom;
        }
    </style>



</head>

<body>
    <div id="bg-img"></div>
    <div id="clock">
        <div id="hour"></div>
        <div id="minute"></div>
        <div id="second"></div>
    </div>
<script>
        const hour = document.getElementById('hour')
        const minute = document.getElementById('minute')
        const second = document.getElementById('second')

        const update = () => {
            const now = new Date()
            hour.style.transform = `rotate(${now.getHours() * 30 }deg)`
            minute.style.transform = `rotate(${now.getMinutes() * 6}deg)`
            second.style.transform = `rotate(${now.getSeconds() * 6}deg)`
        }


        setInterval(update, 1000)
        update()
    </script>
</body>

</html>