---
layout: default
title: Введение в GitHub
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
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">📘 Введение в GitHub</h1>
  <p style="color:#333; font-size:1.5rem;">Платформа для совместной разработки и управления версиями</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-rocket step-icon"></i> Что такое GitHub?</h2>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Простыми словами:</strong> GitHub — это социальная сеть для разработчиков, где можно хранить код, сотрудничать над проектами и отслеживать изменения.</p>
  </div>
  
  <p>GitHub — это облачная платформа для хостинга IT-проектов и совместной работы, использующая систему контроля версий Git. Это крупнейший в мире сервис для хранения исходного кода с более чем 100 миллионами пользователей.</p>
  
  <h3>Ключевые возможности:</h3>
  <ul>
    <li><i class="fas fa-code-branch"></i> Хранение кода с историей изменений</li>
    <li><i class="fas fa-users"></i> Инструменты для командной работы</li>
    <li><i class="fas fa-cogs"></i> Автоматизация процессов разработки</li>
    <li><i class="fas fa-book"></i> Возможность вести документацию</li>
  </ul>

  <h2 style="font-size:2rem;"><i class="fas fa-history step-icon"></i> История создания</h2>
  
  <div style="display:flex; align-items:center; margin:1.5rem 0;">
    <div style="flex:1; padding-right:2rem;">
      <p>GitHub был основан в 2008 году Томом Престоном-Уэрнером, Крисом Ванстратом и PJ Хайеттом. Платформа начиналась как стартап в Сан-Франциско и быстро завоевала популярность среди разработчиков.</p>
      
      <p>В 2018 году Microsoft приобрела GitHub за $7.5 миллиардов, что позволило значительно расширить функциональность платформы.</p>
    </div>
    <div style="flex:1;">
      <img src="https://github.githubassets.com/images/modules/site/social-cards/github-social.png" alt="GitHub Timeline" style="max-width:100%; border-radius:8px;">
    </div>
  </div>

  <h3>Основные вехи развития:</h3>
  <ul>
    <li><strong>2008:</strong> Официальный запуск платформы</li>
    <li><strong>2010:</strong> Введение Pull Requests</li>
    <li><strong>2016:</strong> Запуск GitHub Marketplace</li>
    <li><strong>2018:</strong> Приобретение Microsoft</li>
    <li><strong>2020:</strong> Запуск Codespaces</li>
  </ul>

  <h2 style="font-size:2rem;"><i class="fas fa-question-circle step-icon"></i> Зачем использовать GitHub?</h2>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Факт:</strong> Более 90% компаний из Fortune 100 используют GitHub для разработки своих продуктов.</p>
  </div>
  
  <h3>Преимущества для разработчиков:</h3>
  
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin: 1.5rem 0;">
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-shield-alt" style="color:#28a745;"></i> Безопасность</h4>
      <p>Резервное копирование кода и возможность отката к любой версии проекта</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-users-cog" style="color:#007bff;"></i> Коллаборация</h4>
      <p>Инструменты для совместной работы над кодом с коллегами по всему миру</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-robot" style="color:#6f42c1;"></i> Автоматизация</h4>
      <p>Возможности CI/CD для автоматического тестирования и развертывания</p>
    </div>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-coffee step-icon"></i> GitHub для Java-разработчиков</h2>
  
  <p>Для Java-сообщества GitHub особенно важен, так как здесь размещены:</p>
  
  <ul>
    <li>Исходные коды популярных фреймворков (Spring, Hibernate)</li>
    <li>Библиотеки с открытым исходным кодом</li>
    <li>Образцы кода и учебные материалы</li>
    <li>Шаблоны проектов (Maven, Gradle)</li>
  </ul>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> GitHub — отличное место для создания портфолио Java-разработчика. Работодатели часто оценивают активность кандидатов на платформе.</p>
  </div>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/' | relative_url }}" class="nav-button">← Оглавление</a>
  <a href="{{ '/lessons/02-signup/' | relative_url }}" class="nav-button">Регистрация на GitHub →</a>
</nav>