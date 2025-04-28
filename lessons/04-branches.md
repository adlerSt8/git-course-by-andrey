---
layout: default
title: Работа с ветками
permalink: /lessons/04-branches/
nav_order: 4
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
  <h1 style="font-size:3rem;">🌳 Работа с ветками</h1>
  <p style="color:#333; font-size:1.5rem;">Создаём, переключаемся, сливаем и удаляем ветки в Git</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-question-circle step-icon"></i> Что такое ветка?</h2>
  <p>Ветка в Git — это указатель на определённый коммит, позволяющий работать над отдельными частями проекта, не затрагивая основную ветку (<code>main</code>). Ветки используются для разработки новых функций, исправления багов или экспериментов.</p>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Простыми словами:</strong> Это как отдельная рабочая область, где вы можете экспериментировать, не боясь сломать основной проект.</p>
  </div>
  
  <h3>Зачем нужны ветки?</h3>
  <ul>
    <li><i class="fas fa-code-branch"></i> <strong>Изоляция изменений:</strong> Работа над разными задачами параллельно</li>
    <li><i class="fas fa-shield-alt"></i> <strong>Безопасность:</strong> Основной код остаётся стабильным</li>
    <li><i class="fas fa-users"></i> <strong>Командная работа:</strong> Каждый разработчик может работать независимо</li>
  </ul>
  
  <h3>Как это работает в Java-проектах?</h3>
  <p>Представьте, вы работаете над Spring Boot приложением:</p>
  <ol>
    <li>Создаете ветку: <code>feature-user-auth</code></li>
    <li>Добавляете новый REST-контроллер</li>
    <li>Тестируете изменения</li>
    <li>Сливаете с основной веткой</li>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> В профессиональной разработке работа напрямую в <code>main</code> ветке считается плохой практикой!</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-plus-circle step-icon"></i> Создание и переключение веток</h2>
  
  <h3>Пошаговая инструкция</h3>
  <ol>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong></li>
    <pre><kbd>git checkout -b feature-user-login</kbd></pre>
    <p>Эта команда создаст новую ветку и сразу переключит вас на неё.</p>
    
    <li><i class="fas fa-check-circle step-icon"></i> <strong>Проверьте текущую ветку:</strong></li>
    <pre><kbd>git branch</kbd></pre>
    <p>Звёздочка (*) покажет активную ветку.</p>
    
    <li><i class="fas fa-exchange-alt step-icon"></i> <strong>Переключение между ветками:</strong></li>
    <pre><kbd>git checkout main</kbd> <span style="color:#666;"># Вернуться в main</span></pre>
    <pre><kbd>git switch feature-user-login</kbd> <span style="color:#666;"># Современный вариант (Git 2.23+)</span></pre>
  </ol>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> Используйте понятные имена веток:</p>
    <pre><code>feature/[краткое-описание]  # Для новой функциональности
bugfix/[описание-бага]    # Для исправлений
hotfix/[срочное-исправление] # Для критичных исправлений</code></pre>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-code-merge step-icon"></i> Слияние веток</h2>
  
  <h3>Как объединить изменения</h3>
  <ol>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Переключитесь на основную ветку:</strong></li>
    <pre><kbd>git checkout main</kbd></pre>
    
    <li><i class="fas fa-sync-alt step-icon"></i> <strong>Получите свежие изменения:</strong></li>
    <pre><kbd>git pull origin main</kbd></pre>
    
    <li><i class="fas fa-merge step-icon"></i> <strong>Выполните слияние:</strong></li>
    <pre><kbd>git merge feature-user-login</kbd></pre>
    
    <li><i class="fas fa-cloud-upload-alt step-icon"></i> <strong>Отправьте изменения:</strong></li>
    <pre><kbd>git push origin main</kbd></pre>
  </ol>
  
  <h3>Типы слияния</h3>
  <ul>
    <li><strong>Fast-forward:</strong> Когда нет расхождений в истории</li>
    <li><strong>Recursive:</strong> Когда нужно объединить две линии разработки</li>
    <li><strong>Rebase:</strong> Альтернатива merge для чистой истории</li>
  </ul>
  
  <div style="background:#f8f9fa; border:1px solid #ddd; border-radius:6px; padding:1rem; margin:1.5rem 0;">
    <h4 style="margin-top:0;">Чеклист перед слиянием:</h4>
    <ul>
      <li><input type="checkbox"> Все тесты проходят</li>
      <li><input type="checkbox"> Нет конфликтов</li>
      <li><input type="checkbox"> Код проверен (code review)</li>
    </ul>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-trash-alt step-icon"></i> Удаление веток</h2>
  
  <h3>Когда и как удалять ветки</h3>
  <p>После успешного слияния ненужные ветки можно удалить:</p>
  
  <pre><kbd>git branch -d feature-user-login</kbd> <span style="color:#666;"># Локальное удаление</span></pre>
  <pre><kbd>git push origin --delete feature-user-login</kbd> <span style="color:#666;"># Удаление на сервере</span></pre>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> Убедитесь, что все изменения из ветки перенесены в основную ветку перед удалением!</p>
  </div>
  
  <h2 style="font-size:2rem;"><i class="fas fa-exclamation-triangle step-icon"></i> Частые ошибки</h2>
  
  <ul>
    <li><i class="fas fa-times-circle"></i> <strong>Работа не в той ветке:</strong> Всегда проверяйте текущую ветку перед коммитом</li>
    <li><i class="fas fa-exclamation"></i> <strong>Неразрешённые конфликты:</strong> Решайте конфликты перед слиянием</li>
    <li><i class="fas fa-history"></i> <strong>Долгоживущие ветки:</strong> Старайтесь делать ветки короткоживущими</li>
  </ul>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://git-scm.com/book/en/v2/Git-Branching-Branches-in-a-Nutshell" class="btn" style="font-size:1.2rem;">Документация Git по веткам</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/03-commits/' | relative_url }}" class="nav-button">← Работа с коммитами</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/05-pull-requests/' | relative_url }}" class="nav-button">Пул-реквесты →</a>
</nav>