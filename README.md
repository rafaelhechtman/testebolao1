<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Site de Rafael</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f0f0f0;
        }
        .container {
            width: 90%;
            margin: auto;
            overflow: hidden;
        }
        header {
            background: #333;
            color: #fff;
            padding-top: 30px;
            min-height: 70px;
            border-bottom: #77d7d7 3px solid;
        }
        header a {
            color: #fff;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 16px;
        }
        .content {
            padding: 20px;
            background: #fff;
            margin-bottom: 20px;
        }
        .calendar {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .calendar div {
            width: 14%;
            height: 100px;
            background: #eee;
            text-align: center;
            line-height: 100px;
            cursor: pointer;
        }
        .calendar div.marked {
            background: green;
            color: #fff;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Site de Rafael</h1>
        </div>
    </header>

    <div class="container">
        <div class="content">
            <h2>Facilitador de Bolões Esportivos</h2>
            <!-- Inserir conteúdo específico do bolão esportivo aqui -->
        </div>

        <div class="content">
            <h2>Duda</h2>
            <input type="text" id="userName" placeholder="Digite seu nome">
            <h3>Calendário da Creatina</h3>
            <div class="calendar" id="creatinaCalendar"></div>
            <h3>Calendário de Exercícios</h3>
            <div class="calendar" id="exerciseCalendar"></div>
        </div>

        <div class="content">
            <h2>Separador de Times de Pelada</h2>
            <!-- Inserir caixas e botões para separação de times aqui -->
        </div>

        <div class="content">
            <h2>Organizador de Fotos de Materiais Didáticos</h2>
            <!-- Inserir botões e funcionalidade para upload de fotos aqui -->
        </div>

        <div class="content">
            <h2>Estudo de Investimentos</h2>
            <!-- Inserir conteúdo sobre análise de investimentos aqui -->
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const creatinaCalendar = document.getElementById('creatinaCalendar');
            const exerciseCalendar = document.getElementById('exerciseCalendar');

            // Função para criar o calendário
            function createCalendar(calendarElement, monthDays) {
                for (let day = 1; day <= monthDays; day++) {
                    const dayElement = document.createElement('div');
                    dayElement.textContent = day;
                    dayElement.addEventListener('click', () => {
                        dayElement.classList.toggle('marked');
                    });
                    calendarElement.appendChild(dayElement);
                }
            }

            // Criação dos calendários
            createCalendar(creatinaCalendar, 31);
            createCalendar(exerciseCalendar, 31);
        });
    </script>
</body>
</html>
