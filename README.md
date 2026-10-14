# 2026_ds3
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>7色に光る HelloWorld</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            font-family: sans-serif;
            background-color: #f0f0f0;
        }
        #text {
            font-size: 3rem;
            font-weight: bold;
            margin-bottom: 20px;
            height: 4.5rem; /* 表示領域の確保 */
        }
        button {
            padding: 10px 20px;
            font-size: 1.2rem;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #007bff;
            color: white;
        }
        button:hover {
            background-color: #0056b3;
        }
        /* 7色のグラインデーションアニメーション */
        .rainbow-text {
            background: linear-gradient(
                to right, 
                #ff0000, #ff7f00, #ffff00, #00ff00, #0000ff, #4b0082, #8b00ff
            );
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-size: 200% auto;
            animation: rainbow 3s linear infinite;
        }
        @keyframes rainbow {
            0% { background-position: 0% center; }
            100% { background-position: 200% center; }
        }
    </style>
</head>
<body>

    <div id="text"></div>
    <button id="btn">ボタンを押してね</button>

    <script>
        // HTML要素を取得
        const button = document.getElementById('btn');
        const textContainer = document.getElementById('text');

        // ボタンがクリックされたときの処理
        button.addEventListener('click', () => {
            // テキストをセット
            textContainer.textContent = 'Hello World';
            // CSSアニメーション用のクラスを追加して7色にする
            textContainer.classList.add('rainbow-text');
        });
    </script>

</body>
</html>
