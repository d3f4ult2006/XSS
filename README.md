<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Auto XSS Trigger</title>
</head>
<body>
  <h1>XSS Auto Trigger Demo</h1>

  <div id="output"></div>

  <script>
    // Simulate a malicious user crafting a payload
    const maliciousInput = `<img src="x" onerror="alert('XSS Triggered!')">`;

    // Vulnerable injection point
    document.getElementById("output").innerHTML = maliciousInput;
  </script>
</body>
</html>
