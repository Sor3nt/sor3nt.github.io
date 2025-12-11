<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Projects</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'JetBrains Mono', 'Fira Code', 'Courier New', monospace;
            background: #0d1117;
            color: #c9d1d9;
            min-height: 100vh;
            padding: 60px 20px;
            line-height: 1.6;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
        }

        header {
            margin-bottom: 60px;
            border-bottom: 1px solid #21262d;
            padding-bottom: 30px;
        }

        h1 {
            font-size: 2.5em;
            font-weight: 600;
            color: #58a6ff;
            margin-bottom: 8px;
            letter-spacing: -0.5px;
        }

        h1::before {
            content: '> ';
            color: #8b949e;
        }

        .subtitle {
            font-size: 0.95em;
            color: #8b949e;
            font-weight: 400;
        }

        .projects-grid {
            display: grid;
            gap: 20px;
        }

        .project-card {
            background: #161b22;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 24px;
            transition: all 0.2s ease;
            position: relative;
        }

        .project-card:hover {
            border-color: #58a6ff;
            box-shadow: 0 0 0 1px #58a6ff;
        }

        .project-header {
            display: flex;
            align-items: center;
            gap: 12px;
            margin-bottom: 16px;
        }

        .project-number {
            font-size: 0.85em;
            color: #58a6ff;
            background: #1f6feb1a;
            padding: 4px 10px;
            border-radius: 4px;
            font-weight: 600;
            border: 1px solid #1f6feb33;
        }

        .project-title {
            font-size: 1.3em;
            color: #c9d1d9;
            font-weight: 600;
            flex: 1;
        }

        .project-description {
            color: #8b949e;
            margin-bottom: 20px;
            font-size: 0.95em;
            line-height: 1.7;
        }

        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 20px;
        }

        .tech-tag {
            background: #21262d;
            color: #7d8590;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 0.8em;
            border: 1px solid #30363d;
            font-weight: 500;
        }

        .project-links {
            display: flex;
            gap: 12px;
            padding-top: 16px;
            border-top: 1px solid #21262d;
        }

        .project-link {
            text-decoration: none;
            color: #58a6ff;
            font-size: 0.9em;
            display: flex;
            align-items: center;
            gap: 6px;
            padding: 6px 12px;
            border: 1px solid #30363d;
            border-radius: 4px;
            transition: all 0.2s ease;
            background: #0d1117;
        }

        .project-link:hover {
            border-color: #58a6ff;
            background: #1f6feb1a;
        }

        .project-link svg {
            width: 16px;
            height: 16px;
        }

        footer {
            text-align: center;
            color: #484f58;
            margin-top: 80px;
            padding-top: 30px;
            border-top: 1px solid #21262d;
            font-size: 0.9em;
        }

        .status-indicator {
            display: inline-block;
            width: 8px;
            height: 8px;
            background: #3fb950;
            border-radius: 50%;
            margin-right: 6px;
            animation: pulse 2s infinite;
        }

        @keyframes pulse {
            0%, 100% {
                opacity: 1;
            }
            50% {
                opacity: 0.5;
            }
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2em;
            }

            .project-card {
                padding: 20px;
            }

            .project-links {
                flex-direction: column;
            }

            .project-link {
                justify-content: center;
            }
        }
    </style>
</head>
<body>
<div class="container">
    <header>
        <h1>Vibe Coded</h1>
        <p class="subtitle">
            <span class="status-indicator"></span>Random Vibe coded stuff.
        </p>
    </header>

    <div class="projects-grid">
        <div class="project-card">
            <div class="project-header">
                <span class="project-number">#01</span>
                <h2 class="project-title">TFT Display Emulator</h2>
            </div>
            <p class="project-description">
                Browser-based emulator for visualizing and testing TFT display C++ code directly in the browser. 
                Eliminates the need for physical hardware during embedded graphics development cycles.
            </p>
            <div class="project-tech">
                <span class="tech-tag">C++</span>
                <span class="tech-tag">JavaScript</span>
                <span class="tech-tag">Canvas API</span>
                <span class="tech-tag">Embedded</span>
            </div>
            <div class="project-links">
                <a href="https://sor3nt.github.io/esp32-tft-editor.html" class="project-link">
                    <svg viewBox="0 0 16 16" fill="currentColor">
                        <path d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
                    </svg>
                    View Demo
                </a>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <span class="project-number">#02</span>
                <h2 class="project-title">MDL Format Documentation</h2>
            </div>
            <p class="project-description">
                Comprehensive technical specification of the Manhunt 2 MDL model format. 
                In-depth analysis of file structures, vertex formats, skeletal hierarchies, and matrix transformations 
                with hex examples and reference implementations.
            </p>
            <div class="project-tech">
                <span class="tech-tag">Binary Format</span>
                <span class="tech-tag">3D Graphics</span>
                <span class="tech-tag">Reverse Engineering</span>
                <span class="tech-tag">Documentation</span>
            </div>
            <div class="project-links">
                <a href="MH2_MDL_Format_Documentation.html" class="project-link">
                    <svg viewBox="0 0 16 16" fill="currentColor">
                        <path d="M4 1.75C4 .784 4.784 0 5.75 0h5.586c.464 0 .909.184 1.237.513l2.914 2.914c.329.328.513.773.513 1.237v9.586A1.75 1.75 0 0113.25 16h-7.5A1.75 1.75 0 014 14.25V1.75zm1.75-.25a.25.25 0 00-.25.25v12.5c0 .138.112.25.25.25h7.5a.25.25 0 00.25-.25V6h-2.75A1.75 1.75 0 019 4.25V1.5H5.75zm6.75.062V4.25c0 .138.112.25.25.25h2.688a.252.252 0 00-.011-.013l-2.914-2.914a.254.254 0 00-.013-.011z"/>
                    </svg>
                    Read Docs
                </a>
            </div>
        </div>

        <div class="project-card">
            <div class="project-header">
                <span class="project-number">#03</span>
                <h2 class="project-title">Projection Mapping Tool v4</h2>
            </div>
            <p class="project-description">
                Advanced real-time projection mapping tool with video transformation, animated effects, and live preview. 
                Features wavy video distortion, multi-effect combinations (travel on wave paths), 
                zoom/pan canvas navigation, and dual-tab live sync for professional VJ performances.
            </p>
            <div class="project-tech">
                <span class="tech-tag">Canvas 2D</span>
                <span class="tech-tag">Video Transformation</span>
                <span class="tech-tag">Real-time Effects</span>
                <span class="tech-tag">VJ Tool</span>
                <span class="tech-tag">Live Performance</span>
            </div>
            <div class="project-links">
                <a href="projection-mapping-v4.html" class="project-link">
                    <svg viewBox="0 0 16 16" fill="currentColor">
                        <path d="M1.75 0A1.75 1.75 0 000 1.75v12.5C0 15.216.784 16 1.75 16h12.5A1.75 1.75 0 0016 14.25V1.75A1.75 1.75 0 0014.25 0H1.75zM1.5 1.75a.25.25 0 01.25-.25h12.5a.25.25 0 01.25.25v12.5a.25.25 0 01-.25.25H1.75a.25.25 0 01-.25-.25V1.75zM6 5.25a.75.75 0 01.75-.75h5.5a.75.75 0 010 1.5h-5.5A.75.75 0 016 5.25zm.75 2.25a.75.75 0 000 1.5h5.5a.75.75 0 000-1.5h-5.5zM6 10.25a.75.75 0 01.75-.75h5.5a.75.75 0 010 1.5h-5.5a.75.75 0 01-.75-.75zM3.5 5.25a.75.75 0 01.75-.75h.5a.75.75 0 010 1.5h-.5a.75.75 0 01-.75-.75zM4.25 7.5a.75.75 0 000 1.5h.5a.75.75 0 000-1.5h-.5zM3.5 10.25a.75.75 0 01.75-.75h.5a.75.75 0 010 1.5h-.5a.75.75 0 01-.75-.75z"/>
                    </svg>
                    Launch Tool
                </a>
            </div>
        </div>
    </div>

    <footer>
        <p>Built with precision // 2025</p>
    </footer>
</div>
</body>
</html>
