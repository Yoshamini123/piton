
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>🐍 Путешествие на планету Пайтон — Блокнот 1</title>
    <!-- Шрифты и иконки -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,500;14..32,600;14..32,700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            background: #f8fafc;
            color: #0b1b2f;
            line-height: 1.6;
            padding: 2rem 1rem;
        }

        .notebook {
            max-width: 1000px;
            margin: 0 auto;
            background: white;
            border-radius: 2rem;
            box-shadow: 0 20px 40px -12px rgba(0, 0, 0, 0.15), 0 4px 18px rgba(0, 0, 0, 0.05);
            padding: 2.5rem 2.2rem;
            border: 1px solid #e9eef3;
        }

        /* Заголовок */
        .hero {
            margin-bottom: 2.5rem;
            padding-bottom: 1.8rem;
            border-bottom: 2px dashed #d0dae8;
        }

        .hero h1 {
            font-size: 2.4rem;
            font-weight: 700;
            letter-spacing: -0.02em;
            display: flex;
            align-items: center;
            gap: 12px;
            color: #0b2b4b;
            margin-bottom: 0.75rem;
        }

        .hero h1 i {
            font-size: 2.2rem;
            color: #2b6f9e;
        }

        .meta-bar {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem 2rem;
            background: #eef5fa;
            padding: 0.9rem 1.5rem;
            border-radius: 100px;
            font-size: 0.95rem;
            font-weight: 500;
            color: #1e4b6e;
        }

        .meta-bar span {
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .meta-bar i {
            color: #2b6f9e;
            width: 1.2rem;
            text-align: center;
        }

        /* Секции */
        section {
            margin-bottom: 3rem;
        }

        h2 {
            font-size: 1.8rem;
            font-weight: 700;
            letter-spacing: -0.01em;
            color: #0b2b4b;
            margin-bottom: 1.2rem;
            display: flex;
            align-items: center;
            gap: 12px;
        }

        h2 i {
            font-size: 1.6rem;
            color: #2b6f9e;
            background: #e2eef9;
            padding: 8px;
            border-radius: 14px;
        }

        h3 {
            font-size: 1.3rem;
            font-weight: 600;
            margin: 1.8rem 0 1rem;
            color: #17456b;
        }

        p {
            margin-bottom: 1rem;
            color: #1f3a54;
        }

        /* Карточки целей */
        .goals-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 0.85rem;
            margin: 1.5rem 0;
        }

        .goal-item {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            background: #f4faff;
            padding: 0.9rem 1.2rem;
            border-radius: 16px;
            border-left: 5px solid #2b6f9e;
            transition: transform 0.1s ease;
        }

        .goal-item:hover {
            transform: translateX(4px);
            background: #ecf6ff;
        }

        .goal-item i {
            color: #2b6f9e;
            font-size: 1.2rem;
            margin-top: 3px;
        }

        /* Блоки кода */
        .code-block {
            background: #0d1e2e;
            color: #e3eaf1;
            border-radius: 18px;
            padding: 1.5rem 1.8rem;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.95rem;
            line-height: 1.7;
            margin: 1.5rem 0;
            overflow-x: auto;
            white-space: pre-wrap;
            word-break: break-word;
            box-shadow: 0 10px 20px -8px rgba(0, 0, 0, 0.3);
            border: 1px solid #2a4055;
        }

        .code-block .comment {
            color: #7a9bb5;
        }

        .code-block .output {
            color: #b3d9ff;
            background: #152b3d;
            display: block;
            padding: 0.4rem 1rem;
            margin: 0.8rem -1rem 0;
            border-radius: 8px;
            border-left: 4px solid #3b9bd8;
            font-style: italic;
            font-size: 0.9rem;
        }

        .inline-code {
            background: #e8eef5;
            padding: 0.2rem 0.5rem;
            border-radius: 6px;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.85rem;
            color: #1d4e7a;
            border: 1px solid #d0ddee;
        }

        /* Таблицы */
        .table-wrap {
            overflow-x: auto;
            margin: 1.5rem 0;
            border-radius: 16px;
            border: 1px solid #dce5f0;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.95rem;
            background: white;
        }

        th {
            background: #e5eff9;
            padding: 0.9rem 1.2rem;
            text-align: left;
            font-weight: 600;
            color: #0b2b4b;
            border-bottom: 2px solid #cbdae9;
        }

        td {
            padding: 0.8rem 1.2rem;
            border-bottom: 1px solid #e3ebf4;
        }

        tr:last-child td {
            border-bottom: none;
        }

        tr:hover td {
            background: #f6faff;
        }

        /* Диаграмма переменных */
        .var-diagram {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 2.5rem;
            margin: 2rem 0;
            text-align: center;
        }

        .var-box {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .box-value {
            background: #eaf2fb;
            border: 2px solid #2b6f9e;
            border-radius: 14px;
            padding: 0.8rem 1.8rem;
            font-weight: 600;
            color: #0b2b4b;
            font-size: 1.1rem;
            box-shadow: 0 6px 0 #b3cde0;
        }

        .box-label {
            margin-top: 8px;
            font-family: 'JetBrains Mono', monospace;
            background: #1f3a54;
            color: white;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.8rem;
            font-weight: 500;
        }

        /* Кнопки-аккордеоны */
        .accordion {
            background: #f3f8ff;
            border-radius: 14px;
            padding: 0.8rem 1.5rem;
            margin: 1.5rem 0 0.5rem;
            border: 1px solid #cfdff0;
            cursor: pointer;
            font-weight: 600;
            color: #1a4970;
            display: flex;
            align-items: center;
            gap: 12px;
            transition: background 0.2s;
            user-select: none;
        }

        .accordion i {
            transition: transform 0.25s;
        }

        .accordion.open i {
            transform: rotate(90deg);
        }

        .accordion:hover {
            background: #e7f0fc;
        }

        .solution {
            display: none;
            background: #f0f9f0;
            padding: 1.4rem 1.8rem;
            border-radius: 0 0 16px 16px;
            border-left: 6px solid #2e8b57;
            margin-top: -4px;
            font-family: 'JetBrains Mono', monospace;
            font-size: 0.9rem;
            white-space: pre-wrap;
            color: #1b4d1b;
            border: 1px solid #b8ddb8;
            border-top: none;
        }

        .solution.show {
            display: block;
        }

        /* Вызовы к действию */
        .try-it {
            background: linear-gradient(135deg, #f9fcff 0%, #eaf3fc 100%);
            padding: 1.8rem 2rem;
            border-radius: 24px;
            margin: 2rem 0;
            border: 1px solid #c7dcf0;
            box-shadow: inset 0 1px 4px rgba(255, 255, 255, 0.8);
        }

        .try-it h3 {
            margin-top: 0;
            display: flex;
            align-items: center;
            gap: 12px;
            color: #0e3d63;
        }

        .try-it h3 i {
            color: #e6a017;
        }

        .badge {
            display: inline-block;
            background: #d4e6fa;
            padding: 0.2rem 0.9rem;
            border-radius: 30px;
            font-size: 0.75rem;
            font-weight: 600;
            letter-spacing: 0.3px;
            text-transform: uppercase;
            color: #1d4e7a;
        }

        .footer-note {
            margin-top: 3rem;
            padding-top: 1.8rem;
            border-top: 2px dashed #cbdae9;
            display: flex;
            justify-content: space-between;
            align-items: center;
            flex-wrap: wrap;
            gap: 1rem;
            color: #3a5b7a;
            font-weight: 500;
        }

        .footer-note a {
            color: #1d6fa5;
            text-decoration: none;
            font-weight: 600;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .footer-note a:hover {
            text-decoration: underline;
        }

        /* Адаптивность */
        @media (max-width: 650px) {
            .notebook {
                padding: 1.8rem 1.2rem;
            }
            .hero h1 {
                font-size: 1.8rem;
            }
            .meta-bar {
                border-radius: 20px;
                flex-direction: column;
                gap: 0.5rem;
            }
            h2 {
                font-size: 1.5rem;
            }
            .code-block {
                padding: 1.2rem 1rem;
                font-size: 0.85rem;
            }
            .var-diagram {
                gap: 1.2rem;
            }
        }

        /* Дополнительные утилиты */
        .mt-2 { margin-top: 1.5rem; }
        .mb-2 { margin-bottom: 1.5rem; }
        .text-accent { color: #2b6f9e; font-weight: 600; }
        .highlight { background: #fff2cc; padding: 0.1rem 0.3rem; border-radius: 4px; }
    </style>
</head>
<body>
    <div class="notebook">
        <!-- Шапка -->
        <div class="hero">
            <h1>
                <i class="fas fa-snake"></i> 
                Путешествие на планету Пайтон
            </h1>
            <div class="meta-bar">
                <span><i class="fas fa-track"></i> Вводная сессия — Блокнот 1 из 5</span>
                <span><i class="fas fa-clock"></i> ~15 мин</span>
                <span><i class="fas fa-graduation-cap"></i> для начинающих</span>
            </div>
        </div>

        <!-- Приветствие -->
        <section>
            <p style="font-size: 1.1rem;">Добро пожаловать! В течение следующих 15 минут вы напишете свои первые строки на Python — языке, который лежит в основе большинства современных методов обработки данных и искусственного интеллекта. Опыт программирования не требуется: мы не торопимся, и все необходимое вы найдете на этой странице.</p>
        </section>

        <!-- Цели обучения -->
        <section>
            <h2><i class="fas fa-bullseye"></i> 🎯 Цели обучения</h2>
            <p>К концу этого курса вы сможете:</p>
            <div class="goals-grid">
                <div class="goal-item"><i class="fas fa-check-circle"></i> Запускать код в Jupyter Notebook (и узнаете, что такое ноутбук).</div>
                <div class="goal-item"><i class="fas fa-check-circle"></i> Ознакомиться с базовым синтаксисом Python: операторы идут сверху вниз, а <span class="inline-code">#</span> комментарии — слева направо.</div>
                <div class="goal-item"><i class="fas fa-check-circle"></i> Сохранять значения в переменных и использовать их повторно.</div>
                <div class="goal-item"><i class="fas fa-check-circle"></i> Назвать четыре основных типа данных — <span class="inline-code">int</span>, <span class="inline-code">float</span>, <span class="inline-code">str</span>, <span class="inline-code">bool</span> — и проверить их с помощью <span class="inline-code">type()</span>.</div>
                <div class="goal-item"><i class="fas fa-check-circle"></i> Выполнить арифметические вычисления на Python и создать удобочитаемый вывод с помощью f-строк.</div>
            </div>
            <p><span class="badge">✅ Предпосылки</span> Ничего, кроме браузера, не нужно.</p>
            <p style="margin-top: 0.8rem;">➡️ <strong>Следующий:</strong> 02_data_structures.ipynb</p>
        </section>

        <!-- 1. Привет -->
        <section>
            <h2><i class="fas fa-hand-wave"></i> 1. Привет! Что такое Python и что представляет собой эта страница?</h2>
            <p>Python — это язык программирования, то есть способ давать компьютеру точные и воспроизводимые инструкции. Он доминирует в сфере обработки данных и искусственного интеллекта по двум причинам: он читается почти как английский, и на его основе огромное сообщество создало бесплатные инструменты — для таблиц данных, графиков, машинного обучения. Когда исследователи анализируют данные опросов, когда больница строит модель рисков, когда обучается современная система искусственного интеллекта, почти наверняка используется Python.</p>
            <p>Эта страница представляет собой блокнот Jupyter. В нем сочетаются два типа ячеек:</p>
            <ul style="margin-left: 1.8rem; margin-bottom: 1.2rem;">
                <li><strong>Текстовые ячейки</strong> (как эта) — примечания и пояснения.</li>
                <li><strong>Ячейки с кодом</strong> — настоящий Python, который вы можете запустить.</li>
            </ul>
            <p>Чтобы запустить ячейку с кодом: щелкните по ней, затем нажмите <span class="inline-code">Shift + Enter</span> (или нажмите кнопку ▶). Результат появится прямо под ячейкой.</p>
            <p>Это действительно все, что вам нужно знать. Давайте запустим вашу первую программу — щелкните по ячейке ниже и нажмите <strong>Shift + Enter</strong>:</p>

            <div class="code-block">
                <span class="comment"># Все, что идет после символа #, является комментарием — заметкой для людей. Python игнорирует их.</span><br><br>
                print("Привет, Python! 🐍")
                <span class="output">Привет, Python! 🐍</span>
            </div>

            <p>🎉 <strong>Вы только что запустили свою первую программу.</strong> Команда <span class="inline-code">print(...)</span> указывает Python на необходимость вывести на экран все, что находится в скобках.</p>
            <p>Первое знакомство с тем, как устроен код на Python:</p>
            <ul style="margin-left: 1.8rem; margin-bottom: 1.2rem;">
                <li>Python считывает ячейку <strong>сверху вниз</strong>, по одному выражению в строке, и выполняет именно то, что указано в каждой строке, — в указанном порядке.</li>
                <li>Все, что находится после <span class="inline-code">#</span>, является <strong>комментарием</strong>: только для читателей-людей, Python его игнорирует.</li>
                <li>Python также учитывает структуру строки: пробелы в начале строки имеют значение, а не служат для украшения. Пока нам это не нужно — это станет главной темой Notebook 3.</li>
            </ul>
            <p>И два практических совета для сеанса:</p>
            <ul style="margin-left: 1.8rem;">
                <li>Важен порядок, в котором вы запускаете ячейки, а не порядок их отображения на странице. Если что-то пошло не так, используйте Runtime → Перезапустить и запустить все (Colab), чтобы начать заново.</li>
                <li>Вы ничего не сломаете. Экспериментируйте смело — на ошибках все учатся программировать.</li>
            </ul>
            <p style="margin-top: 1.2rem; background: #f0f7fe; padding: 0.8rem 1.2rem; border-radius: 16px;">💬 <strong>Обсудить (30 секунд, с соседом):</strong> Где вы уже сталкивались с чем-то, созданным на основе данных или искусственного интеллекта, в вашей сфере деятельности или в повседневной жизни?</p>
        </section>

        <!-- 2. Переменные -->
        <section>
            <h2><i class="fas fa-box"></i> 2. Переменные — поля с подписями для ваших данных</h2>
            <p>Прежде чем компьютер сможет работать со значением, ему нужно где-то его сохранить. Переменная — это имя, присвоенное значению. Представьте, что это коробка с этикеткой:</p>

            <div class="var-diagram">
                <div class="var-box">
                    <div class="box-value">"Alice"</div>
                    <div class="box-label">name</div>
                </div>
                <div class="var-box">
                    <div class="box-value">25</div>
                    <div class="box-label">age</div>
                </div>
                <div class="var-box">
                    <div class="box-value">1.70</div>
                    <div class="box-label">height</div>
                </div>
            </div>

            <p>Вы помещаете значение в поле со знаком <span class="inline-code">=</span> (читается как "gets", а не "equals"): <span class="inline-code">age = 25</span> означает "поле с меткой age получает значение 25". С этого момента запись <span class="inline-code">age</span> в любом месте означает "заглянуть в это поле".</p>

            <div class="code-block">
                name = "Alice"      <span class="comment"># text goes in quotes</span><br>
                age = 25            <span class="comment"># a whole number</span><br>
                height = 1.70       <span class="comment"># a decimal number</span><br><br>
                print(name)<br>
                print(age)<br>
                print(height)<br><br>
                <span class="comment"># Variables can be reused and combined:</span><br>
                birth_year = 2026 - age<br>
                print(birth_year)
                <span class="output">Alice<br>25<br>1.7<br>2001</span>
            </div>

            <p>Читаем вывод: первые три строки просто показывают, что находится внутри каждого блока. Один небольшой сюрприз: мы ввели <span class="inline-code">1.70</span>, но Python вывел <span class="inline-code">1.7</span> — Python сохраняет значение числа, а не то, как вы его ввели. (Приведение чисел к виду, удобному для восприятия человеком, — отдельная задача, и в разделе 5 есть инструмент именно для этого.) Последняя строка демонстрирует настоящую мощь: мы вычислили новое значение на основе существующего. Если <span class="inline-code">age</span> изменится, мы внесем изменения в одно место, и все последующие изменения обновятся.</p>

            <p>Запомните два правила именования (есть и другие, но этих достаточно):</p>
            <ul style="margin-left: 1.8rem;">
                <li>Имена записываются в <strong>snake_case</strong>: слова в нижнем регистре, разделенные подчеркиванием, например <span class="inline-code">birth_year</span>, <span class="inline-code">coffee_price</span>.</li>
                <li>Выбирайте названия, которые отражают значение — <span class="inline-code">temperature</span> лучше, чем <span class="inline-code">t</span>.</li>
            </ul>

            <!-- Try it -->
            <div class="try-it">
                <h3><i class="fas fa-pencil-alt"></i> 🎯 Попробуйте (1–2 минуты) — свои собственные коробки</h3>
                <p>В ячейке ниже создайте две переменные: <span class="inline-code">my_name</span> (ваше имя в кавычках) и <span class="inline-code">my_age</span> (число). Затем <span class="inline-code">print</span> обе. Запустите ячейку, чтобы проверить.</p>
                <div class="code-block">
                    <span class="comment"># Your turn 👇  Replace the example values with your own, then press Shift + Enter.</span><br><br>
                    my_name = "..."<br>
                    my_age = 0<br><br>
                    print(my_name)<br>
                    print(my_age)
                    <span class="output">...<br>0</span>
                </div>
                <div class="accordion" onclick="toggleSolution(this)">
                    <i class="fas fa-chevron-right"></i> 💡 Нажмите, чтобы увидеть решение
                </div>
                <div class="solution">
                    my_name = "Мария"<br>
                    my_age = 28<br><br>
                    print(my_name)<br>
                    print(my_age)<br>
                    <span style="color: #2e6b2e;"># Вывод:<br># Мария<br># 28</span>
                </div>
            </div>
        </section>

        <!-- 3. Типы данных -->
        <section>
            <h2><i class="fas fa-tags"></i> 3. Типы данных — не все значения одинаковы</h2>
            <p>Посмотрите на электронную таблицу из любой области: в одних столбцах содержатся целые числа (участники), в других — десятичные дроби (измерения), в третьих — текст (названия городов), а в четвертых — ответы «да» или «нет». В Python то же самое. Четыре типа данных, с которыми вы будете сталкиваться каждый день:</p>

            <div class="table-wrap">
                <table>
                    <thead>
                        <tr><th>Тип</th><th>Имя Python</th><th>Пример</th><th>Типичное использование</th></tr>
                    </thead>
                    <tbody>
                        <tr><td>Целое число</td><td><span class="inline-code">int</span></td><td>42</td><td>количество, годы, идентификаторы</td></tr>
                        <tr><td>Десятичное число</td><td><span class="inline-code">float</span></td><td>19.99</td><td>измерения, цены, средние значения</td></tr>
                        <tr><td>Текст ("строка")</td><td><span class="inline-code">str</span></td><td>"Berlin"</td><td>имена, ярлыки, ответы</td></tr>
                        <tr><td>Да/Нет</td><td><span class="inline-code">bool</span></td><td>True, False</td><td>флаги, результаты сравнения</td></tr>
                    </tbody>
                </table>
            </div>

            <p>Добавить кодовую ячейку <span class="inline-code">Ctrl+M B</span> <span class="inline-code">type()</span></p>

            <div class="code-block">
                participants = 42          <span class="comment"># int</span><br>
                average_temp = 21.5        <span class="comment"># float</span><br>
                city = "Berlin"            <span class="comment"># str</span><br>
                survey_complete = True     <span class="comment"># bool</span><br><br>
                print(type(participants))<br>
                print(type(average_temp))<br>
                print(type(city))<br>
                print(type(survey_complete))
                <span class="output">&lt;class 'int'&gt;<br>&lt;class 'float'&gt;<br>&lt;class 'str'&gt;<br>&lt;class 'bool'&gt;</span>
            </div>

            <p>При чтении вывода: <span class="inline-code">&lt;class 'int'&gt;</span> выглядит более драматично, чем есть на самом деле. Слово в кавычках — это ответ — <span class="inline-code">int</span>, <span class="inline-code">float</span>, <span class="inline-code">str</span>, <span class="inline-code">bool</span>. (<span class="inline-code">class</span> — это просто собственное слово Python для обозначения «типа значения»; пока можете его не учитывать.)</p>
            <p>Зачем нужны типы? Потому что типы определяют, что вы можете сделать со значением. Вы можете перемножить два числа, но <span class="inline-code">"Berlin" * "Hamburg"</span> не имеет смысла — и Python вам об этом сообщит. Самая распространенная ошибка новичков: <span class="inline-code">"42"</span> (в кавычках) — это текст, а не число. <span class="inline-code">"42" + 1</span> приводит к ошибке; <span class="inline-code">42 + 1</span> приводит к <span class="inline-code">43</span>.</p>

            <div class="try-it">
                <h3><i class="fas fa-pencil-alt"></i> 🎯 Попробуйте (1–2 минуты) — Угадайте тип</h3>
                <p>Прежде чем запустить приведенную ниже ячейку, предскажите тип каждого значения. Затем запустите ее и проверьте свои предположения. (Подсказка для последней строки: считайте <span class="inline-code">7 > 3</span> вопросом — «7 больше 3?». Какой ответ можно дать на вопрос, требующий ответа «да» или «нет»?)</p>
                <div class="code-block">
                    <span class="comment"># Сначала предскажи, потом действуй!</span><br>
                    print(type(7))<br>
                    print(type(7.0))<br>
                    print(type("7"))<br>
                    print(type(7 > 3))
                    <span class="output">&lt;class 'int'&gt;<br>&lt;class 'float'&gt;<br>&lt;class 'str'&gt;<br>&lt;class 'bool'&gt;</span>
                </div>
                <div class="accordion" onclick="toggleSolution(this)">
                    <i class="fas fa-chevron-right"></i> 💡 Нажмите, чтобы увидеть решение
                </div>
                <div class="solution">
                    print(type(7))       # &lt;class 'int'&gt;<br>
                    print(type(7.0))     # &lt;class 'float'&gt;<br>
                    print(type("7"))     # &lt;class 'str'&gt;<br>
                    print(type(7 > 3))   # &lt;class 'bool'&gt;
                </div>
            </div>
        </section>

        <!-- 4. Арифметика -->
        <section>
            <h2><i class="fas fa-calculator"></i> 4. Арифметика — Python как очень надежный калькулятор</h2>
            <p>Python знает операторы из школьной математики:</p>

            <div class="table-wrap">
                <table>
                    <thead><tr><th>Оператор</th><th>Значение</th><th>Пример</th><th>Результат</th></tr></thead>
                    <tbody>
                        <tr><td><span class="inline-code">+</span></td><td>дополнение</td><td>7 + 3</td><td>10</td></tr>
                        <tr><td><span class="inline-code">-</span></td><td>вычитание</td><td>7 - 3</td><td>4</td></tr>
                        <tr><td><span class="inline-code">*</span></td><td>умножение</td><td>7 * 3</td><td>21</td></tr>
                        <tr><td><span class="inline-code">/</span></td><td>разделение</td><td>7 / 2</td><td>3.5</td></tr>
                        <tr><td><span class="inline-code">**</span></td><td>сила</td><td>2 ** 10</td><td>1024</td></tr>
                    </tbody>
                </table>
            </div>

            <p>Давайте объединим переменные и арифметику, чтобы произвести небольшой реальный расчет — сколько стоит ежедневная привычка пить кофе в год:</p>

            <div class="code-block">
                coffee_price = 3.20        <span class="comment"># euros per cup</span><br>
                cups_per_day = 2<br>
                days_per_year = 365<br><br>
                yearly_cost = coffee_price * cups_per_day * days_per_year<br>
                print("Coffee per year, in euros:")<br>
                print(yearly_cost)
                <span class="output">Кофе в год, в евро:<br>2336.0</span>
            </div>

            <p>Читаем результат: <span class="inline-code">2336.0</span> — эта ежедневная привычка — маленький праздник каждый год! Но почему <span class="inline-code">.0</span> в сумме в евро? Потому что <span class="inline-code">coffee_price</span> — это <span class="inline-code">float</span>, и если в операции участвует десятичное число, то результат тоже будет десятичным числом. (Деление с <span class="inline-code">/</span> всегда дает <span class="inline-code">float</span>, даже для <span class="inline-code">6 / 2</span>.) Типы из раздела 3 спокойно работают.</p>
        </section>

        <!-- 5. f-строки -->
        <section>
            <h2><i class="fas fa-font"></i> 5. Струны и f-струны — о ваших результатах</h2>
            <p>Простое число (<span class="inline-code">2336.0</span>) — это не результат, а "Кофе обходится вам в 2336 евро в год" — результат. Объединение текста и значений — настолько распространенная задача, что в Python для нее есть специальный инструмент: <strong>f-строка</strong>.</p>
            <p>Поставьте <span class="inline-code">f</span> перед открывающей кавычкой, и вы сможете заключить любую переменную или небольшое вычисление в фигурные скобки <span class="inline-code">{ }</span>. После двоеточия можно добавить инструкцию форматирования; чаще всего при работе с данными используются <span class="inline-code">:.2f</span> (ровно два знака после запятой) и <span class="inline-code">:,</span> (разделитель тысяч).</p>

            <div class="code-block">
                name = "Alice"<br>
                age = 25<br><br>
                <span class="comment"># Embedding values — even small calculations work inside { }</span><br>
                print(f"{name} is
