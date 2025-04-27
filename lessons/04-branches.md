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
    ```
    <pre><code>git branch feature-x</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> В репозитории <code>JavaDev/my-first-repo</code> вы создаёте ветку <code>feature-x</code> для разработки новой функции в <code>Main.java</code>. Ветка готова, но вы всё ещё в <code>main</code>, пока не переключитесь.</p>
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
    ```
    <pre><code>git checkout feature-x</code></pre>
    ```
    <p>Или, используя современную команду:</p>
    ```
    <pre><code>git switch feature-x</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы переключились на <code>feature-x</code> в репозитории <code>my-first-repo</code>. Теперь вы можете добавить новый Java-класс, например, <code>FeatureX.java</code>, и изменения сохранятся только в этой ветке.</p>
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
    ```
    <pre><code>echo "Это новая фича" > feature.txt</code></pre>
    ```
    <li>Добавьте файл в индекс:</li>
    ```
    <pre><code>git add feature.txt</code></pre>
    ```
    <li>Создайте коммит:</li>
    ```
    <pre><code>git commit -m "Добавлен новый файл для feature-x"</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> В ветке <code>feature-x</code> вы добавили <code>feature.txt</code> и зафиксировали изменения. Если вы создадите Java-класс <code>FeatureX.java</code> с новым методом, он тоже будет сохранён только в этой ветке, пока вы не сольёте её с <code>main</code>.</p>
  <p style="font-style:italic; color:#555;">Работа в ветке сохраняет ваш код в безопасности!</p>

  <h2 style="font-size:1.8rem;">🔎 Просмотр веток</h2>
  <p>Команда <code>git branch</code> показывает все ветки в репозитории и текущую активную ветку.</p>
  <p><strong>Зачем это нужно?</strong> Просмотр веток помогает Java-разработчикам отслеживать, какие задачи в работе (например, ветка для нового API или исправления бага) и на какой ветке они находятся.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Текущая ветка отмечена звёздочкой в выводе <code>git branch</code>.</li>
    <li>Команда полезна перед слиянием или переключением, чтобы не запутаться.</li>
    <li>Можно увидеть ветки на GitHub в разделе <strong>Branches</strong>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Просмотрите список веток:</li>
    ```
    <pre><code>git branch</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы выполняете <code>git branch</code> и видите ветки <code>main</code> и <code>feature-x</code>, где <code>feature-x</code> отмечена звёздочкой, так как вы в ней. Это подтверждает, что вы работаете над новым Java-классом в правильной ветке.</p>
  <p style="font-style:italic; color:#555;">Просмотр веток держит вас в курсе проекта!</p>

  <h2 style="font-size:1.8rem;">🤝 Слияние веток</h2>
  <p>Слияние веток объединяет изменения из одной ветки (например, <code>feature-x</code>) в другую (например, <code>main</code>), чтобы включить новые функции или исправления в основной проект.</p>
  <p><strong>Зачем это нужно?</strong> Слияние позволяет Java-разработчикам интегрировать новый код, такой как обновлённый <code>Service.java</code>, в стабильную версию, сохраняя историю изменений.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Слияние выполняется командой <code>git merge</code> в целевой ветке.</li>
    <li>Если изменения не конфликтуют, слияние проходит автоматически.</li>
    <li>После слияния изменения можно отправить на GitHub через <code>git push</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Переключитесь на ветку <code>main</code>:</li>
    ```
    <pre><code>git checkout main</code></pre>
    ```
    <p>Или:</p>
    ```
    <pre><code>git switch main</code></pre>
    ```
    <li>Слейте ветку <code>feature-x</code>:</li>
    ```
    <pre><code>git merge feature-x</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы завершили работу над <code>FeatureX.java</code> в ветке <code>feature-x</code>. Переключившись на <code>main</code>, вы слили изменения с помощью <code>git merge feature-x</code>. Теперь новый класс доступен в основной ветке, и вы можете отправить его на GitHub с помощью <code>git push</code>.</p>
  <p style="font-style:italic; color:#555;">Слияние веток объединяет ваши идеи с проектом!</p>

  <h2 style="font-size:1.8rem;">🛠 Разрешение конфликтов при слиянии</h2>
  <p>Конфликты возникают, если изменения в ветках затрагивают одни и те же строки файла. Git требует ручного разрешения таких конфликтов.</p>
  <p><strong>Зачем это нужно?</strong> Конфликты — обычное явление в командной Java-разработке, например, когда два разработчика редактируют <code>Controller.java</code>. Разрешение конфликтов сохраняет целостность кода.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Git помечает конфликты в файлах с помощью маркеров (<code>&lt;&lt;&lt;&lt;&lt;&lt;&lt;</code>, <code>=======</code>, <code>&gt;&gt;&gt;&gt;&gt;&gt;&gt;</code>).</li>
    <li>После исправления конфликта нужно добавить файлы в индекс и завершить коммит.</li>
    <li>IDE, такие как IntelliJ IDEA, могут упростить разрешение конфликтов.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Откройте файл с конфликтом, например, <code>feature.txt</code>. Git отметит проблемные места:</li>
    ```
    <pre><code>&lt;&lt;&lt;&lt;&lt;&lt;&lt; HEAD
Это основная версия
=======
Это новая фича
&gt;&gt;&gt;&gt;&gt;&gt;&gt; feature-x</code></pre>
    ```
    <li>Отредактируйте файл, выбрав нужные изменения, и удалите маркеры.</li>
    <li>Добавьте исправленный файл:</li>
    ```
    <pre><code>git add feature.txt</code></pre>
    ```
    <li>Завершите слияние:</li>
    ```
    <pre><code>git commit</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> При слиянии <code>feature-x</code> в <code>main</code> возник конфликт в <code>Main.java</code>. Вы открыли файл, выбрали нужные изменения, удалили маркеры, добавили файл в индекс и завершили коммит. Теперь код согласован и готов к отправке на GitHub.</p>
  <p style="font-style:italic; color:#555;">Разрешение конфликтов сохраняет гармонию в коде!</p>

  <h2 style="font-size:1.8rem;">🗑 Удаление ветки</h2>
  <p>Удаление ветки очищает репозиторий от ненужных веток после их слияния.</p>
  <p><strong>Зачем это нужно?</strong> Удаление веток поддерживает порядок в репозитории, что важно для Java-проектов с множеством задач и веток.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команда <code>git branch -d</code> безопасно удаляет слитую ветку.</li>
    <li>Команда <code>git branch -D</code> принудительно удаляет ветку, даже если она не слита.</li>
    <li>Удаление удалённой ветки требует команды <code>git push origin --delete</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Удалите локальную ветку <code>feature-x</code>:</li>
    ```
    <pre><code>git branch -d feature-x</code></pre>
    ```
    <p>Или принудительно:</p>
    ```
    <pre><code>git branch -D feature-x</code></pre>
    ```
    <li>Удалите ветку на GitHub:</li>
    ```
    <pre><code>git push origin --delete feature-x</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> После слияния <code>feature-x</code> в <code>main</code> вы удалили ветку локально с помощью <code>git branch -d feature-x</code> и на GitHub с помощью <code>git push origin --delete feature-x</code>. Репозиторий <code>my-first-repo</code> теперь содержит только <code>main</code> с новым кодом из <code>FeatureX.java</code>.</p>
  <p style="font-style:italic; color:#555;">Удаление веток поддерживает чистоту проекта!</p>

  <h2 style="font-size:1.8rem;">🌍 Работа с удалёнными ветками</h2>
  <p>Удалённые ветки хранятся на GitHub и синхронизируются с локальными для совместной работы.</p>
  <p><strong>Зачем это нужно?</strong> В командной Java-разработке удалённые ветки позволяют делиться кодом, например, новым <code>Repository.java</code>, с коллегами через GitHub.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команда <code>git push</code> отправляет локальную ветку на GitHub.</li>
    <li>Команда <code>git fetch</code> загружает информацию об удалённых ветках.</li>
    <li>Удалённые ветки отображаются в формате <code>origin/branch-name</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Отправьте ветку <code>feature-x</code> на GitHub:</li>
    ```
    <pre><code>git push origin feature-x</code></pre>
    ```
    <li>Загрузите и переключитесь на удалённую ветку:</li>
    ```
    <pre><code>git fetch origin</code></pre>
    <pre><code>git checkout -b feature-x origin/feature-x</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы отправили ветку <code>feature-x</code> с новым <code>Service.java</code> на GitHub. Коллега загрузил её с помощью <code>git fetch</code> и <code>git checkout -b feature-x origin/feature-x</code>, чтобы продолжить работу. Это обеспечивает синхронизацию команды.</p>
  <p style="font-style:italic; color:#555;">Удалённые ветки связывают вашу команду!</p>

  <h2 style="font-size:1.8rem;">🔧 Дополнительные полезные команды</h2>
  <p>Эти команды упрощают работу с ветками и помогают в различных сценариях.</p>
  <p><strong>Зачем это нужно?</strong> Дополнительные команды ускоряют процессы и решают специфические задачи, такие как переименование ветки или быстрое создание, что полезно для Java-проектов.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команды оптимизируют рутинные операции.</li>
    <li>Большинство команд безопасны, но требуют понимания контекста.</li>
    <li>Интеграция с IDE упрощает их использование.</li>
  </ul>
  <p><strong>Команды:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создание и переключение на новую ветку:</strong></li>
    ```
    <pre><code>git checkout -b new-feature</code></pre>
    ```
    <li><strong>Слияние изменений из другой ветки:</strong></li>
    ```
    <pre><code>git merge another-branch</code></pre>
    ```
    <li><strong>Переименование текущей ветки:</strong></li>
    ```
    <pre><code>git branch -m new-branch-name</code></pre>
    ```
    <pre><code>Пример с пре, код</code></pre>
    ```
    <pre>Пример с пре</pre>
    ```
    <code>Пример с коде</code>
    ```
    <kbd>Пример с пре, код</kbd>
    ```
  </ul>
  <p><strong>Пример:</strong> Вы создали и переключились на ветку <code>new-feature</code> одной командой <code>git checkout -b new-feature</code>, добавили <code>Main.java</code>, а затем переименовали ветку в <code>feature-login</code> с помощью <code>git branch -m feature-login</code>. Это экономит время в Java-проекте.</p>
  <p style="font-style:italic; color:#555;">Дополнительные команды делают работу гибкой!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/03-create-repo/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/05-pull-requests/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>