---
layout: default
title: Вопросы и итоги
permalink: /lessons/07-faq/
nav_order: 7
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
    max-width: 2500px;
    width: 99%;   
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
  <h1 style="font-size:3rem;">❓ Вопросы и итоги</h1>
  <p style="color:#333; font-size:1.5rem;">Закрепляем знания и разбираем тонкости работы с Git и GitHub</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-question-circle step-icon"></i> Частые вопросы</h2>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Профессиональный совет:</strong> Эти вопросы задают 90% новичков в первые месяцы работы с Git</p>
  </div>

  <h3>1. Как правильно создать Java-файл в репозитории?</h3>
  <p><strong>Решение:</strong></p>
  <ol>
    <li>В веб-интерфейсе нажмите <kbd>Add file</kbd> → <kbd>Create new file</kbd></li>
    <li>Введите имя с расширением <code>.java</code> (например, <code>Main.java</code>)</li>
    <li>Добавьте код класса:</li>
    <pre><code>public class Main {
  public static void main(String[] args) {
    System.out.println("Hello GitHub!");
  }
}</code></pre>
    <li>Внизу страницы заполните поля коммита и нажмите <kbd>Commit new file</kbd></li>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> Имя файла должно точно соответствовать имени класса (с учётом регистра)!</p>
  </div>

  <h3>2. Как исправить конфликт в пул-реквесте?</h3>
  <p><strong>Пошаговое решение:</strong></p>
  <ol>
    <li>Перейдите на вкладку <kbd>Pull requests</kbd></li>
    <li>Откройте проблемный PR и нажмите <kbd>Resolve conflicts</kbd></li>
    <li>В редакторе вы увидите маркеры конфликтов:</li>
    <pre><code><<<<<< HEAD
Ваши изменения
=======
Изменения из основной ветки
>>>>>>> main</code></pre>
    <li>Удалите маркеры и оставьте нужный код</li>
    <li>Нажмите <kbd>Mark as resolved</kbd> и <kbd>Commit merge</kbd></li>
  </ol>

  <h3>3. Как восстановить удалённую ветку?</h3>
  <p><strong>Способ 1:</strong> Через веб-интерфейс</p>
  <ol>
    <li>Перейдите в <kbd>Branches</kbd> → <kbd>View all branches</kbd></li>
    <li>В разделе <kbd>Recently deleted branches</kbd> найдите нужную</li>
    <li>Нажмите <kbd>Restore</kbd></li>
  </ol>

  <p><strong>Способ 2:</strong> Через командную строку</p>
  <pre><code>git checkout -b feature-x origin/feature-x</code></pre>

  <h2 style="font-size:2rem;"><i class="fas fa-lightbulb step-icon"></i> Полезные тонкости</h2>
  
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 1.5rem; margin: 1.5rem 0;">
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-history" style="color:#6f42c1;"></i> Отмена последнего коммита</h4>
      <pre><code>git reset --soft HEAD~1</code></pre>
      <p>Сохраняет изменения в рабочей директории</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-search" style="color:#28a745;"></i> Поиск в истории</h4>
      <pre><code>git log -p -S"someMethod"</code></pre>
      <p>Находит коммиты, где изменялся указанный метод</p>
    </div>
    <div style="background:#fff; border-radius:8px; padding:1.5rem; box-shadow:0 2px 8px rgba(0,0,0,0.1);">
      <h4 style="margin-top:0;"><i class="fas fa-broom" style="color:#007bff;"></i> Очистка веток</h4>
      <pre><code>git fetch --prune</code></pre>
      <p>Удаляет ссылки на удалённые ветки</p>
    </div>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-book step-icon"></i> Ключевые термины</h2>
  
  <table style="width:100%; border-collapse:collapse; margin:1.5rem 0;">
    <tr style="background:#e9ecef;">
      <th style="padding:0.8rem; text-align:left;">Термин</th>
      <th style="padding:0.8rem; text-align:left;">Значение</th>
      <th style="padding:0.8rem; text-align:left;">Пример</th>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><strong>Репозиторий</strong></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Хранилище проекта с историей изменений</td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>github.com/user/java-project</code></td>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><strong>Коммит</strong></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Фиксация изменений с комментарием</td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>git commit -m "Add Main class"</code></td>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><strong>Ветка</strong></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Изолированная линия разработки</td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>git checkout -b feature-login</code></td>
    </tr>
    <tr>
      <td style="padding:0.8rem;"><strong>Пул-реквест</strong></td>
      <td style="padding:0.8rem;">Запрос на слияние изменений</td>
      <td style="padding:0.8rem;">Обсуждение кода перед мержем в <code>main</code></td>
    </tr>
  </table>

  <h2 style="font-size:2rem;"><i class="fas fa-rocket step-icon"></i> Дальнейшие шаги</h2>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Рекомендация:</strong> Практикуйтесь ежедневно - сделайте хотя бы один коммит в день!</p>
  </div>
  
  <h3>Что изучить дальше:</h3>
  <ul>
    <li><i class="fas fa-book"></i> <a href="https://git-scm.com/book" class="btn">Официальная документация Git</a></li>
    <li><i class="fas fa-code-branch"></i> GitHub Actions для CI/CD</li>
    <li><i class="fas fa-shield-alt"></i> Настройка .gitignore для Java-проектов</li>
    <li><i class="fas fa-users"></i> Участие в open-source проектах</li>
  </ul>

  <h3>Практическое задание:</h3>
  <ol>
    <li>Создайте репозиторий с примером Java-приложения</li>
    <li>Добавьте файлы <code>Main.java</code> и <code>Calculator.java</code></li>
    <li>Настройте GitHub Actions для сборки с Maven</li>
    <li>Сделайте пул-реквест с улучшениями</li>
  </ol>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/06-team-project/' | relative_url }}" class="nav-button">← Командный проект</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/resources/' | relative_url }}" class="nav-button">Дополнительные материалы →</a>
</nav>