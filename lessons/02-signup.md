---
layout: default
title: Регистрация и настройка
permalink: /lessons/02-signup/
nav_order: 2
---

<style>
  /* Основной стиль для блока с кодом */
  pre {
    background: #e9ecef;
    padding: 1rem;
    border: 1px solid #ddd;
    border-radius: 6px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1.2rem;
    overflow-x: auto;
    margin: 1.5rem 0;
  }
  
  /* Стиль для тега <code> */
  code {
    background: #e9ecef;
    padding: 0.3rem 0.5rem;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1.2rem;
  }
  
  /* Стиль для клавиш */
  kbd {
    background: #f1f1f1;
    padding: 0.3rem 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1.2rem;
    box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  }
  
  /* Иконки шагов */
  .step-icon {
    margin-right: 0.5rem;
    font-size: 1.5rem;
  }
  
  /* Стиль контейнера для текста */
  .container {
    background: #f8f9fa;
    border-radius: 8px;
    padding: 2.5rem;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    margin: 2rem 0;
    line-height: 1.8;
    font-size: 1.4rem;
    color: #333;
    max-width: 2000px;
    width: 95%;   
  }
  
  /* Стили для навигации */
  .nav-button {
    text-decoration: none;
    color: #fff;
    background: #007bff;
    padding: 0.8rem 1.5rem;
    border-radius: 8px;
    font-size: 1.4rem;
    transition: background 0.2s;
  }
  
  .nav-button:hover {
    background: #0056b3;
  }
  
  /* Кнопка */
  .btn {
    display: inline-block;
    background-color: #0056b3;
    color: #fff;
    padding: 0.6rem 1.2rem;
    border-radius: 4px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.2s;
  }
  
  .btn:hover {
    background-color: #003d7a;
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">🔐 Регистрация и настройка Git</h1>
  <p style="color:#333; font-size:1.5rem;">Пошаговая инструкция для начала работы с системой контроля версий</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-user-plus step-icon"></i> 1. Создание аккаунта на GitHub</h2>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Зачем это нужно?</strong> Аккаунт на GitHub — это ваша профессиональная визитка в мире разработки. Он позволяет хранить код, участвовать в open-source проектах и показывать свои работы потенциальным работодателям.</p>
  </div>
  
  <h3>Как зарегистрироваться:</h3>
  <ol>
    <li><i class="fas fa-mouse-pointer step-icon"></i> Перейдите на <a href="https://github.com" class="btn">GitHub.com</a></li>
    <li><i class="fas fa-keyboard step-icon"></i> Введите email, придумайте имя пользователя и пароль</li>
    <li><i class="fas fa-check-circle step-icon"></i> Выберите бесплатный тариф (Free)</li>
    <li><i class="fas fa-envelope step-icon"></i> Подтвердите email (проверьте почту)</li>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> Используйте профессиональное имя пользователя — оно станет частью ссылок на ваши проекты (например, github.com/ваше-имя).</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-download step-icon"></i> 2. Установка Git на компьютер</h2>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Зачем это нужно?</strong> Git — это инструмент, который будет отслеживать все изменения в ваших файлах и синхронизировать их с GitHub. Без него невозможно работать с репозиториями локально.</p>
  </div>
  
  <h3>Инструкция по установке:</h3>
  
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin: 1.5rem 0;">
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-windows" style="color:#0078d7;"></i> Windows</h4>
      <ol>
        <li>Скачайте установщик с <a href="https://git-scm.com/download/win">официального сайта</a></li>
        <li>Запустите .exe файл</li>
        <li>Оставьте все настройки по умолчанию</li>
      </ol>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-apple" style="color:#a2aaad;"></i> MacOS</h4>
      <ol>
        <li>Откройте Терминал</li>
        <li>Введите команду:</li>
        <pre><code>brew install git</code></pre>
        <li>Если Homebrew не установлен, следуйте <a href="https://brew.sh">инструкциям</a></li>
      </ol>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-linux" style="color:#fcc624;"></i> Linux</h4>
      <ol>
        <li>Откройте терминал</li>
        <li>Для Ubuntu/Debian:</li>
        <pre><code>sudo apt install git</code></pre>
        <li>Для Fedora:</li>
        <pre><code>sudo dnf install git</code></pre>
      </ol>
    </div>
  </div>

  <h3>Проверка установки:</h3>
  <pre><code>git --version</code></pre>
  <p>Должна появиться информация о версии, например: <code>git version 2.39.2</code></p>

  <h2 style="font-size:2rem;"><i class="fas fa-cog step-icon"></i> 3. Настройка Git</h2>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Зачем это нужно?</strong> Эти настройки будут добавляться к каждому вашему коммиту, чтобы другие участники проекта знали, кто внёс изменения.</p>
  </div>
  
  <h3>Основные команды:</h3>
  <ol>
    <li><i class="fas fa-user step-icon"></i> Укажите своё имя:</li>
    <pre><code>git config --global user.name "Ваше Имя"</code></pre>
    
    <li><i class="fas fa-envelope step-icon"></i> Укажите email (должен совпадать с GitHub):</li>
    <pre><code>git config --global user.email "ваш@email.com"</code></pre>
    
    <li><i class="fas fa-check step-icon"></i> Проверьте настройки:</li>
    <pre><code>git config --list</code></pre>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> Эти данные будут видны в истории изменений всех ваших проектов. Используйте реальное имя и рабочий email.</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-key step-icon"></i> 4. Настройка SSH-ключа</h2>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Зачем это нужно?</strong> SSH-ключи позволяют безопасно подключаться к GitHub без ввода логина и пароля каждый раз. Это как электронный пропуск в ваш аккаунт.</p>
  </div>
  
  <h3>Как создать и добавить ключ:</h3>
  <ol>
    <li><i class="fas fa-terminal step-icon"></i> Сгенерируйте новый SSH-ключ:</li>
    <pre><code>ssh-keygen -t ed25519 -C "ваш@email.com"</code></pre>
    <p>Нажимайте Enter, чтобы принять значения по умолчанию.</p>
    
    <li><i class="fas fa-eye step-icon"></i> Просмотрите и скопируйте ключ:</li>
    <pre><code>cat ~/.ssh/id_ed25519.pub</code></pre>
    
    <li><i class="fas fa-cloud-upload-alt step-icon"></i> Добавьте ключ в GitHub:</li>
    <ol type="a">
      <li>Зайдите в <a href="https://github.com/settings/keys">настройки SSH-ключей</a></li>
      <li>Нажмите "New SSH key"</li>
      <li>Вставьте скопированный ключ и сохраните</li>
    </ol>
    
    <li><i class="fas fa-plug step-icon"></i> Проверьте подключение:</li>
    <pre><code>ssh -T git@github.com</code></pre>
    <p>Должно появиться сообщение с вашим именем на GitHub.</p>
  </ol>
  
  <div style="background:#f8f9fa; border:1px solid #ddd; border-radius:6px; padding:1rem; margin:1.5rem 0;">
    <h4 style="margin-top:0;">Проверка всех настроек:</h4>
    <ul>
      <li><input type="checkbox"> Аккаунт на GitHub создан</li>
      <li><input type="checkbox"> Git установлен (<code>git --version</code>)</li>
      <li><input type="checkbox"> Настроены имя и email</li>
      <li><input type="checkbox"> SSH-ключ добавлен в GitHub</li>
    </ul>
  </div>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/01-intro/' | relative_url }}" class="nav-button">← Введение в Git</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/03-create-repo/' | relative_url }}" class="nav-button">Создание репозитория →</a>
</nav>