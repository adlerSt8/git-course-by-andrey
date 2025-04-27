---
layout: default
title: Работа с ветками
permalink: /lessons/04-branches/
nav_order: 4
---

<style>
  pre, code {
    background: #e9ecef;
    padding: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1rem;
    display: block;
    overflow-x: auto;
  }
  code {
    padding: 0.2rem 0.4rem;
    display: inline;
  }
</style>

<div style="text-align:center; margin: 2rem 0;">
  <h1 style="font-size:2.8rem;">🌳 Работа с ветками</h1>
  <p style="color:#555; font-size:1.3rem;">Создаём, переключаемся, сливаем и удаляем ветки в Git</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:2rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0; line-height:1.8; font-size:1.1rem;">
  <h2 style="font-size:1.8rem;">❓ Что такое ветка?</h2>
  <p>Ветка в Git — это указатель на определённый коммит, позволяющий работать над отдельными частями проекта, не затрагивая основную ветку (<code>main</code>). Ветки используются для разработки новых функций, исправления багов или экспериментов.</p>
  <p><strong>Зачем это нужно?</strong> Ветки позволяют Java-разработчикам изолировать изменения, например, добавление нового API в <code>Controller.java</code>, не рискуя сломать основной код. Это упрощает командную работу и обеспечивает безопасность проекта.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Ветка <code>main</code> обычно содержит стабильную версию проекта.</li>
    <li>Каждая ветка — это независимая линия разработки, которую можно слить с другими.</li>
    <li>Ветки легковесны: создание и переключение занимает доли секунды.</li>
  </ul>
  <p><strong>Пример:</strong> Вы работаете над Java-приложением и хотите добавить сортировку задач в <code>TaskService.java</code>. Вы создаёте ветку <code>feature-sorting</code>, вносите изменения, тестируете их, а затем сливаете в <code>main</code>, не затрагивая основной код до завершения работы.</p>
  
  <p><strong>Аналогия с дорогами:</strong> Представьте, что ваш проект — это большая дорога. Основная дорога — это <code>main</code>, по которой двигаются все машины (код). Если вы хотите протестировать новый маршрут (функцию), вы создаёте ответвление — ветку. Это временный путь, который не влияет на основную дорогу. Вы можете вернуть все изменения на главную дорогу, если маршрут окажется хорошим.</p>

  <p style="font-style:italic; color:#555;">Ветки — ваш способ безопасно экспериментировать!</p>

  <h2 style="font-size:1.8rem;">🌱 Создание новой ветки</h2>
  <p>Создание ветки позволяет начать работу над новой задачей, не изменяя основную ветку.</p>
  <p><strong>Зачем это нужно?</strong> Для Java-разработчиков ветки критично важны при разработке новых функций (например, REST-эндпоинта) или исправлении багов, чтобы не нарушить рабочую версию приложения.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команда <code>git branch</code> создаёт ветку, но не переключает на неё.</li>
    <li>Имя ветки обычно отражает задачу, например, <code>feature-x</code> или <code>bugfix-login</code>.</li>
    <li>Ветки создаются на основе текущего коммита.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте ветку <code>feature-x</code>:</li>
    <pre><code>git branch feature-x</code></pre>
  </ol>
  <p><strong>Пример:</strong> В репозитории <code>JavaDev/my-first-repo</code> вы создаёте ветку <code>feature-x</code> для разработки новой функции в <code>Main.java</code>. Ветка готова, но вы всё ещё в <code>main</code>, пока не переключитесь.</p>

  <p><strong>Аналогия с комнатами:</strong> Представьте, что ваш проект — это дом. Основная комната — это <code>main</code>. Если вы хотите сделать ремонт (новую функцию), вы создаёте новую комнату (ветку), в которой работаете, не вмешиваясь в остальной дом. Когда ремонт завершён, вы сливаете новую комнату с основным пространством.</p>

  <p style="font-style:italic; color:#555;">Создание ветки открывает новую линию разработки!</p>

  <h2 style="font-size:1.8rem;">🔄 Переключение на ветку</h2>
  <p>Переключение на ветку позволяет начать работу в новой линии разработки, изолируя изменения от других веток.</p>
  <p><strong>Зачем это нужно?</strong> Переключение на ветку, например, <code>feature-x</code>, позволяет Java-разработчикам редактировать файлы, такие как <code>Service.java</code>, не затрагивая стабильный код в <code>main</code>.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команда <code>git checkout</code> или <code>git switch</code> (с Git 2.23) переключает на указанную ветку.</li>
    <li>Переключение обновляет рабочую директорию до состояния ветки.</li>
    <li>Текущая ветка отображается в команде <code>git status</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Переключитесь на ветку <code>feature-x</code>:</li>
    <pre><code>git checkout feature-x</code></pre>
    <p>Или, используя современную команду:</p>
    <pre><code>git switch feature-x</code></pre>
  </ol>
  <p><strong>Пример:</strong> Вы переключились на <code>feature-x</code> в репозитории <code>my-first-repo</code>. Теперь вы можете добавить новый Java-класс, например, <code>FeatureX.java</code>, и изменения сохранятся только в этой ветке.</p>

  <p><strong>Аналогия с дорогами:</strong> Переключение на ветку — это как изменение маршрута. Например, вы ехали по основной дороге, а теперь повернули на новый, временный путь, чтобы проверить другую дорогу или новый маршрут.</p>

  <p style="font-style:italic; color:#555;">Переключение на ветку — ваш старт для изменений!</p>

  <h2 style="font-size:1.8rem;">📝 Работа в новой ветке</h2>
  <p>Работа в ветке включает создание файлов, редактирование кода и фиксацию изменений, которые остаются изолированными от других веток.</p>
  <p><strong>Зачем это нужно?</strong> Ветки позволяют Java-разработчикам тестировать новые функции, такие как обработка исключений в <code>Controller.java</code>, без риска для основного проекта.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Изменения в ветке фиксируются через <code>git add</code> и <code>git commit</code>.</li>
    <li>Коммиты в ветке не влияют на другие ветки, пока не выполнено слияние.</li>
    <li>Можно создавать сколько угодно веток для разных задач.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте файл <code>feature.txt</code>:</li>
    <pre><code>echo "Это новая фича" > feature.txt</code></pre>
    <li>Добавьте файл в индекс:</li>
    <pre><code>git add feature.txt</code></pre>
    <li>Создайте коммит:</li>
    <pre><code>git commit -m "Добавлен новый файл для feature-x"</code></pre>
  </ol>
  <p><strong>Пример:</strong> В ветке <code>feature-x</code> вы добавили <code>feature.txt</code> и зафиксировали изменения. Если вы создадите Java-класс <code>FeatureX.java</code> с новым методом, он тоже будет сохранён только в этой ветке, пока вы не сольёте её с <code>main</code>.</p>

  <p><strong>Аналогия с комнатами:</strong> Это как ремонт в новой комнате. Вы добавляете мебель (код), делаете изменения, и пока не завершите работу и не откроете её, комната остаётся отдельной.</p>

  <p style="font-style:italic; color:#555;">Работа в ветке сохраняет ваш код в безопасности!</p>

  <h2 style="font-size:1.8rem;">🔗 Слияние веток</h2>
  <p>После завершения работы в ветке, нужно слить её изменения в основную ветку, чтобы они стали частью проекта.</p>
  <p><strong>Зачем это нужно?</strong> Слияние позволяет Java-разработчикам интегрировать новые функции и исправления, например, в <code>Main.java</code>, в основную версию проекта.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Слияние выполняется через <code>git merge</code>, когда вы переключились на основную ветку.</li>
    <li>Если изменения не конфликтуют, слияние происходит автоматически.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Переключитесь на основную ветку:</li>
    <pre><code>git checkout main</code></pre>
    <li>Слейте изменения из ветки <code>feature-x</code>:</li>
    <pre><code>git merge feature-x</code></pre>
  </ol>
  <p><strong>Пример:</strong> После того, как вы закончили работу в ветке <code>feature-x</code>, вы сливаете её изменения в <code>main</code> для интеграции новой функции в проект.</p>

  <p style="font-style:italic; color:#555;">Слияние — это момент, когда ваш код становится частью общего проекта!</p>

  <h2 style="font-size:1.8rem;">🗑️ Удаление ветки</h2>
  <p>После слияния ветки, если она больше не нужна, её можно удалить, чтобы очистить проект.</p>
  <p><strong>Зачем это нужно?</strong> Удаление веток помогает поддерживать чистоту проекта и избежать путаницы, особенно в крупных Java-приложениях с множеством веток.</p>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Удалите локальную ветку:</li>
    <pre><code>git branch -d feature-x</code></pre>
    <li>Удалите удалённую ветку:</li>
    <pre><code>git push origin --delete feature-x</code></pre>
  </ol>
  <p><strong>Пример:</strong> После слияния ветки <code>feature-x</code> с <code>main</code> вы удаляете её, чтобы проект оставался организованным и понятным.</p>
  <p style="font-style:italic; color:#555;">Удаление ветки — это шаг к поддержанию порядка в проекте!</p>
</div>
