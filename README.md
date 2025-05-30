<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Seu Site Minimalista</title>
    <style>
        body {
            background-color: #0a0a0a;
            color: #00ff9d; /* Verde neon ajustado */
            font-family: 'Courier New', monospace;
            text-align: center;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
            line-height: 1.6;
        }
        .container {
            max-width: 600px;
            padding: 20px;
        }
        .typewriter {
            border-right: 2px solid #00ff9d;
            white-space: nowrap;
            overflow: hidden;
            margin: 0 auto;
            animation: typing 3.5s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        @keyframes typing {
            from { width: 0 }
            to { width: 100% }
        }
        @keyframes blink-caret {
            from, to { border-color: transparent }
            50% { border-color: #00ff9d }
        }
        a {
            color: #00ff9d;
            text-decoration: none;
            border-bottom: 1px dashed #00ff9d;
        }
        a:hover {
            opacity: 0.8;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="typewriter">
            <h1>hello, i'm [your_name].</h1>
        </div>
        <p>↓</p>
        <p>welcome to my digital space.</p>
        <p><a href="#" id="secret-link">(enter)</a></p>
    </div>

    <script>
        // Efeito typewriter
        document.addEventListener('DOMContentLoaded', function() {
            const elements = document.querySelectorAll('.typewriter');
            elements.forEach(el => {
                const text = el.textContent;
                el.textContent = '';
                let i = 0;
                function type() {
                    if (i < text.length) {
                        el.textContent += text.charAt(i);
                        i++;
                        setTimeout(type, 100);
                    }
                }
                type();
            });

            // Simulação de interação (como no original)
            document.getElementById('secret-link').addEventListener('click', function(e) {
                e.preventDefault();
                alert('✨ (This would navigate to another page in the real version)');
            });
        });
    </script>
</body>
</html>
