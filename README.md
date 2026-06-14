<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kadori Garang</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #121212; 
            color: #ffffff;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            padding: 20px;
            overflow: hidden;
        }

        .container {
            text-align: center;
            width: 100%;
            max-width: 400px; 
        }

        .tulisan-utama {
            font-size: 3rem; 
            font-weight: 900;
            text-transform: uppercase;
            letter-spacing: 2px;
            color: #ff3333; 
            text-shadow: 0px 4px 10px rgba(255, 51, 51, 0.5);
            transition: transform 0.1s ease, color 0.3s ease;
            user-select: none;
            cursor: pointer;
        }

        .tulisan-utama:active {
            transform: scale(0.9);
            color: #ffffff;
        }

        .keterangan {
            margin-top: 15px;
            font-size: 0.9rem;
            color: #888888;
            letter-spacing: 1px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1 class="tulisan-utama" id="textGarang">Kadori Garang</h1>
        <p class="keterangan">Coba tap layarnya</p>
    </div>

    <script>
        const textElement = document.getElementById('textGarang');
        textElement.addEventListener('click', () => {
            if (navigator.vibrate) {
                navigator.vibrate(50); 
            }
            console.log('Kadori emang garang!');
        });
    </script>
</body>
</html>
