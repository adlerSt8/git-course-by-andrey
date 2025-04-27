---
layout: default
title: Регистрация и настройка
permalink: /lessons/02-signup/
nav_order: 2
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
  <h1 style="font-size:2.8rem;">📝 Регистрация и настройка GitHub</h1>
  <p style="color:#555; font-size:1.3rem;">Создаём аккаунт и настраиваем Git на Windows, Linux и MacOS</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:2rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0; line-height:1.8; font-size:1.1rem;">
  <h2 style="font-size:1.8rem;">🌐 Регистрация на GitHub</h2>
  <p>Создание аккаунта на GitHub — это ваш вход в мир управления кодом и совместной разработки. Аккаунт позволяет создавать репозитории, публиковать проекты, вносить изменения через пул-реквесты, взаимодействовать с сообществом и использовать интеграции для автоматизации.</p>
  <p><strong>Зачем это нужно?</strong> Без аккаунта вы не сможете полноценно работать с GitHub: ни создавать свои проекты, ни вносить вклад в open-source, ни делиться кодом с коллегами. Для Java-разработчиков аккаунт открывает доступ к миллионам репозиториев, включая популярные библиотеки (например, Spring, Apache Maven), и позволяет демонстрировать свои проекты в портфолио.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Бесплатный план GitHub включает неограниченное количество публичных и приватных репозиториев, что достаточно для большинства начинающих.</li>
    <li>Имя пользователя становится частью URL ваших репозиториев (например, <code>github.com/JavaDev123</code>), поэтому выбирайте запоминающееся и профессиональное имя.</li>
    <li>Подтверждение email необходимо для безопасности и получения уведомлений о пул-реквестах, комментариях и обновлениях.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите на <a href="https://github.com" style="color:#007bff; text-decoration:none;">GitHub</a> и нажмите <strong>Sign up</strong> в правом верхнем углу.</li>
    <li>Введите email (например, <code>user@example.com</code>), выберите уникальное имя пользователя (например, <code>JavaDev123</code>) и создайте сложный пароль (не менее 8 символов, с буквами и цифрами).</li>
    <li>Выберите бесплатный план (<strong>Free</strong>) и пройдите проверку CAPTCHA, чтобы подтвердить, что вы не робот.</li>
    <li>Нажмите <strong>Create account</strong> и перейдите по ссылке в письме от GitHub для подтверждения email.</li>
  </ol>
  <p><strong>Пример:</strong> Вы регистрируетесь с именем <code>JavaDev123</code> и email <code>user@example.com</code>. После подтверждения email вы входите в аккаунт и создаёте репозиторий <code>JavaDev123/MyFirstApp</code> для своего Java-приложения. Теперь вы можете поделиться ссылкой <code>https://github.com/JavaDev123/MyFirstApp</code> с коллегами или добавить проект в резюме.</p>
  <p style="font-style:italic; color:#555;">Регистрация на GitHub открывает двери в сообщество разработчиков и инструменты для ваших проектов!</p>

  <h2 style="font-size:1.8rem;">🛠 Установка Git</h2>
  <p>Git — это распределённая система контроля версий, которая позволяет отслеживать изменения в коде, создавать ветки, фиксировать коммиты и синхронизировать проекты с GitHub. Установка Git на ваш компьютер — обязательный шаг для локальной работы с репозиториями.</p>
  <p><strong>Зачем это нужно?</strong> Git — основа работы с GitHub. Без него вы не сможете клонировать репозитории, вносить изменения или отправлять код на сервер. Для Java-разработчиков Git особенно важен, так как проекты часто включают множество файлов (классы, ресурсы, зависимости), и Git помогает управлять их версиями, избегать конфликтов и восстанавливать код при ошибках.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Git работает в командной строке, но интегрируется с IDE, такими как IntelliJ IDEA, для удобного управления.</li>
    <li>На Windows Git Bash предоставляет Unix-подобную среду для выполнения команд.</li>
    <li>Проверка версии (<code>git --version</code>) подтверждает, что Git установлен и готов к работе.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Windows:</strong> Скачайте установщик с <a href="https://git-scm.com/download/win" style="color:#007bff; text-decoration:none;">официального сайта</a>, запустите его и оставьте настройки по умолчанию. После установки найдите <strong>Git Bash</strong> в меню «Пуск».</li>
    <li><strong>Linux:</strong> Откройте терминал и установите Git:
      <ul style="padding-left:1.5rem;">
        <li>Для Ubuntu/Debian:</li>
        <pre><code>sudo apt update</code></pre>
        <pre><code>sudo apt install git</code></pre>
        <li>Для Fedora:</li>
        <pre><code>sudo dnf install git</code></pre>
      </ul>
    </li>
    <li><strong>MacOS:</strong> Установите Git через Homebrew:</li>
    <pre><code>brew install git</code></pre>
    <p>Если Homebrew не установлен, выполните:</p>
    <pre><code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</code></pre>
    <p>Или скачайте Git с <a href="https://git-scm.com/download/mac" style="color:#007bff; text-decoration:none;">официального сайта</a>.</p>
  </ul>
  <p>После установки проверьте версию:</p>
  <pre><code>git --version</code></pre>
  <p>Ожидаемый вывод: <code>git version 2.39.2</code> (или новее).</p>
  <p><strong>Пример:</strong> Вы установили Git на Ubuntu, выполнив <code>sudo apt install git</code>. Теперь вы клонируете Java-проект:</p>
  <pre><code>git clone https://github.com/JavaDev123/MyFirstApp.git</code></pre>
  <p>Это создаёт локальную копию репозитория в папке <code>MyFirstApp</code>. Вы открываете проект в IntelliJ IDEA, редактируете <code>Main.java</code> и фиксируете изменения:</p>
  <pre><code>git commit -m "Updated main method"</code></pre>
  <p>Git сохраняет историю, позволяя вам откатиться, если что-то пойдёт не так.</p>
  <p style="font-style:italic; color:#555;">Git — ваш надёжный помощник для управления кодом локально!</p>

  <h2 style="font-size:1.8rem;">⚙ Настройка Git</h2>
  <p>Настройка Git связывает ваши локальные коммиты с аккаунтом GitHub, добавляя ваше имя и email к каждому изменению. Это обеспечивает прозрачность и идентификацию авторства в проектах.</p>
  <p><strong>Зачем это нужно?</strong> Без настройки коммиты могут быть анонимными или подписаны случайными данными (например, именем пользователя компьютера). Для Java-разработчиков это критично в командной работе, где нужно чётко знать, кто внёс изменения в файлы, такие как <code>Service.java</code>, чтобы упростить код-ревью и отследить ответственность.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Глобальные настройки (<code>--global</code>) применяются ко всем репозиториям на вашем компьютере.</li>
    <li>Email должен совпадать с тем, что использовался при регистрации на GitHub, чтобы коммиты автоматически связывались с вашим аккаунтом.</li>
    <li>Проверка настроек помогает избежать ошибок, таких как неверный email.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Задайте имя:</li>
    <pre><code>git config --global user.name "Alex Smith"</code></pre>
    <li>Укажите email, связанный с GitHub:</li>
    <pre><code>git config --global user.email "user@example.com"</code></pre>
    <li>Проверьте настройки:</li>
    <pre><code>git config --list</code></pre>
    <p>Ожидаемый вывод включает:</p>
    <pre><code>user.name=Alex Smith</code></pre>
    <pre><code>user.email=user@example.com</code></pre>
  </ol>
  <p><strong>Пример:</strong> Вы настроили Git с именем <code>Alex Smith</code> и email <code>user@example.com</code>. В своём Java-проекте вы редактируете <code>Controller.java</code>, фиксируете изменения:</p>
  <pre><code>git commit -m "Fixed bug in API endpoint"</code></pre>
  <p>На GitHub в истории коммитов отображается <code>Alex Smith <user@example.com></code>. Коллеги видят, что именно вы исправили баг, и могут обсудить изменения в пул-реквесте.</p>
  <p style="font-style:italic; color:#555;">Настройка Git делает вашу работу видимой и профессиональной!</p>

  <h2 style="font-size:1.8rem;">🔑 Генерация SSH-ключа</h2>
  <p>SSH-ключ создаёт безопасное соединение между вашим компьютером и GitHub, позволяя работать с репозиториями без ввода пароля. Это пара ключей: приватный (хранится локально) и публичный (загружается на GitHub).</p>
  <p><strong>Зачем это нужно?</strong> SSH повышает безопасность и удобство. Пароли могут быть перехвачены или забыты, а SSH-ключи исключают необходимость ввода учётных данных при каждом <code>git push</code> или <code>git clone</code>. Для Java-разработчиков, работающих с частыми обновлениями кода, это экономит время и снижает риски.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>SSH использует криптографию RSA с длиной ключа 4096 бит для высокой безопасности.</li>
    <li>SSH-агент управляет ключами в фоновом режиме, упрощая доступ.</li>
    <li>Публичный ключ безопасно хранится на GitHub, а приватный никогда не покидает ваш компьютер.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Сгенерируйте ключ:</li>
    <pre><code>ssh-keygen -t rsa -b 4096 -C "user@example.com"</code></pre>
    <p>Нажмите Enter для стандартного пути (<code>~/.ssh/id_rsa</code>) и оставьте пароль пустым для простоты.</p>
    <li>Запустите SSH-агент:</li>
    <pre><code>eval "$(ssh-agent -s)"</code></pre>
    <p>Добавьте приватный ключ:</p>
    <pre><code>ssh-add ~/.ssh/id_rsa</code></pre>
    <li>Скопируйте публичный ключ:</li>
    <pre><code>cat ~/.ssh/id_rsa.pub</code></pre>
    <p>Перейдите в <a href="https://github.com/settings/keys" style="color:#007bff; text-decoration:none;">настройки GitHub</a>, нажмите <strong>New SSH key</strong>, вставьте ключ и сохраните.</p>
  </ol>
  <p><strong>Пример:</strong> Вы сгенерировали SSH-ключ и добавили публичный ключ на GitHub. Теперь вы клонируете свой Java-проект через SSH:</p>
  <pre><code>git clone git@github.com:JavaDev123/MyFirstApp.git</code></pre>
  <p>После изменений в <code>Main.java</code> вы пушите код:</p>
  <pre><code>git push origin main</code></pre>
  <p>Без ввода пароля! Это особенно удобно, если вы часто обновляете проект, например, добавляя новые Java-классы.</p>
  <p style="font-style:italic; color:#555;">SSH-ключи ускоряют и защищают вашу работу с GitHub!</p>

  <h2 style="font-size:1.8rem;">💻 GitHub Desktop (опционально)</h2>
  <p>GitHub Desktop — это графическое приложение для работы с Git и GitHub, которое упрощает управление репозиториями без необходимости использовать командную строку. Оно идеально для новичков или тех, кто предпочитает визуальный интерфейс.</p>
  <p><strong>Зачем это нужно?</strong> Командная строка может быть сложной для начинающих, а GitHub Desktop предоставляет интуитивный способ клонировать репозитории, делать коммиты и создавать пул-реквесты. Для Java-разработчиков это удобный инструмент для управления проектами, особенно если вы только начинаете изучать Git.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>GitHub Desktop автоматически синхронизируется с вашим аккаунт GitHub, показывая все ваши репозитории.</li>
    <li>Поддерживает базовые операции Git: клонирование, коммиты, пуш, пул-реквесты.</li>
    <li>Для Linux официальной версии нет, но альтернативы (GitKraken, Sublime Merge) предлагают схожий функционал.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Скачайте <a href="https://desktop.github.com" style="color:#007bff; text-decoration:none;">GitHub Desktop</a> для Windows или MacOS и установите.</li>
    <li>Войдите в свой аккаунт GitHub через приложение.</li>
    <li>Для Linux попробуйте GitKraken (<a href="https://www.gitkraken.com" style="color:#007bff; text-decoration:none;">сайт</a>) или Sublime Merge (<a href="https://www.sublimemerge.com" style="color:#007bff; text-decoration:none;">сайт</a>).</li>
  </ul>
  <p><strong>Пример:</strong> Вы установили GitHub Desktop на Windows и клонировали проект <code>JavaDev123/MyFirstApp</code>. В интерфейсе вы видите изменения в <code>Service.java</code>, добавляете описание «Improved error handling» и делаете коммит. Затем одним кликом отправляете изменения на GitHub и создаёте пул-реквест для обсуждения с командой.</p>
  <p style="font-style:italic; color:#555;">GitHub Desktop — простой способ начать работу с Git для новичков!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/01-intro/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/03-create-repo/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>