---
layout: default
title: Командная работа
permalink: /lessons/06-team-project/
nav_order: 6
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
  
  /* Стиль для списков */
  ul, ol {
    margin: 1rem 0;
    padding-left: 2rem;
  }
  
  li {
    margin: 0.5rem 0;
  }
  
  /* Стиль для подзаголовков */
  h3 {
    font-size: 1.6rem;
    margin: 1.5rem 0 1rem;
    color: #222;
  }
  
  /* Стиль для примера вывода */
  samp {
    display: block;
    background: #e9ecef;
    padding: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1.2rem;
    margin: 1.5rem 0;
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">👥 Командная работа</h1>
  <p style="color:#333; font-size:1.5rem;">Создаём викторину на Java вместе!</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-tools step-icon"></i> Подготовка к работе</h2>
  <p>Мы создаём викторину на Java, где игроки отвечают на вопросы с четырьмя вариантами ответа. Проект уже готов в репозитории <code>JavaTeam/team-quiz</code> на GitHub. Ваша задача — добавить один вопрос в файл <code>Quiz.java</code>.</p>
  
  <h3>Как начать</h3>
  <ol>
    <li><i class="fas fa-download step-icon"></i> <strong>Скачайте проект:</strong></li>
    <pre><kbd>git clone https://github.com/JavaTeam/team-quiz.git</kbd></pre>
    <p>Введите эту команду в терминале (например, в Git Bash или командной строке).</p>
    
    <li><i class="fas fa-folder-open step-icon"></i> <strong>Зайдите в папку проекта:</strong></li>
    <pre><kbd>cd team-quiz</kbd></pre>
    
    <li><i class="fas fa-file-code step-icon"></i> <strong>Проверьте файлы:</strong></li>
    <ul>
      <li><code>Question.java</code> — определяет структуру вопроса</li>
      <li><code>Quiz.java</code> — сюда вы добавите свой вопрос</li>
      <li><code>Main.java</code> — запускает викторину</li>
      <li><code>.gitignore</code> — указывает, какие файлы не загружать</li>
      <li><code>README.md</code> — инструкции по запуску</li>
    </ul>
  </ol>

  <h2 style="font-size:2rem;"><i class="fas fa-pen step-icon"></i> Добавление вопроса</h2>
  
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачу на GitHub:</strong></li>
    <pre><code>questions.add(new Question(
    "Какой язык программирования используется для Android?",
    new String[]{"Java", "Python", "C++", "Ruby"},
    1
));</code></pre>
    
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong></li>
    <pre><kbd>git checkout -b question-alex</kbd></pre>
    
    <li><i class="fas fa-file-alt step-icon"></i> <strong>Откройте Quiz.java:</strong></li>
    <pre><code>import java.util.ArrayList;

public class Quiz {
    private ArrayList&lt;Question&gt; questions = new ArrayList&lt;&gt;();
    private int score = 0;

    public Quiz() {
        // Здесь добавляем вопросы
    }

    public ArrayList&lt;Question&gt; getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</code></pre>
    
    <li><i class="fas fa-plus-circle step-icon"></i> <strong>Добавьте вопрос:</strong></li>
    <pre><code>public Quiz() {
    // Здесь добавляем вопросы
    questions.add(new Question(
        "Какой язык программирования используется для Android?",
        new String[]{"Java", "Python", "C++", "Ruby"},
        1
    ));
}</code></pre>
    
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните изменения:</strong></li>
    <pre><kbd>git add Quiz.java</kbd></pre>
    
    <li><i class="fas fa-comment step-icon"></i> <strong>Опишите изменения:</strong></li>
    <pre><kbd>git commit -m "Added question about Android programming language"</kbd></pre>
    
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте изменения:</strong></li>
    <pre><kbd>git push origin question-alex</kbd></pre>
  </ol>

  <h2 style="font-size:2rem;"><i class="fas fa-search step-icon"></i> Проверка вашего вопроса</h2>
  
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-eye step-icon"></i> <strong>Проверьте пул-реквест:</strong></li>
    <p>Зайдите на GitHub и проверьте комментарии к вашему PR.</p>
    
    <li><i class="fas fa-edit step-icon"></i> <strong>Исправьте, если нужно:</strong></li>
    <pre><code>questions.add(new Question(
    "Какой язык программирования чаще всего используется для Android?",
    new String[]{"Java", "Python", "C++", "Ruby"},
    1
));</code></pre>
  </ol>

  <h2 style="font-size:2rem;"><i class="fas fa-play step-icon"></i> Запуск викторины</h2>
  
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-check step-icon"></i> <strong>Обновите проект:</strong></li>
    <pre><kbd>git checkout main</kbd></pre>
    <pre><kbd>git pull origin main</kbd></pre>
    
    <li><i class="fas fa-cogs step-icon"></i> <strong>Скомпилируйте программу:</strong></li>
    <pre><kbd>javac Question.java Quiz.java Main.java</kbd></pre>
    
    <li><i class="fas fa-rocket step-icon"></i> <strong>Запустите викторину:</strong></li>
    <pre><kbd>java Main</kbd></pre>
    
    <li><i class="fas fa-gamepad step-icon"></i> <strong>Пример вывода:</strong></li>
    <samp>
Вопрос: Какой язык программирования используется для Android?
1. Java
2. Python
3. C++
4. Ruby
Ваш ответ: 1
Правильно! Счёт: 1
    </samp>
  </ol>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://github.com/JavaTeam/team-quiz" class="btn">Посмотреть репозиторий</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/05-pull-requests/' | relative_url }}" class="nav-button">← Назад</a>
  <a href="{{ '/' | relative_url }}" class="nav-button">Оглавление</a>
  <a href="{{ '/lessons/07-faq/' | relative_url }}" class="nav-button">Далее →</a>
</nav>