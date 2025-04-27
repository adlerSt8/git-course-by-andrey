---
layout: default
title: Создание репозитория и первые коммиты
permalink: /lessons/03-create-repo/
nav_order: 3
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
  <h1 style="font-size:2.8rem;">📁 Создание репозитория и первые коммиты</h1>
  <p style="color:#555; font-size:1.3rem;">Настраиваем репозиторий на GitHub и делаем первые изменения</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:2rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0; line-height:1.8; font-size:1.1rem;">
  <h2 style="font-size:1.8rem;">🌐 Создание репозитория на GitHub</h2>
  <p>Репозиторий на GitHub — это место, где хранится ваш код, история изменений и файлы проекта. Создание репозитория — первый шаг к публикации и управлению вашим Java-проектом.</p>
  <p><strong>Зачем это нужно?</strong> Репозиторий позволяет централизованно хранить код, делиться им с коллегами и отслеживать изменения. Для Java-разработчиков это важно, так как проекты часто включают множество файлов (классы, конфигурации, зависимости), и репозиторий упрощает их организацию и совместную работу.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Публичные репозитории доступны всем, приватные — только приглашённым пользователям.</li>
    <li>Файл <code>README.md</code> служит главной страницей проекта, где описывается его назначение.</li>
    <li>Имя репозитория должно быть уникальным в пределах вашего аккаунта и отражать суть проекта.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите на <a href="https://github.com" style="color:#007bff; text-decoration:none;">GitHub</a> и войдите в свою учётную запись.</li>
    <li>Нажмите на <strong>+</strong> в правом верхнем углу и выберите <strong>New repository</strong>.</li>
    <li>Заполните поля:
      <ul style="padding-left:1.5rem;">
        <li><strong>Repository name</strong>: Например, <code>my-first-repo</code>.</li>
        <li><strong>Description</strong>: Например, "Мой первый репозиторий для обучения".</li>
        <li><strong>Public/Private</strong>: Выберите <strong>Public</strong> для открытого доступа.</li>
        <li><strong>Initialize this repository with a README</strong>: Поставьте галочку.</li>
      </ul>
    </li>
    <li>Нажмите <strong>Create repository</strong>.</li>
  </ol>
  <p><strong>Пример:</strong> Вы создали репозиторий <code>JavaDev/my-first-repo</code> с описанием "Мой первый Java-проект". После создания вы видите страницу с файлом <code>README.md</code>, который можно редактировать через веб-интерфейс GitHub. Теперь ваш проект доступен по ссылке <code>https://github.com/JavaDev/my-first-repo</code>.</p>
  <p style="font-style:italic; color:#555;">Создание репозитория — ваш первый шаг к публикации кода!</p>

  <h2 style="font-size:1.8rem;">💾 Клонирование репозитория на ваш компьютер</h2>
  <p>Клонирование копирует репозиторий с GitHub на ваш компьютер, чтобы вы могли работать с кодом локально. Это создаёт папку с файлами проекта и историей изменений.</p>
  <p><strong>Зачем это нужно?</strong> Локальная копия позволяет редактировать файлы в вашей IDE (например, IntelliJ IDEA), добавлять Java-классы и фиксировать изменения, не завися от интернета. Для Java-разработчиков клонирование — стандартный способ начать работу над проектом.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Клонирование через HTTPS проще для новичков, так как не требует настройки SSH.</li>
    <li>Команда <code>git clone</code> создаёт папку с именем репозитория (например, <code>my-first-repo</code>).</li>
    <li>После клонирования вы можете сразу начать работу с файлами, например, открыть проект в IDE.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите в ваш репозиторий на GitHub.</li>
    <li>Нажмите зелёную кнопку <strong>Code</strong> и скопируйте HTTPS-ссылку (например, <code>https://github.com/JavaDev/my-first-repo.git</code>).</li>
    <li>Откройте терминал и выполните:</li>
    ```
    <pre><code>git clone https://github.com/JavaDev/my-first-repo.git</code></pre>
    ```
    <li>Перейдите в папку репозитория:</li>
    ```
    <pre><code>cd my-first-repo</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы клонировали репозиторий <code>my-first-repo</code>, и на вашем компьютере появилась папка <code>my-first-repo</code> с файлом <code>README.md</code>. Вы открываете папку в IntelliJ IDEA, чтобы создать Java-класс, например, <code>Main.java</code>, и начать разработку.</p>
  <p style="font-style:italic; color:#555;">Клонирование соединяет ваш компьютер с GitHub!</p>

  <h2 style="font-size:1.8rem;">✍ Добавление файла и первый коммит</h2>
  <p>Коммит фиксирует изменения в вашем репозитории, создавая «снимок» файлов. Это позволяет отслеживать историю и возвращаться к предыдущим версиям.</p>
  <p><strong>Зачем это нужно?</strong> Коммиты — основа работы с Git. Для Java-разработчиков они важны, чтобы сохранять изменения в коде (например, новые классы или исправления багов) и делиться ими с командой. Первый коммит — это ваш первый вклад в проект.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команда <code>git add</code> добавляет файлы в «индекс» (список для коммита).</li>
    <li>Команда <code>git commit</code> сохраняет изменения с описанием (сообщением).</li>
    <li>Команда <code>git push</code> отправляет коммиты на GitHub.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте файл <code>hello-world.txt</code>:</li>
    ```
    <pre><code>echo "Hello, Git!" > hello-world.txt</code></pre>
    ```
    <li>Добавьте файл в индекс:</li>
    ```
    <pre><code>git add hello-world.txt</code></pre>
    ```
    <li>Создайте коммит:</li>
    ```
    <pre><code>git commit -m "Добавлен файл hello-world.txt"</code></pre>
    ```
    <li>Отправьте изменения на GitHub:</li>
    ```
    <pre><code>git push origin main</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы создали файл <code>hello-world.txt</code> в репозитории <code>my-first-repo</code>. После выполнения <code>git add</code> и <code>git commit</code> вы зафиксировали изменения с сообщением "Добавлен файл hello-world.txt". Команда <code>git push</code> отправила файл на GitHub, и теперь он виден в веб-интерфейсе. Если вы добавите Java-класс, например, <code>Main.java</code>, процесс будет аналогичным.</p>
  <p style="font-style:italic; color:#555;">Первый коммит — ваш первый шаг к управлению кодом!</p>

  <h2 style="font-size:1.8rem;">🔍 Проверка изменений на GitHub</h2>
  <p>После отправки изменений на GitHub вы можете проверить их в веб-интерфейсе, чтобы убедиться, что всё работает правильно.</p>
  <p><strong>Зачем это нужно?</strong> Проверка подтверждает, что ваши коммиты и файлы корректно загружены. Для Java-разработчиков это важно, чтобы убедиться, что команда видит последние изменения, например, новый класс или исправление бага.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Веб-интерфейс GitHub показывает файлы, коммиты и их сообщения.</li>
    <li>Раздел <strong>Commits</strong> отображает историю изменений с датами и авторами.</li>
    <li>Вы можете сравнить изменения между версиями файлов.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите на страницу вашего репозитория на GitHub.</li>
    <li>Обновите страницу или перейдите в раздел <strong>Commits</strong>.</li>
    <li>Проверьте, что файл <code>hello-world.txt</code> и коммит с сообщением "Добавлен файл hello-world.txt" отображаются.</li>
  </ol>
  <p><strong>Пример:</strong> Вы отправили файл <code>hello-world.txt</code> на GitHub. В веб-интерфейсе вы видите его в списке файлов, а в разделе <strong>Commits</strong> — ваш коммит с сообщением. Если вы добавите Java-класс, например, <code>Main.java</code>, он тоже появится после <code>git push</code>.</p>
  <p style="font-style:italic; color:#555;">Проверка на GitHub подтверждает ваш успех!</p>

  <h2 style="font-size:1.8rem;">🛠 Дополнительные команды Git</h2>
  <p>Git предоставляет множество команд для управления репозиториями. Вот несколько полезных для начинающих, которые помогут в работе с Java-проектами.</p>
  <p><strong>Зачем это нужно?</strong> Знание дополнительных команд позволяет эффективно управлять изменениями, исправлять ошибки и организовывать проект. Для Java-разработчиков это помогает поддерживать порядок в сложных проектах с множеством файлов.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Команды работают в терминале (например, Git Bash на Windows).</li>
    <li>Большинство команд безопасны, но некоторые (например, <code>git reset</code>) требуют осторожности.</li>
    <li>Команды можно комбинировать для сложных операций, например, отката изменений.</li>
  </ul>
  <p><strong>Команды:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Посмотреть статус репозитория:</strong> Показывает изменённые и индексированные файлы.</li>
    ```
    <pre><code>git status</code></pre>
    ```
    <li><strong>Просмотр истории коммитов:</strong> Показывает все коммиты.</li>
    ```
    <pre><code>git log</code></pre>
    ```
    <p>Для короткого вывода:</p>
    ```
    <pre><code>git log --oneline</code></pre>
    ```
    <li><strong>Отмена изменений в файле (до коммита):</strong> Восстанавливает файл до последнего коммита.</li>
    ```
    <pre><code>git checkout -- hello-world.txt</code></pre>
    ```
    <li><strong>Отмена последнего коммита:</strong> Сохраняет изменения в рабочем каталоге.</li>
    ```
    <pre><code>git reset --soft HEAD~1</code></pre>
    ```
    <li><strong>Удаление файла из репозитория:</strong> Удаляет файл из индекса, но оставляет локально.</li>
    ```
    <pre><code>git rm --cached hello-world.txt</code></pre>
    ```
    <li><strong>Создание нового репозитория локально:</strong> Инициализирует Git в папке.</li>
    ```
    <pre><code>git init</code></pre>
    ```
    <p>Добавление удалённого репозитория:</p>
    ```
    <pre><code>git remote add origin https://github.com/JavaDev/my-first-repo.git</code></pre>
    ```
  </ul>
  <p><strong>Пример:</strong> Вы случайно изменили <code>Main.java</code>, но хотите отменить изменения:</p>
  ```
  <pre><code>git checkout -- Main.java</code></pre>
  ```
  <p>Или вы сделали ошибочный коммит и отменяете его:</p>
  ```
  <pre><code>git reset --soft HEAD~1</code></pre>
  ```
  <p>Для проверки статуса вы используете:</p>
  ```
  <pre><code>git status</code></pre>
  ```
  <p>Это показывает, что <code>Main.java</code> готов к новому коммиту. Эти команды спасают при работе с Java-проектами.</p>
  <p style="font-style:italic; color:#555;">Дополнительные команды делают Git мощным инструментом!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/02-signup/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/04-branches/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>