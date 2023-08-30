this is qr by javascript;
////// first step :HTML:
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

 ///// second step:JAVASCRIPT:
 
 <script>
          let urlInput = document.getElementById("url");
          let qrImage = document.getElementById("qrimg");
          let imgBox=document.getElementById("imgBox");

    function QR(){
  
        qrImage.src = "https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=" + urlInput.value;
          imgBox.classList.add("show-img");
        
}</script>



and then u can add somme style by css:
<style>
* {
    margin: 0;
    padding: 0;
    font-family: 'poppins', sans-serif;
    box-sizing: border-box;
}

body {
    background: #262a2f;
}

.container {
    width: 400px;
    padding: 25px 35px;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    background: #fff;
    border-radius: 10px;
}

.container p {
    font-weight: 600;
    font-size: 15px;
    margin-bottom: 8px;
}

.container input {
    width: 100%;
    height: 50px;
    border: 1px solid #494eea;
    outline: 0;
    padding: 10px;
    margin: 10px 0 20px;
    border-radius: 5px;
}


.container button {
    width: 100%;
    height: 50px;
    background: #494eea;
    color: #fff;
    border: 0;
    outline: 0;
    border-radius: 5px;
    box-shadow: 0 10px 10px rgba(0, 0, 0, 0.1);
    cursor: pointer;
    margin: 20px 0;
    font-weight: 500;
}

.imgBox {
    width: 200px;
    border-radius: 5px;
    max-height: 0;
    overflow: hidden;
    transition: max-height 1s;
}
.imgBox.show-img {
    max-height: 300px;
    margin: 10px auto;
    border: 1px solid #d1d1d1;
}

.imgBox.show-img img {
    width: 100%;
    padding: 10px;
}

</style>
