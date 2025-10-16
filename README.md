<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Meine Projekte</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
        }

        header {
            text-align: center;
            color: white;
            margin-bottom: 50px;
        }

        h1 {
            font-size: 3em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .subtitle {
            font-size: 1.2em;
            opacity: 0.9;
        }

        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-top: 40px;
        }

        .project-card {
            background: white;
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }

        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 15px 40px rgba(0,0,0,0.3);
        }

        .project-number {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            text-align: center;
            line-height: 40px;
            font-weight: bold;
            margin-bottom: 15px;
        }

        .project-title {
            font-size: 1.5em;
            color: #333;
            margin-bottom: 10px;
        }

        .project-description {
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: #f0f0f0;
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.85em;
            color: #555;
        }

        .project-links {
            display: flex;
            gap: 15px;
        }

        .project-link {
            text-decoration: none;
            color: #667eea;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 5px;
            transition: color 0.3s ease;
        }

        .project-link:hover {
            color: #764ba2;
        }

        .project-link svg {
            width: 18px;
            height: 18px;
        }

        footer {
            text-align: center;
            color: white;
            margin-top: 60px;
            opacity: 0.8;
        }

        @media (max-width: 600px) {
            h1 {
                font-size: 2em;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <header>
        <h1>Meine Projekte</h1>
        <p class="subtitle">Eine Übersicht meiner Entwicklungsprojekte</p>
    </header>

    <div class="projects-grid">
        <div class="project-card">
            <div class="project-number">1</div>
            <h2 class="project-title">TFT-Display Emulator</h2>
            <p class="project-description">
                Ein Browser-basierter Emulator, der TFT-Display C++ Code direkt im Browser visualisiert und testet. Perfekt für die Entwicklung von Embedded-Grafiken ohne Hardware.
            </p>
            <div class="project-tech">
                <span class="tech-tag">C++</span>
                <span class="tech-tag">JavaScript</span>
                <span class="tech-tag">Canvas</span>
            </div>
            <div class="project-links">
                <a href="https://sor3nt.github.io/esp32-tft-editor.html" class="project-link">
                    <svg viewBox="0 0 16 16" fill="currentColor">
                        <path d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm0 14c-3.31 0-6-2.69-6-6s2.69-6 6-6 6 2.69 6 6-2.69 6-6 6z"/>
                        <path d="M8 4c-.55 0-1 .45-1 1v3c0 .28.11.53.29.71l2 2c.39.39 1.02.39 1.41 0 .39-.39.39-1.02 0-1.41L9 7.59V5c0-.55-.45-1-1-1z"/>
                    </svg>
                    Demo
                </a>
            </div>
        </div>

    </div>

    <footer>
        <p>&copy; 2025 - Erstellt mit ❤️ und Code</p>
    </footer>
</div>
</body>
</html>
