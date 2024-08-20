<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Números Primos</title>
    <style>
        body {
            background-color: black;
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-size: 10em;
            font-family: Arial, sans-serif;
            user-select: none;
        }
    </style>
</head>
<body>
    <div id="prime-number">2</div>

    <script>
        let primeNumbers = [2];
        let currentIndex = 0;

        function isPrime(num) {
            for (let i = 2; i <= Math.sqrt(num); i++) {
                if (num % i === 0) {
                    return false;
                }
            }
            return num > 1;
        }

        function getNextPrime() {
            let candidate = primeNumbers[primeNumbers.length - 1] + 1;
            while (!isPrime(candidate)) {
                candidate++;
            }
            primeNumbers.push(candidate);
        }

        function updateDisplay() {
            document.getElementById("prime-number").innerText = primeNumbers[currentIndex];
        }

        document.addEventListener("click", function(event) {
            if (event.button === 0) { // Click izquierdo
                currentIndex++;
                if (currentIndex >= primeNumbers.length) {
                    getNextPrime();
                }
            } else if (event.button === 2) { // Click derecho
                if (currentIndex > 0) {
                    currentIndex--;
                }
            }
            updateDisplay();
        });

        // Evitar el menú contextual en el clic derecho
        document.addEventListener("contextmenu", function(event) {
            event.preventDefault();
        });

    </script>
</body>
</html>
