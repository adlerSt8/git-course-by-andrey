---
layout: default
title: Регистрация и настройка
permalink: /lessons/02-signup/
nav_order: 2
---

<div style="text-align:center; margin: 2rem 0;">
  <h1>📝 Регистрация и настройка GitHub</h1>
  <p style="color:#555; font-size:1.1rem;">Создаём аккаунт и настраиваем Git на Windows, Linux и MacOS</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0;">
  <h2>🌐 Регистрация на GitHub</h2>
  <p>Создание аккаунта на GitHub — это первый шаг к управлению вашими проектами и участию в сообществе разработчиков. Аккаунт позволяет хранить код, делиться проектами, вносить изменения через пул-реквесты и взаимодействовать с другими разработчиками.</p>
  <p><strong>Зачем это нужно?</strong> Без аккаунта вы не сможете создавать репозитории, публиковать код или участвовать в совместной работе. Например, если вы хотите поделиться своим Java-проектом или внести вклад в open-source библиотеку, вам нужен аккаунт.</p>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите на <a href="https://github.com" style="color:#007bff; text-decoration:none;">GitHub</a> и нажмите <strong>Sign up</strong> в правом верхнем углу.</li>
    <li>Введите ваш email (например, <code>user@example.com</code>), выберите уникальное имя пользователя (например, <code>JavaDev123</code>) и придумайте сложный пароль.</li>
    <li>Выберите бесплатный план (<strong>Free</strong>), который подходит для большинства пользователей, и пройдите проверку на робота.</li>
    <li>Нажмите <strong>Create account</strong> и подтвердите email по ссылке в письме.</li>
  </ol>
  <p><strong>Пример:</strong> Допустим, вы регистрируетесь как <code>JavaDev123</code>. После создания аккаунта вы сможете создать репозиторий для своего Java-проекта, например, <code>JavaDev123/MyFirstApp</code>, и поделиться им с коллегами.</p>
  <p style="font-style:italic; color:#555;">Регистрация открывает доступ к миллионам проектов и инструментов для совместной разработки!</p>

  <h2>🛠 Установка Git</h2>
  <p>Git — это система контроля версий, которая позволяет отслеживать изменения в коде, работать с ветками и синхронизировать проекты с GitHub. Установка Git на ваш компьютер необходима для локальной работы с репозиториями.</p>
  <p><strong>Зачем это нужно?</strong> Без Git вы не сможете клонировать репозитории, фиксировать изменения (коммиты) или отправлять код на GitHub. Например, если вы пишете Java-код, Git поможет сохранить историю изменений и откатиться к предыдущей версии при ошибке.</p>
  <p><strong>Шаги:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Windows:</strong> Скачайте установщик с <a href="https://git-scm.com/download/win" style="color:#007bff; text-decoration:none;">официального сайта</a>, запустите его и оставьте настройки по умолчанию. После установки откройте <strong>Git Bash</strong> из меню «Пуск».</li>
    <li><strong>Linux:</strong> Откройте терминал и установите Git:
      <ul style="padding-left:1.5rem;">
        <li>Для Ubuntu/Debian: <code>sudo apt update && sudo apt install git</code></li>
        <li>Для Fedora: <code>sudo dnf install git</code></li>
      </ul>
    </li>
    <li><strong>MacOS:</strong> Установите Git через Homebrew (<code>brew install git</code>) или скачайте с <a href="https://git-scm.com/download/mac" style="color:#007bff; text-decoration:none;">сайта</a>. Для Homebrew, если он не установлен, выполните: <code>/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"</code>.</li>
  </ul>
  <p>После установки проверьте версию: <code>git --version</code>. Вы должны увидеть что-то вроде <code>git version 2.39.2</code>.</p>
  <p><strong>Пример:</strong> Вы установили Git на Windows и открыли Git Bash. Теперь вы можете клонировать репозиторий командой <code>git clone https://github.com/JavaDev123/MyFirstApp.git</code>, чтобы начать работу с проектом локально.</p>
  <p style="font-style:italic; color:#555;">Git — ваш инструмент для управления версиями кода на компьютере.</p>

  <h2>⚙ Настройка Git</h2>
  <p>Настройка Git связывает ваши локальные изменения с аккаунтом GitHub, чтобы коммиты ассоциировались с вашим именем и email. Это важно для идентификации автора изменений в проекте.</p>
  <p><strong>Зачем это нужно?</strong> Без настройки ваши коммиты могут быть анонимными, и коллеги не узнают, кто внёс изменения. Например, если вы работаете в команде над Java-приложением, ваши коммиты будут подписаны вашим именем, что упрощает код-ревью.</p>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Задайте имя: <code>git config --global user.name "Ваше Имя"</code> (например, <code>git config --global user.name "Alex Smith"</code>).</li>
    <li>Укажите email, связанный с GitHub: <code>git config --global user.email "ваш.емейл@домен.com"</code> (например, <code>git config --global user.email "user@example.com"</code>).</li>
    <li>Проверьте настройки: <code>git config --list</code>. Вы увидите строки вроде <code>user.name=Alex Smith</code> и <code>user.email=user@example.com</code>.</li>
  </ol>
  <p><strong>Пример:</strong> Вы настроили Git с именем «Alex Smith» и email «user@example.com». Теперь, когда вы сделаете коммит (например, <code>git commit -m "Add main.java"</code>), он будет подписан как «Alex Smith <user@example.com>», и на GitHub это отобразится в истории изменений.</p>
  <p style="font-style:italic; color:#555;">Правильная настройка Git делает вашу работу прозрачной для команды.</p>

  <h2>🔑 Генерация SSH-ключа</h2>
  <p>SSH-ключ обеспечивает безопасное соединение между вашим компьютером и GitHub, позволяя работать с репозиториями без ввода пароля. Это пара ключей: приватный (хранится локально) и публичный (добавляется на GitHub).</p>
  <p><strong>Зачем это нужно?</strong> SSH упрощает работу и повышает безопасность. Например, вместо ввода пароля при каждом <code>git push</code> вы используете ключ, что удобно при частых обновлениях Java-проекта. Также SSH защищает от перехвата пароля.</p>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Сгенерируйте ключ: <code>ssh-keygen -t rsa -b 4096 -C "ваш.емейл@домен.com"</code>. Нажмите Enter для стандартного пути (<code>~/.ssh/id_rsa</code>) и оставьте пароль пустым для простоты.</li>
    <li>Запустите SSH-агент: <code>eval "$(ssh-agent -s)"</code>, затем добавьте ключ: <code>ssh-add ~/.ssh/id_rsa</code>.</li>
    <li>Скопируйте публичный ключ: <code>cat ~/.ssh/id_rsa.pub</code>. Перейдите в <a href="https://github.com/settings/keys" style="color:#007bff; text-decoration:none;">настройки GitHub</a>, нажмите <strong>New SSH key</strong>, вставьте ключ и сохраните.</li>
  </ol>
  <p><strong>Пример:</strong> Вы сгенерировали SSH-ключ и добавили публичный ключ на GitHub. Теперь вместо HTTPS-ссылки (<code>https://github.com/JavaDev123/MyFirstApp.git</code>) вы используете SSH (<code>git@github.com:JavaDev123/MyFirstApp.git</code>) для <code>git clone</code> или  <code>git push</code>, и пушите изменения без ввода пароля.</p>
  <p style="font-style:italic; color:#555;">SSH-ключи делают вашу работу быстрой и безопасной.</p>

  <h2>💻 GitHub Desktop (опционально)</h2>
  <p>GitHub Desktop — это графический интерфейс для работы с Git и GitHub, который упрощает управление репозиториями без командной строки. Он подходит для новичков или тех, кто предпочитает визуальные инструменты.</p>
  <p><strong>Зачем это нужно?</strong> GitHub Desktop позволяет клонировать репозитории, делать коммиты и пул-реквесты через удобный интерфейс. Например, вы можете использовать его для управления Java-проектом, если не хотите запоминать команды Git.</p>
  <p><strong>Шаги:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Скачайте <a href="https://desktop.github.com" style="color:#007bff; text-decoration:none;">GitHub Desktop</a> для Windows или MacOS и установите.</li>
    <li>Войдите в свой аккаунт GitHub через приложение.</li>
    <li>Для Linux используйте альтернативы, такие как GitKraken или Sublime Merge.</li>
  </ul>
  <p><strong>Пример:</strong> Вы установили GitHub Desktop и клонировали свой проект <code>MyFirstApp</code>. Через интерфейс вы видите изменения в файле <code>Main.java</code>, делаете коммит с описанием «Added new feature» и отправляете изменения на GitHub одним кликом.</p>
  <p style="font-style:italic; color:#555;">GitHub Desktop — отличный старт для тех, кто только начинает!</p>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>