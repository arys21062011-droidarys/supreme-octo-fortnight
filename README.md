<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Мой интерактивный справочник</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f7f6;
            color: #333;
            max-width: 800px;
            margin: 40px auto;
            padding: 20px;
        }
        h1 {
            text-align: center;
            color: #2c3e50;
        }
        .section {
            background: #ffffff;
            margin-bottom: 20px;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        .section h2 {
            margin-top: 0;
            color: #34495e;
            border-bottom: 2px solid #ecf0f1;
            padding-bottom: 10px;
        }
        .formula-item {
            margin: 10px 0;
        }
        .formula-btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 10px 15px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            text-align: left;
            transition: background 0.3s;
        }
        .formula-btn:hover {
            background-color: #2980b9;
        }
        .formula-info {
            display: none;
            background-color: #e8f8f5;
            border-left: 4px solid #2ecc71;
            padding: 12px;
            margin-top: 5px;
            border-radius: 0 5px 5px 0;
        }
    </style>
</head>
<body>

    <h1>Мой учебный справочник</h1>

    <!-- Раздел 1 -->
    <div class="section">
        <h2>Физика (Кинематика)</h2>
        
        <div class="formula-item">
            <button class="formula-btn" onclick="toggleInfo('info1')">Формула скорости: v = s / t</button>
            <div id="info1" class="formula-info">
                <p><strong>Описание:</strong> Эта формула определяет скорость при равномерном движении.</p>
                <p><strong>Где:</strong><br>
                v — скорость (м/с)<br>
                s — пройденное расстояние (м)<br>
                t — время (с)</p>
            </div>
        </div>

        <div class="formula-item">
            <button class="formula-btn" onclick="toggleInfo('info2')">Кинетическая энергия: Ek = (m * v^2) / 2</button>
            <div id="info2" class="formula-info">
                <p><strong>Описание:</strong> Энергия тела, обусловленная его движением.</p>
                <p><strong>Где:</strong><br>
                m — масса тела (кг)<br>
                v — скорость тела (м/с)</p>
            </div>
        </div>
    </div>

    <!-- Раздел 2 -->
    <div class="section">
        <h2>Математика (Геометрия)</h2>
        
        <div class="formula-item">
            <button class="formula-btn" onclick="toggleInfo('info3')">Площадь круга: S = π * r^2</button>
            <div id="info3" class="formula-info">
                <p><strong>Описание:</strong> Позволяет найти площадь круга через его радиус.</p>
                <p><strong>Где:</strong><br>
                S — площадь<br>
                π ≈ 3.14159<br>
                r — радиус круга</p>
            </div>
        </div>
    </div>

    <script>
        function toggleInfo(id) {
            var infoBlock = document.getElementById(id);
            if (infoBlock.style.display === "block") {
                infoBlock.style.display = "none";
            } else {
                infoBlock.style.display = "block";
            }
        }
    </script>

</body>
</html>
