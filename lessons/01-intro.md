---
layout: default
title: Система контроля версий Git
permalink: /lessons/01-intro/
nav_order: 1
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

  /* Стиль для временной шкалы */
  .timeline {
    position: relative;
    padding-left: 3rem;
    margin: 2rem 0;
  }

  .timeline-item {
    position: relative;
    padding-bottom: 2rem;
  }

  .timeline-item:last-child {
    padding-bottom: 0;
  }

  .timeline-dot {
    position: absolute;
    left: -1.7rem;
    width: 1.2rem;
    height: 1.2rem;
    border-radius: 50%;
    background: #007bff;
    top: 0.3rem;
  }

  .timeline-date {
    font-weight: bold;
    color: #007bff;
  }

  .timeline-content {
    padding-left: 1rem;
  }

  /* Сохранены все стили из предыдущей версии */
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">📜 Эволюция Git: от концепции к стандарту. Ред 1</h1>
  <p style="color:#333; font-size:1.5rem;">Как проблемы BitKeeper привели к созданию самой популярной системы контроля версий</p>
</div>

<div class="container">
  <!-- 1. Предшественники Git -->
  <h2 style="font-size:2rem;"><i class="fas fa-history step-icon"></i> Что было до Git?</h2>
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Контекст:</strong> В 2005 году разработчики ядра Linux использовали BitKeeper, но нуждались в свободной альтернативе</p>
  </div>

  <h3>Основные системы контроля версий:</h3>
  <ul>
    <li><strong>Локальные (1970-е):</strong> SCCS, RCS - работали с отдельными файлами</li>
    <li><strong>Централизованные (1990-е):</strong> CVS, SVN - требовали постоянного подключения к серверу</li>
    <li><strong>BitKeeper (2002-2005):</strong> Проприетарная распределённая система, использовавшаяся для Linux</li>
  </ul>

  <!-- 2. Проблемы BitKeeper -->
  <h2 style="font-size:2rem;"><i class="fas fa-exclamation-triangle step-icon"></i> Почему создали Git?</h2>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">2005</div>
      <div class="timeline-content">
        <p><strong>Кризис BitKeeper:</strong></p>
        <ul>
          <li>Компания BitMover отозвала бесплатную лицензию</li>
          <li>Сообщество Linux отказалось от проприетарного решения</li>
          <li>Существующие аналоги (SVN) не поддерживали распределённую разработку</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- 3. Рождение и развитие Git -->
  <h2 style="font-size:2rem;"><i class="fas fa-baby step-icon"></i> Рождение Git</h2>
  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">Апрель 2005</div>
      <div class="timeline-content">
        <p><strong>Линус Торвальдс:</strong> "Мне нужно было:</p>
        <ul>
          <li>Распределённую систему без центрального сервера</li>
          <li>Мгновенное создание веток</li>
          <li>Гарантию целостности данных (SHA-1)"</li>
        </ul>
      </div>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">2005-2010</div>
      <div class="timeline-content">
        <p><strong>Эволюция:</strong></p>
        <ul>
          <li>Первая версия за 2 недели</li>
          <li>Переход с C на POSIX-скрипты</li>
          <li>Интеграция в ядро Linux</li>
        </ul>
      </div>
    </div>
  </div>

  <!-- 4. Как работает Git -->
  <h2 style="font-size:2rem;"><i class="fas fa-cogs step-icon"></i> Три состояния файлов</h2>
  <div style="display:flex; align-items:center; margin:1.5rem 0;">
    <div style="flex:1; padding-right:2rem;">
      <ol>
        <li><strong>Modified</strong> - файл изменён, но не помечен для коммита</li>
        <li><strong>Staged</strong> - изменения подготовлены для фиксации</li>
        <li><strong>Committed</strong> - данные безопасно сохранены в локальной БД</li>
      </ol>
      <pre><code>git add "file" # Переводит в staged
git commit    # Фиксирует изменения</code></pre>
    </div>
    <div style="flex:1;">
      <img src="https://git-scm.com/book/en/v2/images/areas.png" alt="Git workflow" style="max-width:100%; border-radius:8px;">
    </div>
  </div>

  <!-- 5. Эволюция Git -->
  <h2 style="font-size:2rem;"><i class="fas fa-chart-line step-icon"></i> Становление стандартом</h2>
  <ul>
    <li><strong>2008:</strong> GitHub делает Git доступным для масс</li>
    <li><strong>2010:</strong> 75% open-source проектов переходят на Git</li>
    <li><strong>2014:</strong> Git 2.0 с улучшенной производительностью</li>
    <li><strong>2020:</strong> 90% разработчиков используют Git ежедневно</li>
  </ul>

  <!-- 6. Использование без хостингов -->
  <h2 style="font-size:2rem;"><i class="fas fa-server step-icon"></i> Git без хостингов</h2>
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Когда нужно:</strong> Для локальных проектов, приватного кода или когда важна автономность</p>
  </div>

  <h3>Как использовать:</h3>
  <ol>
    <li>Инициализация репозитория:
      <pre><code>git init</code></pre>
    </li>
    <li>Работа с историей:
      <pre><code>git log --oneline</code></pre>
    </li>
    <li>Синхронизация между компьютерами через USB или SSH</li>
  </ol>

  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Преимущества:</strong> Полный контроль, нет ограничений хостингов, работа без интернета</p>
  </div>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/' | relative_url }}" class="nav-button">← Оглавление</a>
  <a href="{{ '/lessons/02-git-basics/' | relative_url }}" class="nav-button">Основные команды →</a>
</nav>