<!DOCTYPE html>
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
                <span class="tech-tag">WebAssembly</span>
                <span class="tech-tag">JavaScript</span>
                <span class="tech-tag">Canvas API</span>
            </div>
            <div class="project-links">
                <a href="https://github.com/username/tft-emulator" class="project-link">
                    <svg viewBox="0 0 16 16" fill="currentColor">
                        <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
                    </svg>
                    GitHub
                </a>
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
