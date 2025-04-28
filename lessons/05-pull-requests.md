---
layout: default
title: Пул-реквесты и совместная работа
permalink: /lessons/05-pull-requests/
nav_order: 5
---

<style>
  /* Основные стили */
  .lesson-container {
    max-width: 1200px;
    margin: 2rem auto;
    background: #f8f9fa;
    border-radius: 12px;
    padding: 3rem;
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    line-height: 1.8;
    font-size: 1.4rem;
    color: #333;
  }

  /* Заголовки */
  .lesson-title {
    font-size: 3rem;
    text-align: center;
    margin-bottom: 1rem;
    color: #2c3e50;
  }
  
  .lesson-subtitle {
    font-size: 1.5rem;
    text-align: center;
    color: #555;
    margin-bottom: 3rem;
  }
  
  .section-title {
    font-size: 2.2rem;
    margin: 2.5rem 0 1.5rem;
    color: #2c3e50;
    border-bottom: 2px solid #e9ecef;
    padding-bottom: 0.5rem;
  }
  
  .subsection-title {
    font-size: 1.8rem;
    margin: 2rem 0 1rem;
    color: #34495e;
  }

  /* Блоки кода */
  pre {
    background: #2d3748;
    padding: 1.5rem;
    border-radius: 8px;
    font-family: 'Fira Code', 'Courier New', monospace;
    font-size: 1.2rem;
    overflow-x: auto;
    margin: 1.5rem 0;
    color: #f8f9fa;
    border-left: 4px solid #4299e1;
  }
  
  code {
    background: #edf2f7;
    padding: 0.3rem 0.5rem;
    border-radius: 4px;
    font-family: 'Fira Code', 'Courier New', monospace;
    font-size: 1.2rem;
    color: #2d3748;
  }
  
  kbd {
    background: #f7fafc;
    padding: 0.3rem 0.5rem;
    border: 1px solid #cbd5e0;
    border-radius: 4px;
    font-family: 'Fira Code', 'Courier New', monospace;
    font-size: 1.2rem;
    box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  }

  /* Иконки */
  .step-icon {
    margin-right: 0.8rem;
    font-size: 1.6rem;
    color: #4299e1;
  }
  
  /* Специальные блоки */
  .tip-box {
    background: #ebf8ff;
    border-left: 4px solid #4299e1;
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 8px 8px 0;
  }
  
  .warning-box {
    background: #fffaf0;
    border-left: 4px solid #dd6b20;
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 8px 8px 0;
  }
  
  .success-box {
    background: #f0fff4;
    border-left: 4px solid #48bb78;
    padding: 1.5rem;
    margin: 2rem 0;
    border-radius: 0 8px 8px 0;
  }

  /* Визуализация Git */
  .git-visualization {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    margin: 2.5rem 0;
    background: #f7fafc;
    padding: 2rem;
    border-radius: 8px;
    border: 1px solid #e2e8f0;
  }
  
  .git-branch {
    display: flex;
    align-items: center;
  }
  
  .git-commit {
    width: 36px;
    height: 36px;
    border-radius: 50%;
    background: #4299e1;
    color: white;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-right: 15px;
    font-family: monospace;
    font-weight: bold;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .git-line {
    width: 2px;
    height: 25px;
    background: #4299e1;
    margin-left: 17px;
  }

  /* Таблицы */
  .merge-table {
    width: 100%;
    border-collapse: collapse;
    margin: 2rem 0;
    font-size: 1.3rem;
  }
  
  .merge-table th {
    background: #2d3748;
    color: white;
    padding: 12px;
    text-align: left;
  }
  
  .merge-table td {
    padding: 12px;
    border-bottom: 1px solid #e2e8f0;
  }
  
  .merge-table tr:nth-child(even) {
    background: #f7fafc;
  }

  /* Кнопки */
  .btn {
    display: inline-block;
    background-color: #4299e1;
    color: white;
    padding: 0.8rem 1.8rem;
    border-radius: 6px;
    text-decoration: none;
    font-weight: bold;
    font-size: 1.3rem;
    transition: all 0.2s;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .btn:hover {
    background-color: #3182ce;
    transform: translateY(-2px);
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  }

  /* Навигация */
  .lesson-navigation {
    display: flex;
    justify-content: space-between;
    margin: 4rem 0 2rem;
  }
  
  .nav-button {
    text-decoration: none;
    color: white;
    background: #4299e1;
    padding: 1rem 2rem;
    border-radius: 8px;
    font-size: 1.4rem;
    transition: all 0.2s;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }
  
  .nav-button:hover {
    background: #3182ce;
    transform: translateY(-2px);
    box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
<link href="https://fonts.googleapis.com/css2?family=Fira+Code:wght@400;500&display=swap" rel="stylesheet">

<div class="lesson-container">
  <h1 class="lesson-title">🤝 Пул-реквесты и совместная работа</h1>
  <p class="lesson-subtitle">Полное руководство по работе с Pull Requests в команде</p>

  <div class="tip-box">
    <p><strong><i class="fas fa-lightbulb"></i> Простыми словами:</strong> Пул-реквест (PR) — это способ сказать команде: "Я сделал изменения, давайте обсудим их перед добавлением в основной проект".</p>
  </div>

  <h2 class="section-title"><i class="fas fa-question-circle step-icon"></i> Основы Pull Requests</h2>
  
  <h3 class="subsection-title">Зачем нужны пул-реквесты?</h3>
  <ul>
    <li><i class="fas fa-check-circle" style="color: #48bb78;"></i> <strong>Контроль качества:</strong> Код проверяют несколько разработчиков</li>
    <li><i class="fas fa-comments" style="color: #4299e1;"></i> <strong>Обсуждение:</strong> Возможность получить обратную связь</li>
    <li><i class="fas fa-history" style="color: #9f7aea;"></i> <strong>История изменений:</strong> Полная запись всех модификаций</li>
    <li><i class="fas fa-shield-alt" style="color: #ed8936;"></i> <strong>Безопасность:</strong> Предотвращение ошибок перед слиянием</li>
  </ul>
  
  <h3 class="subsection-title">Типичный workflow с PR:</h3>
  <ol>
    <li>Создать ветку для новой фичи/исправления</li>
    <li>Реализовать изменения в коде</li>
    <li>Создать Pull Request на GitHub</li>
    <li>Пройти код-ревью от коллег</li>
    <li>Исправить замечания (если есть)</li>
    <li>Слить изменения после одобрения</li>
  </ol>

  <h2 class="section-title"><i class="fas fa-plus-circle step-icon"></i> Создание Pull Request</h2>
  
  <h3 class="subsection-title">Пошаговая инструкция</h3>
  
  <div class="git-visualization">
    <div class="git-branch">
      <div class="git-commit">A</div>
      <div class="git-commit">B</div>
      <div class="git-commit">C</div>
      <span style="margin-left: 1rem;">main branch</span>
    </div>
    <div class="git-line"></div>
    <div class="git-branch" style="margin-left: 50px;">
      <div class="git-commit">D</div>
      <div class="git-commit">E</div>
      <span style="margin-left: 1rem;">feature branch</span>
    </div>
  </div>

  <pre><code># 1. Создать новую ветку
git checkout -b feature-user-auth

# 2. Внести изменения и сделать коммиты
git add .
git commit -m "Реализована аутентификация"

# 3. Отправить ветку на GitHub
git push origin feature-user-auth</code></pre>

  <div class="success-box">
    <h4><i class="fas fa-check-circle"></i> На GitHub:</h4>
    <ol>
      <li>Перейти в репозиторий → вкладка "Pull requests"</li>
      <li>Нажать "New pull request"</li>
      <li>Выбрать base: main ← compare: feature-user-auth</li>
      <li>Заполнить заголовок и описание</li>
      <li>Нажать "Create pull request"</li>
    </ol>
  </div>

  <h2 class="section-title"><i class="fas fa-code-branch step-icon"></i> Стратегии слияния</h2>
  
  <table class="merge-table">
    <thead>
      <tr>
        <th>Метод</th>
        <th>Команда</th>
        <th>Когда использовать</th>
        <th>История коммитов</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Merge commit</strong></td>
        <td><code>git merge --no-ff</code></td>
        <td>Большие фичи, командная работа</td>
        <td>Сохраняет всю историю</td>
      </tr>
      <tr>
        <td><strong>Squash and merge</strong></td>
        <td><code>git merge --squash</code></td>
        <td>Мелкие правки, багфиксы</td>
        <td>Один коммит</td>
      </tr>
      <tr>
        <td><strong>Rebase and merge</strong></td>
        <td><code>git rebase</code></td>
        <td>Личные ветки, чистые фичи</td>
        <td>Линейная история</td>
      </tr>
    </tbody>
  </table>

  <h3 class="subsection-title">Подробно про Rebase and merge</h3>
  
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 2rem; margin: 2rem 0;">
    <div>
      <h4><i class="fas fa-project-diagram"></i> Как работает:</h4>
      <ol>
        <li>Берет ваши коммиты из feature-ветки</li>
        <li>Применяет их поверх текущего состояния main</li>
        <li>Создает новые коммиты с новыми хэшами</li>
        <li>Делает fast-forward merge</li>
      </ol>
      
      <div class="git-visualization">
        <div class="git-branch">
          <div class="git-commit">A</div>
          <div class="git-commit">B</div>
          <div class="git-commit">C</div>
          <div class="git-commit">D'</div>
          <div class="git-commit">E'</div>
        </div>
      </div>
    </div>
    
    <div>
      <h4><i class="fas fa-desktop"></i> В GitHub:</h4>
      <ul>
        <li>История остается абсолютно линейной</li>
        <li>Нет merge-коммитов</li>
        <li>Коммиты помечены как rebased</li>
        <li>Хэши изменяются (появляется ')</li>
      </ul>
      
      <div class="warning-box">
        <h4><i class="fas fa-exclamation-triangle"></i> Важно!</h4>
        <p>Не используйте rebase для веток, с которыми работают другие разработчики - это перезапишет историю и вызовет проблемы.</p>
      </div>
    </div>
  </div>

  <h3 class="subsection-title">Пошаговый пример Rebase:</h3>
  <pre><code># 1. Переключиться на feature-ветку
git checkout feature-login

# 2. Получить свежие изменения из main
git fetch origin main

# 3. Выполнить rebase
git rebase main

# 4. Разрешить конфликты (если есть)
git add .
git rebase --continue

# 5. Переключиться на main и сделать merge
git checkout main
git merge feature-login

# 6. Отправить изменения
git push origin main</code></pre>

  <div class="tip-box">
    <h4><i class="fas fa-lightbulb"></i> Советы по rebase:</h4>
    <ul>
      <li>Используйте для небольших фич (1-5 коммитов)</li>
      <li>Отлично подходит для личных веток</li>
      <li>Делает историю проекта чище</li>
      <li>Разрешайте конфликты по одному коммиту за раз</li>
    </ul>
  </div>

  <h2 class="section-title"><i class="fas fa-check-double step-icon"></i> Лучшие практики</h2>
  
  <h3 class="subsection-title">Для авторов PR:</h3>
  <ul>
    <li>Делайте небольшие PR (200-300 строк)</li>
    <li>Пишите понятные описания</li>
    <li>Добавляйте скриншоты для UI-изменений</li>
    <li>Включайте тесты для нового кода</li>
  </ul>
  
  <h3 class="subsection-title">Для ревьюверов:</h3>
  <ul>
    <li>Проверяйте код в течение 1-2 дней</li>
    <li>Будьте вежливы в комментариях</li>
    <li>Обращайте внимание на:
      <ul>
        <li>Корректность логики</li>
        <li>Читаемость кода</li>
        <li>Потенциальные уязвимости</li>
        <li>Соответствие стандартам</li>
      </ul>
    </li>
  </ul>

  <div style="text-align: center; margin: 3rem 0;">
    <a href="https://github.com/features" class="btn">
      <i class="fab fa-github"></i> Узнать больше на GitHub
    </a>
  </div>
</div>

<div class="lesson-navigation">
  <a href="{{ '/lessons/04-branching/' | relative_url }}" class="nav-button">
    <i class="fas fa-arrow-left"></i> Работа с ветками
  </a>
  <a href="{{ '/' | relative_url }}" class="nav-button">
    <i class="fas fa-home"></i> Оглавление
  </a>
  <a href="{{ '/lessons/06-team-project/' | relative_url }}" class="nav-button">
    Командный проект <i class="fas fa-arrow-right"></i>
  </a>
</div>