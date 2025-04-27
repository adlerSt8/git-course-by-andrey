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

<div style="display:grid; grid-template-columns:repeat(auto-fit, minmax(300px, 1fr)); gap:1.5rem; margin:2rem 0;">
  <section style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
    <h2>🌐 Регистрация на GitHub</h2>
    <p>Создайте аккаунт для работы с репозиториями:</p>
    <ol style="padding-left:1.5rem; margin:0.5rem 0;">
      <li>Перейдите на <a href="https://github.com" style="color:#007bff; text-decoration:none;">GitHub</a> и нажмите <strong>Sign up</strong>.</li>
      <li>Введите email, уникальное имя пользователя и пароль.</li>
      <li>Выберите бесплатный план и подтвердите, что вы не робот.</li>
      <li>Нажмите <strong>Create account</strong>.</li>
    </ol>
    <p style="font-style:italic; color:#555;">Это ваш первый шаг к управлению проектами и участию в сообществе!</p>
  </section>

  <section style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
    <h2>🛠 Установка Git</h2>
    <p>Установите Git для работы с версиями кода:</p>
    <ul style="padding-left:1.5rem; margin:0.5rem 0;">
      <li><strong>Windows:</strong> Скачайте с <a href="https://git-scm.com/download/win" style="color:#007bff; text-decoration:none;">официального сайта</a>, установите с настройками по умолчанию.</li>
      <li><strong>Linux:</strong> Используйте <code>sudo apt install git</code> (Ubuntu) или <code>sudo dnf install git</code> (Fedora).</li>
      <li><strong>MacOS:</strong> Установите через <code>brew install git</code> или скачайте с сайта.</li>
    </ul>
    <p>Проверьте установку: <code>git --version</code>.</p>
  </section>

  <section style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
    <h2>⚙ Настройка Git</h2>
    <p>Свяжите Git с вашим аккаунтом:</p>
    <ol style="padding-left:1.5rem; margin:0.5rem 0;">
      <li>Задайте имя: <code>git config --global user.name "Ваше Имя"</code></li>
      <li>Укажите email: <code>git config --global user.email "ваш.емейл@домен.com"</code></li>
      <li>Проверьте: <code>git config --list</code></li>
    </ol>
    <p style="font-style:italic; color:#555;">Теперь ваши коммиты будут связаны с аккаунтом GitHub.</p>
  </section>

  <section style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
    <h2>🔑 Генерация SSH-ключа</h2>
    <p>Настройте безопасное соединение:</p>
    <ol style="padding-left:1.5rem; margin:0.5rem 0;">
      <li>Сгенерируйте ключ: <code>ssh-keygen -t rsa -b 4096 -C "ваш.емейл@домен.com"</code></li>
      <li>Запустите SSH-агент: <code>eval "$(ssh-agent -s)"</code> и добавьте ключ: <code>ssh-add ~/.ssh/id_rsa</code></li>
      <li>Скопируйте публичный ключ: <code>cat ~/.ssh/id_rsa.pub</code> и добавьте его в <a href="https://github.com/settings/keys" style="color:#007bff; text-decoration:none;">настройки GitHub</a>.</li>
    </ol>
    <p>SSH упрощает работу без ввода пароля.</p>
  </section>

  <section style="background:#f8f9fa; border-radius:8px; padding:1.5rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
    <h2>💻 GitHub Desktop (опционально)</h2>
    <p>Используйте графический интерфейс:</p>
    <ul style="padding-left:1.5rem; margin:0.5rem 0;">
      <li>Скачайте <a href="https://desktop.github.com" style="color:#007bff; text-decoration:none;">GitHub Desktop</a> для Windows/MacOS.</li>
      <li>Войдите в аккаунт и начните работу.</li>
      <li>Для Linux: попробуйте GitKraken или Sublime Merge.</li>
    </ul>
    <p style="font-style:italic; color:#555;">Подходит для новичков, избегающих командной строки.</p>
  </section>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>