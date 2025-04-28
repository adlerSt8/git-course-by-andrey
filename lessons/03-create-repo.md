---
layout: default
title: Создание репозитория и первые коммиты
permalink: /lessons/03-create-repo/
nav_order: 3
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
  <h1 style="font-size:3rem;">📁 Создание репозитория и первые коммиты</h1>
  <p style="color:#333; font-size:1.5rem;">Настраиваем репозиторий на GitHub и делаем первые изменения</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-globe step-icon"></i> Создание репозитория на GitHub</h2>
  <p>Репозиторий на GitHub — это место, где хранится ваш код, история изменений и файлы проекта. Создание репозитория — первый шаг к публикации и управлению вашим Java-проектом.</p>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Простыми словами:</strong> Это как создать папку для проекта, но в облаке, с возможностью делиться с другими и хранить историю изменений.</p>
  </div>
  
  <h3>Зачем нужен репозиторий?</h3>
  <ul>
    <li><i class="fas fa-code"></i> <strong>Хранение кода:</strong> Все файлы проекта в одном месте</li>
    <li><i class="fas fa-history"></i> <strong>История изменений:</strong> Возможность откатить ошибки</li>
    <li><i class="fas fa-users"></i> <strong>Совместная работа:</strong> Несколько разработчиков могут работать вместе</li>
  </ul>
  
  <h3>Как создать репозиторий?</h3>
  <ol>
    <li><i class="fas fa-sign-in-alt step-icon"></i> <strong>Войдите в GitHub:</strong></li>
    <p>Откройте <a href="https://github.com" class="btn" style="font-size:1.2rem; display:inline-block; margin:0.5rem 0;">GitHub.com</a></p>
    
    <li><i class="fas fa-plus-circle step-icon"></i> <strong>Создайте новый репозиторий:</strong></li>
    <pre><kbd>1. Нажмите "+" в правом верхнем углу
2. Выберите "New repository"</kbd></pre>
    
    <li><i class="fas fa-edit step-icon"></i> <strong>Заполните информацию:</strong></li>
    <pre><code>Repository name: my-java-project
Description: Мой первый Java проект
Public/Private: Public
Initialize with README: ✔</code></pre>
    
    <li><i class="fas fa-check-circle step-icon"></i> <strong>Нажмите "Create repository":</strong></li>
    <p>Ваш репозиторий создан! Теперь он доступен по адресу:</p>
    <pre><code>https://github.com/ваш-логин/my-java-project</code></pre>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> Всегда добавляйте README.md - это визитная карточка вашего проекта!</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-download step-icon"></i> Клонирование репозитория</h2>
  
  <h3>Как получить копию проекта на компьютер?</h3>
  <ol>
    <li><i class="fas fa-copy step-icon"></i> <strong>Скопируйте ссылку на репозиторий:</strong></li>
    <pre><kbd>1. Нажмите зеленую кнопку "Code"
2. Скопируйте HTTPS-ссылку</kbd></pre>
    
    <li><i class="fas fa-terminal step-icon"></i> <strong>Выполните команду клонирования:</strong></li>
    <pre><code>git clone https://github.com/ваш-логин/my-java-project.git</code></pre>
    
    <li><i class="fas fa-folder-open step-icon"></i> <strong>Перейдите в папку проекта:</strong></li>
    <pre><code>cd my-java-project</code></pre>
  </ol>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> Для работы с Java проектом откройте папку в вашей IDE (IntelliJ IDEA, Eclipse и др.)</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-code-commit step-icon"></i> Первые коммиты</h2>
  
  <h3>Как сохранить изменения в репозитории?</h3>
  <ol>
    <li><i class="fas fa-file-alt step-icon"></i> <strong>Создайте или измените файл:</strong></li>
    <pre><code>echo "public class Main {}" > Main.java</code></pre>
    
    <li><i class="fas fa-plus-square step-icon"></i> <strong>Добавьте файл в индекс:</strong></li>
    <pre><code>git add Main.java</code></pre>
    
    <li><i class="fas fa-save step-icon"></i> <strong>Сделайте коммит:</strong></li>
    <pre><code>git commit -m "Добавлен Main класс"</code></pre>
    
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте изменения на GitHub:</strong></li>
    <pre><code>git push origin main</code></pre>
  </ol>
  
  <div style="background:#f8f9fa; border:1px solid #ddd; border-radius:6px; padding:1rem; margin:1.5rem 0;">
    <h4 style="margin-top:0;">Чеклист перед коммитом:</h4>
    <ul>
      <li><input type="checkbox"> Код компилируется</li>
      <li><input type="checkbox"> Добавлены все нужные файлы</li>
      <li><input type="checkbox"> Сообщение коммита понятное и информативное</li>
    </ul>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-cogs step-icon"></i> Полезные команды Git</h2>
  
  <h3>Основные команды для работы</h3>
  <table style="width:100%; border-collapse:collapse; margin:1.5rem 0;">
    <tr style="background:#e9ecef;">
      <th style="padding:0.8rem; text-align:left;">Команда</th>
      <th style="padding:0.8rem; text-align:left;">Описание</th>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>git status</code></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Показать текущее состояние</td>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>git log</code></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Показать историю коммитов</td>
    </tr>
    <tr>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;"><code>git diff</code></td>
      <td style="padding:0.8rem; border-bottom:1px solid #ddd;">Показать изменения в файлах</td>
    </tr>
    <tr>
      <td style="padding:0.8rem;"><code>git restore --staged файл</code></td>
      <td style="padding:0.8rem;">Отменить добавление файла</td>
    </tr>
  </table>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> Используйте <code>git log --oneline</code> для компактного просмотра истории</p>
  </div>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://git-scm.com/book/ru/v2" class="btn" style="font-size:1.2rem;">Официальная документация Git</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/02-signup/' | relative_url }}" class="nav-button">← Регистрация на GitHub</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/04-branches/' | relative_url }}" class="nav-button">Работа с ветками →</a>
</nav>