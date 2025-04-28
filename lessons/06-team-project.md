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
  }
  /* Стили для навигации */
  nav a {
    transition: background 0.2s;
  }
  nav a:hover {
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
  /* Адаптивность для мобильных устройств */
  @media (max-width: 600px) {
    pre, code, kbd {
      font-size: 1.1rem;
    }
    .container {
      padding: 2rem;
      font-size: 1.3rem;
    }
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 3rem 0;">
  <h1 style="font-size:3rem;">👥 Командная работа. Изменение 3</h1>
  <p style="color:#555; font-size:1.5rem;">Создаём викторину на Java вместе!</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-tools step-icon"></i> Подготовка к работе</h2>
  <p style="font-size:1.4rem;">Мы создаём викторину, где игроки отвечают на вопросы с четырьмя вариантами ответа. Проект уже есть на GitHub в репозитории <code>JavaTeam/team-quiz</code>, и ваша задача — добавить вопрос в <code>Quiz.java</code>.</p>
  <p><strong>Почему это важно?</strong> В команде из 13 человек каждый будет добавлять свой вопрос, и вместе мы получим большую и интересную викторину!</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>📥 Вы скачаете проект на свой компьютер с помощью команды <kbd>git clone</kbd>.</li>
    <li>🌿 После этого создадите свою ветку <code>question-<ваше_имя></code> (например, <code>question-alex</code>), чтобы работать отдельно.</li>
    <li>✅ Когда закончите, создадите пул-реквест (PR), чтобы учитель проверил ваш вопрос.</li>
  </ul>
  <p><strong>Как начать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-download step-icon"></i> <strong>Скачайте проект:</strong> С помощью команды <kbd>git clone</kbd> вы загрузите проект на свой компьютер. Это создаст папку с названием <code>team-quiz</code>.</li>
    <pre>git clone https://github.com/JavaTeam/team-quiz.git</pre>
    <li><i class="fas fa-folder-open step-icon"></i> <strong>Зайдите в папку:</strong> Откройте папку с проектом командой <kbd>cd</kbd> (change directory), чтобы начать работать.</li>
    <pre>cd team-quiz</pre>
    <li><i class="fas fa-file-code step-icon"></i> <strong>Проверьте файлы:</strong> Убедитесь, что в папке есть несколько файлов:
      <ul style="padding-left:1.5rem;">
        <li><code>Question.java</code> — хранит структуру вопроса и ответов.</li>
        <li><code>Quiz.java</code> — сюда мы добавим свой вопрос.</li>
        <li><code>Main.java</code> — запускает викторину.</li>
        <li><code>.gitignore</code> — исключает ненужные файлы (например, временные). Это важно, чтобы не загружать их на GitHub.</li>
        <li><code>README.md</code> — инструкция по запуску проекта.</li>
      </ul>
    </li>
    <li><i class="fas fa-user-plus step-icon"></i> <strong>Станьте участником:</strong> Попросите учителя добавить вас в список участников репозитория на GitHub. Это даст вам возможность вносить изменения.</li>
  </ol>
  <p><strong>Пример:</strong> После выполнения <kbd>git clone</kbd> вы получите папку с проектом. В этой папке будут все нужные файлы, например <code>Quiz.java</code>, в который нужно добавить ваш вопрос.</p>
  <p style="font-style:italic; color:#555;">Репозиторий на GitHub — это ваша рабочая база! 🚀</p>

  <h2 style="font-size:2rem;"><i class="fas fa-pen step-icon"></i> Добавление вопроса</h2>
  <p style="font-size:1.4rem;">Теперь давайте добавим ваш вопрос в викторину. Важно понимать, что вы работаете в своей личной ветке, и это позволяет вам не мешать работе другим участникам команды.</p>
  <p><strong>Почему это важно?</strong> Ветки позволяют нам работать одновременно и без конфликтов, а пул-реквесты помогают учителю проверять изменения перед тем, как они попадут в основную версию.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>📝 Вопрос добавляется в метод <code>addQuestion</code> в <code>Quiz.java</code>.</li>
    <li>🌿 Ваша ветка будет называться <code>question-<ваше_имя> (например, question-alex</code>).</li>
    <li>❓ Вопрос — это строка с текстом вопроса, 4 варианта ответа и правильный ответ (номер 1–4).</li>
  </ul>
  <p><strong>Как это сделать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачу:</strong> На GitHub в разделе <strong>Issues</strong> создайте новую задачу с описанием "Добавить вопрос от [ваше имя]". Это как заметка о том, что вы хотите добавить вопрос.</li>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong> Введите команду <kbd>git checkout -b question-alex</kbd>, чтобы создать и переключиться на свою ветку.</li>
    <pre>git checkout -b question-alex</pre>
    <li><i class="fas fa-edit step-icon"></i> <strong>Добавьте вопрос:</strong> Откройте файл <code>Quiz.java</code> и добавьте ваш вопрос в метод <code>addQuestion</code>. Пример строки:
      <pre>questions.add(new Question("Какой язык программирования используется для Android?", "Java", "Python", "C++", "Ruby", 1));</pre>
    </li>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте изменения:</strong> Когда вы добавите вопрос, отправьте изменения на GitHub командой <kbd>git push</kbd>.</li>
    <pre>git push origin question-alex</pre>
    <li><i class="fas fa-check step-icon"></i> <strong>Создайте пул-реквест:</strong> На GitHub создайте пул-реквест, чтобы предложить ваш вопрос для проверки и добавления в проект.</li>
  </ol>
  <p style="font-style:italic; color:#555;">Ваш вопрос теперь добавлен! Осталось только дождаться одобрения. 📩</p>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://github.com/JavaTeam/team-quiz" class="btn">Посмотреть репозиторий</a>
</div>
