---
layout: default
title: Пул-реквесты и совместная работа
permalink: /lessons/05-pull-requests/
nav_order: 5
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
  
  /* Дополнительные стили для визуализации */
  .visualization {
    display: flex;
    justify-content: space-between;
    margin: 2rem 0;
  }
  .visualization > div {
    width: 48%;
    background: #f0f0f0;
    padding: 1rem;
    border-radius: 6px;
  }
  .pros-cons {
    display: flex;
    justify-content: space-between;
    margin: 1rem 0;
  }
  .pros {
    width: 48%;
    background: #e8f5e9;
    padding: 1rem;
    border-radius: 6px;
  }
  .cons {
    width: 48%;
    background: #ffebee;
    padding: 1rem;
    border-radius: 6px;
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">🤝 Пул-реквесты и совместная работа 2</h1>
  <p style="color:#333; font-size:1.5rem;">Учимся работать в команде через GitHub</p>
</div>

<div class="container">
  <!-- Предыдущие разделы остаются без изменений -->
  <!-- ... -->

  <h2 style="font-size:2rem;"><i class="fas fa-code-branch step-icon"></i> Rebase and merge</h2>
  
  <h3>Что происходит:</h3>
  <ol>
    <li><strong>Перемещение коммитов:</strong> Ваши коммиты "пересаживаются" на вершину основной ветки (main/master)</li>
    <li><strong>Линейная история:</strong> Создается прямая линия коммитов без merge-коммитов</li>
    <li><strong>Переписывание истории:</strong> Хэши коммитов изменяются (так как они теперь основаны на другом родителе)</li>
  </ol>

  <div class="visualization">
    <div>
      <h4>До rebase:</h4>
      <pre>        main:    A---B---C
                      \
        feature:       D---E</pre>
    </div>
    <div>
      <h4>После rebase and merge:</h4>
      <pre>        main:    A---B---C---D'---E'</pre>
    </div>
  </div>

  <h3>Как это выглядит в GitHub:</h3>
  <ol>
    <li>После нажатия "Rebase and merge" в интерфейсе PR:
      <ul>
        <li>GitHub выполняет <code>git rebase main</code> для вашей ветки</li>
        <li>Затем делает fast-forward merge в основную ветку</li>
      </ul>
    </li>
    <li>В истории коммитов:
      <ul>
        <li>Нет merge-коммита (в отличие от обычного merge)</li>
        <li>Ваши коммиты отображаются как продолжение основной ветки</li>
      </ul>
    </li>
  </ol>

  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <h4 style="margin-top:0;"><i class="fas fa-desktop"></i> Визуализация в GitHub UI:</h4>
    <p>1. В списке коммитов PR вы увидите пометку <span style="background:#e1f5fe; padding:2px 6px; border-radius:4px;">Rebased</span></p>
    <p>2. График истории будет показывать линейную цепочку без ответвлений</p>
    <p>3. Хэши коммитов изменятся (появится суффикс <code>'</code> в схемах)</p>
  </div>

  <h3>Когда использовать:</h3>
  <div class="pros-cons">
    <div class="pros">
      <h4><i class="fas fa-check-circle"></i> Хорошо для:</h4>
      <ul>
        <li>Небольших фич с 1-3 коммитами</li>
        <li>Когда нужна чистая линейная история</li>
        <li>Личных проектов с одним разработчиком</li>
      </ul>
    </div>
    <div class="cons">
      <h4><i class="fas fa-exclamation-triangle"></i> Избегайте:</h4>
      <ul>
        <li>Уже опубликованных в общий репозиторий веток</li>
        <li>Когда несколько человек работают в ветке</li>
        <li>Для сложных фич с десятками коммитов</li>
      </ul>
    </div>
  </div>

  <h3>Как сделать вручную через терминал:</h3>
  <pre><code># Переключиться на вашу ветку
git checkout feature-branch

# Сделать rebase на текущий main
git rebase main

# Разрешить возможные конфликты (если будут)
git add .
git rebase --continue

# Переключиться на main и сделать merge
git checkout main
git merge feature-branch</code></pre>

  <div style="background:#fff3e0; border-left:4px solid #fb8c00; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong><i class="fas fa-exclamation-triangle"></i> Важно:</strong> Не используйте rebase для веток, которые уже были отправлены в общий репозиторий, если другие разработчики с ними работают!</p>
  </div>

  <!-- Таблица сравнения методов слияния -->
  <h3>Сравнение методов слияния:</h3>
  <table style="width:100%; border-collapse:collapse; margin:1.5rem 0;">
    <thead>
      <tr style="background:#007bff; color:white;">
        <th style="padding:12px; text-align:left;">Feature</th>
        <th style="padding:12px; text-align:left;">Merge commit</th>
        <th style="padding:12px; text-align:left;">Squash and merge</th>
        <th style="padding:12px; text-align:left;">Rebase and merge</th>
      </tr>
    </thead>
    <tbody>
      <tr style="border-bottom:1px solid #ddd;">
        <td style="padding:12px;"><strong>История</strong></td>
        <td style="padding:12px;">С ответвлениями</td>
        <td style="padding:12px;">Один коммит</td>
        <td style="padding:12px;">Абсолютно линейная</td>
      </tr>
      <tr style="border-bottom:1px solid #ddd;">
        <td style="padding:12px;"><strong>Хэши коммитов</strong></td>
        <td style="padding:12px;">Сохраняются</td>
        <td style="padding:12px;">Новый хэш</td>
        <td style="padding:12px;">Изменяются</td>
      </tr>
      <tr style="border-bottom:1px solid #ddd;">
        <td style="padding:12px;"><strong>Подходит для</strong></td>
        <td style="padding:12px;">Больших фич</td>
        <td style="padding:12px;">Мелких правок</td>
        <td style="padding:12px;">Небольших фич</td>
      </tr>
      <tr>
        <td style="padding:12px;"><strong>Merge-коммит</strong></td>
        <td style="padding:12px;">Создается</td>
        <td style="padding:12px;">Создается</td>
        <td style="padding:12px;">Не создается</td>
      </tr>
    </tbody>
  </table>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://github.com/features" class="btn" style="font-size:1.2rem;">Узнать больше на GitHub</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/04-branching/' | relative_url }}" class="nav-button">← Работа с ветками</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/06-team-project/' | relative_url }}" class="nav-button">Командный проект →</a>
</nav>