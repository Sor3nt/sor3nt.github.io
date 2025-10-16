<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>TFT Display Editor - 320x160</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Courier New', monospace;
            background: #1e1e1e;
            color: #d4d4d4;
            padding: 20px;
            display: flex;
            gap: 20px;
            height: 100vh;
        }

        .left-panel {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 10px;
            min-width: 400px;
        }

        .right-panel {
            flex: 0 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            min-width: 700px;
        }

        h1 {
            color: #4ec9b0;
            font-size: 18px;
            margin-bottom: 10px;
        }

        #canvas {
            border: 3px solid #4ec9b0;
            background: #000;
            image-rendering: pixelated;
            box-shadow: 0 0 20px rgba(78, 201, 176, 0.3);
            transform: scale(2);
            margin-top: 100px;
            margin-bottom: 200px;
        }

        .display-info {
            color: #608b4e;
            font-size: 12px;
            text-align: center;
        }

        #code {
            width: 100%;
            flex: 1;
            background: #252526;
            color: #d4d4d4;
            border: 2px solid #3e3e42;
            padding: 15px;
            font-family: 'Courier New', monospace;
            font-size: 14px;
            resize: none;
            outline: none;
            border-radius: 4px;
        }

        #code:focus {
            border-color: #4ec9b0;
        }

        .toolbar {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        button {
            background: #0e639c;
            color: white;
            border: none;
            padding: 8px 16px;
            cursor: pointer;
            border-radius: 3px;
            font-family: inherit;
            font-size: 12px;
        }

        button:hover {
            background: #1177bb;
        }

        button:active {
            background: #0d5a8f;
        }

        button.stop {
            background: #c72e0f;
        }

        button.stop:hover {
            background: #e03e1f;
        }

        .error {
            background: #3c1f1f;
            border-left: 3px solid #f48771;
            padding: 10px;
            color: #f48771;
            font-size: 12px;
            border-radius: 3px;
            max-height: 150px;
            overflow-y: auto;
        }

        .error:empty {
            display: none;
        }

        .status {
            color: #4ec9b0;
            font-size: 11px;
        }
    </style>
</head>
<body>
<div class="left-panel">
    <h1>📝 C++ Code Editor</h1>
    <textarea id="code" spellcheck="false">// Beispiel Code - probiere es aus!
tft->fillScreen(0x0821);

// Header Box
tft->fillRoundRect(8, 8, 304, 45, 6, 0x1082);
tft->drawRoundRect(8, 8, 304, 45, 6, 0x4208);

// Protocol Badge
tft->fillRoundRect(15, 23, 120, 20, 3, 0x1082);
tft->setTextColor(0xFFFF);
tft->setTextSize(2);
tft->setCursor(20, 26);
tft->print("PRINCETON");

// Address
tft->setTextSize(1);
tft->setTextColor(0x07FF);
tft->setCursor(145, 30);
tft->print("0x68E649");

// Signal Bars
for (uint8_t i = 0; i < 4; i++) {
    uint16_t barH = 4 + (i * 3);
    uint16_t barX = 268 + (i * 8);
    uint16_t barY = 38 - barH;
    uint16_t color = i < 3 ? 0x07E0 : 0x2104;
    tft->fillRoundRect(barX, barY, 5, barH, 2, color);
}

// Frequency
tft->setTextColor(0x8410);
tft->setCursor(253, 38);
tft->print("~");
tft->setTextColor(0xFFFF);
tft->setCursor(261, 37);
tft->print("433.92");</textarea>

    <div class="toolbar">
        <button id="runBtn" onclick="executeCode()">▶ Run Code</button>
        <button id="stopBtn" class="stop" onclick="stopExecution()" style="display:none">⬛ Stop</button>
        <button onclick="clearDisplay()">🗑 Clear Display</button>
        <button onclick="loadExample()">📋 Load Example</button>
        <span class="status" id="status"></span>
    </div>

    <div id="error" class="error"></div>
</div>

<div class="right-panel">
    <h1>📺 TFT Display Preview</h1>

    <canvas id="canvas" width="320" height="160"></canvas>

    <div class="display-info">
        <span id="displaySize">320 x 160 pixels</span> | ESP32 TFT Simulation
    </div>
    <div style="margin-top: 10px;">
        <label for="sizeSelect" style="color: #608b4e; margin-right: 10px;">Display Size:</label>
        <select id="sizeSelect" onchange="changeDisplaySize()" style="background: #252526; color: #d4d4d4; border: 1px solid #3e3e42; padding: 5px 10px; border-radius: 3px; cursor: pointer;">
            <option value="320x160" selected>320 x 160 (ST7789 1.9")</option>
            <option value="240x240">240 x 240 (ST7789 1.3" Square)</option>
            <option value="240x320">240 x 320 (ILI9341 2.4")</option>
            <option value="320x240">320 x 240 (ILI9341 2.8" Landscape)</option>
            <option value="480x320">480 x 320 (ILI9486 3.5")</option>
            <option value="128x160">128 x 160 (ST7735 1.8")</option>
            <option value="128x128">128 x 128 (ST7735 1.44" Square)</option>
        </select>
    </div>
</div>

<script>
    const canvas = document.getElementById('canvas');
    const ctx = canvas.getContext('2d');
    const codeEditor = document.getElementById('code');
    const errorDiv = document.getElementById('error');
    const statusDiv = document.getElementById('status');
    const runBtn = document.getElementById('runBtn');
    const stopBtn = document.getElementById('stopBtn');
    const sizeSelect = document.getElementById('sizeSelect');
    const displaySizeText = document.getElementById('displaySize');

    let executionStopped = false;

    // ST77XX Color Constants
    const ST77XX_BLACK = 0x0000;
    const ST77XX_WHITE = 0xFFFF;
    const ST77XX_RED = 0xF800;
    const ST77XX_GREEN = 0x07E0;
    const ST77XX_BLUE = 0x001F;
    const ST77XX_CYAN = 0x07FF;
    const ST77XX_MAGENTA = 0xF81F;
    const ST77XX_YELLOW = 0xFFE0;
    const ST77XX_ORANGE = 0xFC00;

    // Convert RGB565 to RGB
    function rgb565ToRgb(color) {
        const r = ((color >> 11) & 0x1F) * 255 / 31;
        const g = ((color >> 5) & 0x3F) * 255 / 63;
        const b = (color & 0x1F) * 255 / 31;
        return `rgb(${Math.round(r)}, ${Math.round(g)}, ${Math.round(b)})`;
    }

    // TFT Wrapper Class
    class TFT {
        constructor(ctx) {
            this.ctx = ctx;
            this.textColor = ST77XX_WHITE;
            this.textSize = 1;
            this.cursorX = 0;
            this.cursorY = 0;
            this.width = 320;
            this.height = 160;
        }

        fillScreen(color) {
            this.ctx.fillStyle = rgb565ToRgb(color);
            this.ctx.fillRect(0, 0, this.width, this.height);
        }

        fillRect(x, y, w, h, color) {
            this.ctx.fillStyle = rgb565ToRgb(color);
            this.ctx.fillRect(x, y, w, h);
        }

        drawRect(x, y, w, h, color) {
            this.ctx.strokeStyle = rgb565ToRgb(color);
            this.ctx.lineWidth = 1;
            this.ctx.strokeRect(x + 0.5, y + 0.5, w - 1, h - 1);
        }

        fillRoundRect(x, y, w, h, r, color) {
            this.ctx.fillStyle = rgb565ToRgb(color);
            this.ctx.beginPath();
            this.ctx.roundRect(x, y, w, h, r);
            this.ctx.fill();
        }

        drawRoundRect(x, y, w, h, r, color) {
            this.ctx.strokeStyle = rgb565ToRgb(color);
            this.ctx.lineWidth = 1;
            this.ctx.beginPath();
            this.ctx.roundRect(x + 0.5, y + 0.5, w - 1, h - 1, r);
            this.ctx.stroke();
        }

        fillCircle(x, y, radius, color) {
            this.ctx.fillStyle = rgb565ToRgb(color);
            this.ctx.beginPath();
            this.ctx.arc(x, y, radius, 0, Math.PI * 2);
            this.ctx.fill();
        }

        drawCircle(x, y, radius, color) {
            this.ctx.strokeStyle = rgb565ToRgb(color);
            this.ctx.lineWidth = 1;
            this.ctx.beginPath();
            this.ctx.arc(x, y, radius, 0, Math.PI * 2);
            this.ctx.stroke();
        }

        drawLine(x0, y0, x1, y1, color) {
            this.ctx.strokeStyle = rgb565ToRgb(color);
            this.ctx.lineWidth = 1;
            this.ctx.beginPath();
            this.ctx.moveTo(x0, y0);
            this.ctx.lineTo(x1, y1);
            this.ctx.stroke();
        }

        setTextColor(color) {
            this.textColor = color;
        }

        setTextSize(size) {
            this.textSize = size;
        }

        setCursor(x, y) {
            this.cursorX = x;
            this.cursorY = y;
        }

        print(text) {
            // Adafruit GFX Font: 5x8 pixels per character (6x8 with spacing)
            const charWidth = 6 * this.textSize;
            const charHeight = 8 * this.textSize;

            this.ctx.font = `bold ${charHeight}px monospace`;
            this.ctx.fillStyle = rgb565ToRgb(this.textColor);
            this.ctx.textBaseline = 'top';

            const str = String(text);

            // Draw each character with fixed width spacing (like Adafruit GFX)
            for (let i = 0; i < str.length; i++) {
                this.ctx.fillText(str[i], this.cursorX, this.cursorY);
                this.cursorX += charWidth;
            }
        }

        printf(format, ...args) {
            let result = format;
            let argIndex = 0;

            result = result.replace(/%([0-9]*)([dxX]|[0-9]*l[xX])/g, (match, width, type) => {
                if (argIndex >= args.length) return match;
                const value = args[argIndex++];

                if (type === 'd') {
                    return String(value).padStart(parseInt(width) || 0, '0');
                } else if (type === 'x' || type === 'X' || type.includes('lx') || type.includes('lX')) {
                    let hex = Number(value).toString(16);
                    if (type === 'X' || type.includes('X')) hex = hex.toUpperCase();
                    const padWidth = parseInt(width) || 0;
                    return hex.padStart(padWidth, '0');
                }
                return match;
            });

            this.print(result);
        }
    }

    // Global TFT instance (as pointer)
    const tft = new TFT(ctx);

    // Delay functions
    function delay(ms) {
        return new Promise(resolve => setTimeout(resolve, ms));
    }

    function delayMicroseconds(us) {
        return new Promise(resolve => setTimeout(resolve, us / 1000));
    }

    // C++ to JavaScript transpiler
    function transpileCppToJs(code) {
        let jsCode = code;

        // Replace tft-> with tft.
        jsCode = jsCode.replace(/tft->/g, 'tft.');

        // Replace uint8_t, uint16_t, uint32_t, int16_t etc. with let
        jsCode = jsCode.replace(/\b(uint8_t|uint16_t|uint32_t|int8_t|int16_t|int32_t)\s+/g, 'let ');

        // Replace size_t with let
        jsCode = jsCode.replace(/\bsize_t\s+/g, 'let ');

        // Replace char arrays with let
        jsCode = jsCode.replace(/\bchar\s+(\w+)\[.*?\]/g, 'let $1');

        // Replace sprintf with template literals (simplified)
        jsCode = jsCode.replace(/sprintf\s*\(\s*(\w+)\s*,\s*"(.+?)"\s*,\s*(.+?)\s*\)/g, (match, var1, format, args) => {
            // Simple sprintf replacement
            let replacement = format;
            const argList = args.split(',').map(a => a.trim());
            let argIndex = 0;

            replacement = replacement.replace(/%([0-9]*)([dxX]|05[xX]|05l[xX])/g, (m, width, type) => {
                if (argIndex >= argList.length) return m;
                const arg = argList[argIndex++];

                if (type === 'd') {
                    return '${' + arg + '}';
                } else if (type.includes('x') || type.includes('X')) {
                    let hex = '${' + arg + '.toString(16)';
                    if (width) hex += '.padStart(' + width + ', "0")';
                    if (type.includes('X')) hex += '.toUpperCase()';
                    return hex + '}';
                }
                return m;
            });

            return `${var1} = \`${replacement}\``;
        });

        // Replace strlen with .length
        jsCode = jsCode.replace(/strlen\s*\(\s*(\w+)\s*\)/g, '$1.length');

        // Make delay async
        jsCode = jsCode.replace(/\bdelay\s*\(/g, 'await delay(');
        jsCode = jsCode.replace(/\bdelayMicroseconds\s*\(/g, 'await delayMicroseconds(');

        return jsCode;
    }

    // Auto-execute on code change
    let timeout;
    codeEditor.addEventListener('input', () => {
        clearTimeout(timeout);
        timeout = setTimeout(executeCode, 800);
    });

    async function executeCode() {
        try {
            executionStopped = false;
            runBtn.style.display = 'none';
            stopBtn.style.display = 'inline-block';
            statusDiv.textContent = '▶ Running...';
            errorDiv.textContent = '';
            tft.fillScreen(ST77XX_BLACK);

            // Transpile C++ to JavaScript
            const jsCode = transpileCppToJs(codeEditor.value);

            // Execute as async function
            const asyncFunc = new Function('tft', 'delay', 'delayMicroseconds', 'ST77XX_BLACK', 'ST77XX_WHITE', 'ST77XX_RED', 'ST77XX_GREEN', 'ST77XX_BLUE', 'ST77XX_CYAN', 'ST77XX_MAGENTA', 'ST77XX_YELLOW', 'ST77XX_ORANGE',
                `return (async () => {
                        ${jsCode}
                    })();`
            );

            await asyncFunc(tft, delay, delayMicroseconds, ST77XX_BLACK, ST77XX_WHITE, ST77XX_RED, ST77XX_GREEN, ST77XX_BLUE, ST77XX_CYAN, ST77XX_MAGENTA, ST77XX_YELLOW, ST77XX_ORANGE);

            if (!executionStopped) {
                statusDiv.textContent = '✓ Done';
            }
        } catch (error) {
            errorDiv.textContent = `❌ Error: ${error.message}`;
            statusDiv.textContent = '✗ Error';
            console.error(error);
        } finally {
            runBtn.style.display = 'inline-block';
            stopBtn.style.display = 'none';
        }
    }

    function stopExecution() {
        executionStopped = true;
        statusDiv.textContent = '⬛ Stopped';
        runBtn.style.display = 'inline-block';
        stopBtn.style.display = 'none';
    }

    function clearDisplay() {
        tft.fillScreen(ST77XX_BLACK);
        errorDiv.textContent = '';
        statusDiv.textContent = '';
    }

    function loadExample() {
        codeEditor.value = `// Sub-Sw0rd Bootscreen
tft->fillScreen(ST77XX_BLACK);

// Grüner Hacker-Text
uint16_t hackGreen = 0x07E0;
uint16_t darkGreen = 0x0320;
uint16_t dimGreen = 0x0200;

// ASCII Art Header - zentriert für 320px
tft->setTextSize(1);
tft->setTextColor(hackGreen);
tft->setCursor(20, 10);
tft->print("================================================");

// Matrix-Style Zahlen
tft->setCursor(55, 22);
tft->setTextColor(dimGreen);
tft->print("01001010 11010011 10110101 00111001");

// Haupttitel - größer und zentriert
tft->setTextSize(4);
tft->setTextColor(hackGreen);
tft->setCursor(55, 45);
tft->print("Sub-Sw0rd");

// Doppelter Glitch-Rahmen um Titel
tft->drawRect(50, 42, 220, 38, hackGreen);
tft->drawRect(52, 44, 216, 34, darkGreen);

// Trennlinie
tft->setTextSize(1);
tft->setCursor(20, 90);
tft->setTextColor(darkGreen);
tft->print("================================================");

tft->setCursor(40, 105);
tft->setTextColor(darkGreen);
tft->print("Freq: 433.92MHz | Power: HIGH | Mode: RX");

tft->setTextSize(2);
tft->setCursor(5, 135);
tft->setTextColor(hackGreen);
tft->print(">>> WAITING FOR SIGNAL <<<");

delay(2000);

// After delay, show next screen
tft->fillScreen(0x0821);
tft->setTextSize(3);
tft->setTextColor(ST77XX_GREEN);
tft->setCursor(80, 60);
tft->print("READY!");`;
        executeCode();
    }

    function changeDisplaySize() {
        const size = sizeSelect.value;
        const [width, height] = size.split('x').map(Number);

        canvas.width = width;
        canvas.height = height;
        displaySizeText.textContent = `${width} x ${height} pixels`;

        // Update TFT dimensions
        tft.width = width;
        tft.height = height;

        // Re-execute code with new size
        executeCode();
    }

    // Initial execution
    executeCode();
</script>
</body>
</html>
