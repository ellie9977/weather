# weather
javascript today weather


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <p id="myTxt">안녕하세요!</p>
    <input id="nameInp" type="text" placeholder="이름을 입력하세요." />
    <button id="saveBtn" type="button">저장</button>
   
    
    <script>
        //1. 로컬스토리지에 name이란 값이 있는지 확인
        //1-1. 값이 있으면, 반갑습니다 ㅇㅇㅇ님!
        const username= localStorage.getItem("name");
        //console.log("username", username);
        if (username) {
            const myTxt = document.getElementById("myTxt");
            myTxt.innerText = `반갑습니다! ${username}님!`;
        }
        //2. 저장하기를 누르면 입력창에 있는 값을 로컬스토리지에 저장하기
        document.getElementById("saveBtn").addEventListener("click", () => {
            const name = document.getElementById("nameInp").value;
            locakStorge.setItem("name", name);

            const myTxt = document.getElementById("myTxt");
            myTxt.innerText = `반갑습니다! ${username}님!`;
        });

    </script>
</body>
</html>
