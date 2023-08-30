this is qr by javascript;

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="qr.css">
    <title>Document</title>
</head>
<body>
 <div class="container" >
 <p><u>Enter your text or URL:</u></p>
<input type="text" name="txt1" id="url" placeholder="URL">
<div class="imgBox" id="imgBox">
    <img src="" id="qrimg">
</div>
<button type="submit" onclick="QR()">Generate QR Code</button>
 </div>  
