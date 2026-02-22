<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Prediction Game</title>
    <style>
        body { font-family: Arial; text-align: center; background: #f4f4f4; }
        .card { background: white; margin: 20px; padding: 20px; border-radius: 10px; shadow: 2px 2px 10px gray; }
        .btn { padding: 10px 20px; margin: 5px; cursor: pointer; border: none; color: white; border-radius: 5px; }
        .red { background: red; } .green { background: green; }
        #qr-section { display: none; margin-top: 20px; }
        img { width: 200px; height: 200px; }
    </style>
</head>
<body>

    <h2>Color Prediction Game</h2>
    
    <div class="card">
        <h3>Balance: ₹<span id="balance">0</span></h3>
        <button class="btn green" onclick="showPayment()">Recharge to Play</button>
    </div>

    <div class="card">
        <p>Predict Next Color:</p>
        <button class="btn red" onclick="play('Red')">Red</button>
        <button class="btn green" onclick="play('Green')">Green</button>
    </div>

    <div id="qr-section" class="card">
        <h3>Scan to Pay</h3>
        <img src="YOUR_QR_IMAGE_LINK_HERE" alt="QR Scanner">
        <p>After payment, send screenshot to Admin.</p>
        <button onclick="hidePayment()">Close</button>
    </div>

    <script>
        function showPayment() { document.getElementById('qr-section').style.display = 'block'; }
        function hidePayment() { document.getElementById('qr-section').style.display = 'none'; }
        
        function play(choice) {
            alert("Aapne " + choice + " chuna hai. Khelne ke liye recharge karein!");
        }
    </script>
</body>
</html>
