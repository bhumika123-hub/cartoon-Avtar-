# cartoon-Avatar
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cartoon Avatar Creator</title>
    <style>
        body { text-align: center; font-family: Arial, sans-serif; background: #f0f0f0; }
        .avatar-container { display: flex; justify-content: center; margin-top: 20px; }
        .avatar { width: 200px; height: 250px; background: #ffcc80; border-radius: 50%; position: relative; }
        .eyes, .mouth, .hair, .accessory { position: absolute; }
        .eyes { top: 50px; left: 50px; width: 100px; height: 20px; background: black; border-radius: 50%; }
        .mouth { top: 120px; left: 70px; width: 60px; height: 20px; background: red; border-radius: 10px; }
        .hair { top: -30px; left: 30px; width: 140px; height: 70px; background: brown; border-radius: 50px; }
        .accessory { top: 140px; left: 85px; width: 30px; height: 30px; background: gold; border-radius: 50%; }
    </style>
</head>
<body>
    <h1>Cartoon Avatar Creator</h1>
    <div class="avatar-container">
        <div class="avatar">
            <div class="hair"></div>
            <div class="eyes"></div>
            <div class="mouth"></div>
            <div class="accessory"></div>
        </div>
    </div>
    <br>
    <label>Hair Color:</label>
    <input type="color" id="hairColor" value="#8B4513" onchange="changeHair()">
    <br><br>
    <label>Eye Color:</label>
    <input type="color" id="eyeColor" value="#000000" onchange="changeEyes()">
    <br><br>
    <label>Mouth Color:</label>
    <input type="color" id="mouthColor" value="#ff0000" onchange="changeMouth()">
    <br><br>
    <label>Accessory:</label>
    <select id="accessorySelect" onchange="changeAccessory()">
        <option value="gold">Gold</option>
        <option value="silver">Silver</option>
        <option value="blue">Blue</option>
        <option value="none">None</option>
    </select>
    <br><br>
    <script>
        function changeHair() {
            document.querySelector('.hair').style.background = document.getElementById('hairColor').value;
        }
        function changeEyes() {
            document.querySelector('.eyes').style.background = document.getElementById('eyeColor').value;
        }
        function changeMouth() {
            document.querySelector('.mouth').style.background = document.getElementById('mouthColor').value;
        }
        function changeAccessory() {
            let accessory = document.querySelector('.accessory');
            let value = document.getElementById('accessorySelect').value;
            if (value === "none") {
                accessory.style.display = "none";
            } else {
                accessory.style.display = "block";
                accessory.style.background = value;
            }
        }
    </script>
</body>
</html>
