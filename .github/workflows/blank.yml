<!DOCTYPE html>
<html>
<head>
    <title>Free Age Calculator</title>
    <style>
        body { font-family: Arial; text-align: center; padding: 20px; }
        input { padding: 8px; margin: 10px; }
        button { padding: 10px 20px; background: #4CAF50; color: white; border: none; cursor: pointer; }
        #result { margin-top: 20px; font-size: 18px; }
    </style>
</head>
<body>
    <h1>🔢 Free Age Calculator</h1>
    <p>Enter your birthdate:</p>
    <input type="date" id="birthdate">
    <button onclick="calculateAge()">Calculate Age</button>
    <div id="result"></div>

    <script>
        function calculateAge() {
            const birthdate = document.getElementById("birthdate").value;
            if (!birthdate) {
                alert("Please enter your birthdate!");
                return;
            }

            const today = new Date();
            const birthDate = new Date(birthdate);
            
            let age = today.getFullYear() - birthDate.getFullYear();
            const monthDiff = today.getMonth() - birthDate.getMonth();
            
            if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < birthDate.getDate())) {
                age--;
            }

            // Calculate days, hours, minutes, seconds
            const diffTime = Math.abs(today - birthDate);
            const diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
            const diffHours = diffDays * 24;
            const diffMinutes = diffHours * 60;
            const diffSeconds = diffMinutes * 60;
            const diffWeeks = Math.floor(diffDays / 7);

            // Display result
            document.getElementById("result").innerHTML = `
                <h3>📅 Your Age:</h3>
                <p><b>${age} years</b> old</p>
                <p>${diffDays} days | ${diffWeeks} weeks</p>
                <p>${diffHours} hours | ${diffMinutes} minutes | ${diffSeconds} seconds</p>
            `;
        }
    </script>
</body>
</html>
