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
    max-width: 2000px;  /* Добавили максимальную ширину */
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
  <h1 style="font-size:3rem;">🤝 Пул-реквесты и совместная работа. Редакция 3</h1>
  <p style="color:#333; font-size:1.5rem;">Учимся работать в команде через GitHub</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-question-circle step-icon"></i> Что такое пул-реквест?</h2>
  <p>Пул-реквест (Pull Request, PR) — это способ предложить изменения в проект и обсудить их с командой перед добавлением в основную версию.</p>
  
  <div style="background:#e6f3ff; border-left:4px solid #007bff; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Простыми словами:</strong> Это как сказать коллегам: "Я сделал новую функцию, посмотрите, всё ли правильно, прежде чем мы добавим её в проект".</p>
  </div>
  
  <h3>Зачем нужны пул-реквесты?</h3>
  <ul>
    <li><i class="fas fa-check-circle"></i> <strong>Контроль качества:</strong> Код проверяют несколько человек</li>
    <li><i class="fas fa-comments"></i> <strong>Обсуждение:</strong> Можно задать вопросы и предложить улучшения</li>
    <li><i class="fas fa-history"></i> <strong>История изменений:</strong> Все правки сохраняются и видны</li>
  </ul>
  
  <h3>Как это работает на практике?</h3>
  <p>Представьте, вы работаете над классом <code>UserService.java</code>:</p>
  <ol>
    <li>Создаете отдельную ветку: <code>feature-user-auth</code></li>
    <li>Добавляете новый метод аутентификации</li>
    <li>Отправляете изменения на GitHub</li>
    <li>Создаете PR и просите коллег проверить ваш код</li>
  </ol>
  
  <div style="background:#fff8e6; border-left:4px solid #ffc107; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Важно:</strong> В хороших проектах никто не добавляет код в основную ветку <code>main</code> напрямую — все изменения проходят через пул-реквесты!</p>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-plus-circle step-icon"></i> Как создать пул-реквест</h2>
  
  <h3>Пошаговая инструкция</h3>
  <ol>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong></li>
    <pre><kbd>git checkout -b feature-user-login</kbd></pre>
    <p>Эта команда создаст новую ветку и сразу переключит вас на неё.</p>
    
    <li><i class="fas fa-edit step-icon"></i> <strong>Внесите изменения:</strong></li>
    <p>Например, добавьте новый метод в <code>AuthController.java</code>:</p>
    <pre><code>public ResponseEntity&lt;String&gt; loginUser(@RequestBody User user) {
    // Ваш код аутентификации
    return ResponseEntity.ok("Успешный вход!");
}</code></pre>
    
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните изменения:</strong></li>
    <pre><kbd>git add AuthController.java</kbd></pre>
    <pre><kbd>git commit -m "Добавлен метод входа пользователя"</kbd></pre>
    
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте на GitHub:</strong></li>
    <pre><kbd>git push origin feature-user-login</kbd></pre>
    
    <li><i class="fas fa-code-pull-request step-icon"></i> <strong>Создайте PR на GitHub:</strong></li>
    <p>После push откройте GitHub, перейдите в свой репозиторий:</p>
    <ol type="a">
      <li>Нажмите на вкладку <strong>Pull requests</strong></li>
      <li>Выберите <strong>New pull request</strong></li>
      <li>Укажите вашу ветку (feature-user-login) и целевую (main)</li>
      <li>Заполните описание: что изменили и зачем</li>
      <li>Нажмите <strong>Create pull request</strong></li>
    </ol>
  </ol>
  
  <div style="background:#e6ffe6; border-left:4px solid #28a745; padding:1rem; margin:1.5rem 0; border-radius:0 4px 4px 0;">
    <p><strong>Совет:</strong> В описании PR используйте чеклист, чтобы показать, что сделано:</p>
    <pre><code>- [x] Добавлен метод loginUser()
- [ ] Написаны тесты (сделаю в следующем PR)</code></pre>
  </div>

  <h2 style="font-size:2rem;"><i class="fas fa-search step-icon"></i> Как проводить код-ревью</h2>
  <p>Код-ревью — это процесс проверки кода в пул-реквесте другими разработчиками.</p>
  
  <h3>Что проверять в чужом коде?</h3>
  <ul>
    <li><i class="fas fa-bug"></i> <strong>Ошибки:</strong> Логические ошибки, потенциальные баги</li>
    <li><i class="fas fa-book"></i> <strong>Читаемость:</strong> Понятные названия переменных и методов</li>
    <li><i class="fas fa-shield-alt"></i> <strong>Безопасность:</strong> Нет уязвимостей (например, в паролях)</li>
    <li><i class="fas fa-copy"></i> <strong>Стиль:</strong> Соответствие стандартам проекта</li>
  </ul>
  
  <h3>Как оставить хороший комментарий?</h3>
  <p>Плохой комментарий:</p>
  <div style="background:#ffe6e6; padding:0.5rem; border-radius:4px; margin:0.5rem 0;">
    <p>"Этот код ужасен, переделай!"</p>
  </div>
  
  <p>Хороший комментарий:</p>
  <div style="background:#e6ffe6; padding:0.5rem; border-radius:4px; margin:0.5rem 0;">
    <p>"Метод <code>validatePassword()</code> сейчас не проверяет минимальную длину пароля. Предлагаю добавить проверку <code>if (password.length() < 8)</code> для безопасности."</p>
  </div>
  
  <h3>Как отвечать на комментарии?</h3>
  <ol>
    <li>Если согласны — исправьте и сообщите об этом</li>
    <pre><kbd>git commit -m "Добавил проверку длины пароля"</kbd></pre>
    <pre><kbd>git push origin feature-user-login</kbd></pre>
    
    <li>Если не согласны — вежливо объясните свою позицию</li>
    <p>"Спасибо за замечание! Я специально не добавлял эту проверку, потому что минимальная длина задаётся в настройках безопасности."</p>
  </ol>
  
  <h2 style="font-size:2rem;"><i class="fas fa-check-circle step-icon"></i> Как правильно завершить PR</h2>
  
  <h3>Когда можно мержить?</h3>
  <ul>
    <li>Все комментарии учтены</li>
    <li>Код проходит тесты</li>
    <li>Изменения одобрены ревьюверами (обычно нужно 1-2 approve)</li>
  </ul>
  
  <h3>Типы слияния:</h3>
<ol>
  <li><strong>Merge commit:</strong> Сохраняет историю всех коммитов</li>
  <pre><code>git merge --no-ff feature-user-login</code></pre>
  
  <li><strong>Squash and merge:</strong> Объединяет все коммиты PR в один (для небольших изменений)</li>
  <pre><code># 1. Переключитесь на основную ветку
git checkout main

# 2. Выполните squash-merge
git merge --squash feature-user-login

# 3. Создайте новый коммит (все изменения из PR станут одним коммитом)
git commit -m "Добавлена аутентификация пользователя"

# 4. Отправьте изменения
git push origin main</code></pre>
  <p><i class="fas fa-check-circle"></i> <strong>Преимущества:</strong><br>
  - Чистая история коммитов<br>
  - Подходит для мелких исправлений (1-3 файла)</p>
  
  <p><i class="fas fa-clock"></i> <strong>Когда использовать:</strong><br>
  - При исправлении опечаток<br>
  - Для небольших багфиксов<br>
  - Когда отдельные коммиты PR не имеют самостоятельной ценности</p>

  <div style="background:#f8f9fa; border-left:4px solid #007bff; padding:1rem; margin:1rem 0; border-radius:0 4px 4px 0;">
  <h4 style="margin-top:0;"><i class="fas fa-comment-dots"></i> Пример хорошего сообщения для squash-коммита:</h4>
  <pre><code>feat: Добавлена аутентификация пользователя

- Реализован метод loginUser() 
- Добавлена валидация пароля
- Написаны базовые тесты
- Обновлена документация</code></pre>
  <p><i class="fas fa-lightbulb"></i> <strong>Совет:</strong> Используйте <a href="https://www.conventionalcommits.org/" style="color:#007bff;">Conventional Commits</a> для стандартизации сообщений.</p>
</div>
  
  <li><strong>Rebase and merge:</strong> Перемещает ваши коммиты поверх основной ветки</li>
  <pre><code>git checkout feature-user-login
git rebase main
git checkout main
git merge feature-user-login</code></pre>
</ol>
  
  <div style="background:#f8f9fa; border:1px solid #ddd; border-radius:6px; padding:1rem; margin:1.5rem 0;">
    <h4 style="margin-top:0;">Чеклист перед мержем:</h4>
    <ul>
      <li><input type="checkbox"> Все тесты проходят</li>
      <li><input type="checkbox"> Нет конфликтов с основной веткой</li>
      <li><input type="checkbox"> Описание PR актуально</li>
      <li><input type="checkbox"> Код соответствует стандартам проекта</li>
    </ul>
  </div>
  
  <h2 style="font-size:2rem;"><i class="fas fa-exclamation-triangle step-icon"></i> Частые ошибки новичков</h2>
  
  <h3>1. Большие PR</h3>
  <p><strong>Проблема:</strong> PR на 1000+ строк кода сложно проверять</p>
  <p><strong>Решение:</strong> Разбивайте на маленькие PR по 200-300 строк</p>
  
  <h3>2. Непонятное описание</h3>
  <p><strong>Проблема:</strong> "Исправлены баги" — что именно исправлено?</p>
  <p><strong>Решение:</strong> Подробно описывайте изменения:</p>
  <pre><code>Исправлено:
- Утечка памяти в UserCache
- Некорректная валидация email
- Ошибка при null-значениях</code></pre>
  
  <h3>3. Игнорирование комментариев</h3>
  <p><strong>Проблема:</strong> Автор не отвечает на вопросы ревьюверов</p>
  <p><strong>Решение:</strong> Отвечайте на все комментарии, даже если просто "Спасибо, исправил"</p>
  
  <h3>4. Мерж без тестов</h3>
  <p><strong>Проблема:</strong> Новый код без тестов может сломать проект</p>
  <p><strong>Решение:</strong> Всегда пишите unit-тесты для нового функционала</p>
  <pre><code>@Test
public void testLoginUser() {
    // Тест для метода loginUser()
}</code></pre>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://github.com/features" class="btn" style="font-size:1.2rem;">Узнать больше на GitHub</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/04-branching/' | relative_url }}" class="nav-button">← Работа с ветками</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/06-team-project/' | relative_url }}" class="nav-button">Командный проект →</a>
</nav>