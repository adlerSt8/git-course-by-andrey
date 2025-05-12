layout: default
title: Система контроля версий Git
permalink: /lessons/01-git-intro/
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
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">📜 История Git и системы контроля версий</h1>
  <p style="color:#333; font-size:1.5rem;">Как появился и развивался самый популярный инструмент управления кодом</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-history step-icon"></i> Истоки контроля версий</h2>

  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Интересный факт:</strong> Первые системы контроля версий появились еще в 1970-х годах, задолго до Git!</p>
  </div>

  <p>Концепция контроля версий возникла из необходимости:</p>
  <ul>
    <li>Отслеживать изменения в коде</li>
    <li>Работать над проектом в команде</li>
    <li>Возвращаться к предыдущим версиям при ошибках</li>
    <li>Параллельно разрабатывать разные функции</li>
  </ul>

  <h3>До Git существовали:</h3>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 1.5rem; margin: 1.5rem 0;">
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-archive" style="color:#6f42c1;"></i> SCCS (1972)</h4>
      <p>Первая система контроля версий от AT&T Bell Labs</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-copy" style="color:#28a745;"></i> RCS (1982)</h4>
      <p>Работала с отдельными файлами, а не проектами</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-network-wired" style="color:#007bff;"></i> CVS (1990)</h4>
      <p>Первая сетевая система, популярная в 1990-х</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-server" style="color:#fd7e14;"></i> SVN (2000)</h4>
      <p>Централизованная система, главный конкурент Git</p>
    </div>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-birthday-cake step-icon"></i> Рождение Git</h2>

  <div class="timeline">
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">2005</div>
      <div class="timeline-content">
        <p><strong>Линус Торвальдс</strong>, создатель Linux, начинает разработку Git из-за проблем с проприетарной системой BitKeeper</p>
      </div>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">7 апреля 2005</div>
      <div class="timeline-content">
        <p>Первая публичная версия Git. Основные принципы:</p>
        <ul>
          <li>Распределенная архитектура</li>
          <li>Высокая скорость работы</li>
          <li>Надежность и целостность данных</li>
          <li>Поддержка нелинейной разработки</li>
        </ul>
      </div>
    </div>
    <div class="timeline-item">
      <div class="timeline-dot"></div>
      <div class="timeline-date">2005-2007</div>
      <div class="timeline-content">
        <p>Git становится стандартом для разработки ядра Linux. Основные преимущества:</p>
        <ul>
          <li>Каждый разработчик имеет полную историю проекта</li>
          <li>Возможность работы оффлайн</li>
          <li>Мгновенное создание веток</li>
        </ul>
      </div>
    </div>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-cogs step-icon"></i> Как работает Git?</h2>

  <div style="display:flex; align-items:center; margin:1.5rem 0;">
    <div style="flex:1; padding-right:2rem;">
      <p>Git кардинально отличается от предыдущих систем контроля версий своей <strong>распределенной архитектурой</strong>:</p>
      <ul>
        <li>Нет центрального сервера - каждый репозиторий полный</li>
        <li>Все операции (кроме push/pull) выполняются локально</li>
        <li>Используется хеширование SHA-1 для идентификации объектов</li>
        <li>Три основных состояния файлов: modified, staged, committed</li>
      </ul>
    </div>
    <div style="flex:1;">
      <img src="https://git-scm.com/book/en/v2/images/areas.png" alt="Git workflow" style="max-width:100%; border-radius:8px;">
    </div>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-chart-line step-icon"></i> Эволюция Git</h2>

  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Сегодня Git</strong> используется 90% разработчиков и стал стандартом де-факто в индустрии</p>
  </div>

  <h3>Ключевые этапы развития:</h3>
  <ul>
    <li><strong>2008:</strong> Появление GitHub - социальной платформы для Git</li>
    <li><strong>2010:</strong> Git становится стандартом в open-source сообществе</li>
    <li><strong>2014:</strong> Microsoft переносит .NET на GitHub</li>
    <li><strong>2018:</strong> Git интегрируется во все основные IDE</li>
    <li><strong>2020:</strong> GitHub насчитывает 100 млн репозиториев</li>
  </ul>

  <h2 style="font-size:2rem;"><i class="fab fa-github step-icon"></i> GitHub и другие платформы</h2>

  <p>Хотя Git можно использовать самостоятельно, платформы хостинга делают совместную работу удобнее:</p>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin: 1.5rem 0;">
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-github" style="color:#24292e;"></i> GitHub</h4>
      <p>Крупнейшая платформа, приобретенная Microsoft в 2018</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-gitlab" style="color:#fc6d26;"></i> GitLab</h4>
      <p>Альтернатива с мощными CI/CD возможностями</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fab fa-bitbucket" style="color:#0052cc;"></i> Bitbucket</h4>
      <p>Решение от Atlassian с интеграцией Jira</p>
    </div>
  </div>

  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> Git ≠ GitHub. Git - это инструмент, а GitHub - сервис для хостинга Git-репозиториев с дополнительными функциями.</p>
  </div>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/' | relative_url }}" class="nav-button">← Оглавление</a>
  <a href="{{ '/lessons/02-git-basics/' | relative_url }}" class="nav-button">Основы Git →</a>