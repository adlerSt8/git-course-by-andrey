---
layout: default
title: Командная работа
permalink: /lessons/06-team-project/
nav_order: 6
---

<style>
  pre {
    background: #e9ecef;
    padding: 1rem;
    border: 1px solid #ddd;
    border-radius: 6px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1rem;
    overflow-x: auto;
    margin: 1rem 0;
  }
  code {
    background: #e9ecef;
    padding: 0.2rem 0.4rem;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1rem;
  }
  kbd {
    background: #f1f1f1;
    padding: 0.2rem 0.4rem;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    box-shadow: 0 1px 1px rgba(0,0,0,0.1);
  }
  .step-icon {
    margin-right: 0.5rem;
    font-size: 1.2rem;
  }
  .container {
    background: #f8f9fa;
    border-radius: 8px;
    padding: 2rem;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    margin: 2rem 0;
    line-height: 1.8;
    font-size: 1.15rem;
  }
  nav a {
    transition: background 0.2s;
  }
  nav a:hover {
    background: #0056b3;
  }
  .btn {
    display: inline-block;
    background-color: #0056b3;
    color: #fff;
    padding: 0.5rem 1rem;
    border-radius: 4px;
    text-decoration: none;
    font-weight: bold;
    transition: background-color 0.2s;
  }
  .btn:hover {
    background-color: #003d7a;
  }
  @media (max-width: 600px) {
    pre, code, kbd {
      font-size: 0.95rem;
    }
    .container {
      padding: 1.5rem;
      font-size: 1.1rem;
    }
  }
</style>

<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

<div style="text-align:center; margin: 2rem 0;">
  <h1 style="font-size:2.8rem;">👥 Командная работа</h1>
  <p style="color:#555; font-size:1.3rem;">Создаём викторину на Java вместе!</p>
</div>

<div class="container">
  <h2 style="font-size:1.8rem;"><i class="fas fa-tools step-icon"></i> Подготовка к работе</h2>
  <p>Мы создаём викторину, где игроки отвечают на вопросы с четырьмя вариантами ответа. Проект уже готов в репозитории <code>JavaTeam/team-quiz</code> на GitHub. В нём есть файлы: <code>Question.java</code> (для вопросов), <code>Quiz.java</code> (для списка вопросов), <code>Main.java</code> (для запуска), <code>.gitignore</code> (чтобы не загружать лишнее) и <code>README.md</code> (с инструкцией). Ваша задача — добавить один вопрос в <code>Quiz.java</code>.</p>
  <p><strong>Почему это важно?</strong> В команде из 13 человек каждый добавляет свой вопрос, и вместе мы получаем крутую викторину!</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>📥 Репозиторий можно скачать на компьютер.</li>
    <li>🌿 Вы создадите свою ветку <code>question-<ваше_имя></code> (например, <code>question-alex</code>), чтобы работать отдельно.</li>
    <li>✅ Изменения отправляются через пул-реквесты (PR), чтобы учитель их проверил.</li>
  </ul>
  <p><strong>Как начать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-download step-icon"></i> <strong>Скачайте проект:</strong> Команда <kbd>git clone</kbd> копирует проект на ваш компьютер, создавая папку <code>team-quiz</code>. Это как скачать папку с файлами викторины.</li>
    <pre>git clone https://github.com/JavaTeam/team-quiz.git</pre>
    <li><i class="fas fa-folder-open step-icon"></i> <strong>Зайдите в папку:</strong> Команда <kbd>cd</kbd> открывает папку <code>team-quiz</code>, где лежат все файлы.</li>
    <pre>cd team-quiz</pre>
    <li><i class="fas fa-file-code step-icon"></i> <strong>Проверьте файлы:</strong> Убедитесь, что в папке есть:
      <ul style="padding-left:1.5rem;">
        <li><code>Question.java</code> — хранит вопрос и ответ.</li>
        <li><code>Quiz.java</code> — сюда вы добавите свой вопрос.</li>
        <li><code>Main.java</code> — запускает викторину.</li>
        <li><code>.gitignore</code> — исключает ненужные файлы, например, <code>.class</code>.</li>
        <li><code>README.md</code> — объясняет, как запустить проект.</li>
      </ul>
    </li>
    <li><i class="fas fa-user-plus step-icon"></i> <strong>Станьте участником:</strong> Попросите учителя добавить вас в <strong>Settings > Collaborators</strong> на GitHub, чтобы вы могли отправлять свои изменения.</li>
  </ol>
  <p><strong>Пример:</strong> Вы ввели <kbd>git clone https://github.com/JavaTeam/team-quiz.git</kbd>, получили папку <code>team-quiz</code> и нашли <code>Quiz.java</code>. Теперь вы готовы добавить свой вопрос!</p>
  <p style="font-style:italic; color:#555;">Репозиторий — это ваш старт для викторины! 🚀</p>

  <h2 style="font-size:1.8rem;"><i class="fas fa-pen step-icon"></i> Добавление вопроса</h2>
  <p>Вы создадите ветку — это как ваш личный черновик проекта, где можно работать, не мешая другим. Затем добавите вопрос в <code>Quiz.java</code> и отправите его на проверку через пул-реквест.</p>
  <p><strong>Почему это важно?</strong> Ветки позволяют всем 13 участникам работать одновременно. Пул-реквесты проверяют, что ваш вопрос правильный и интересный.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>📝 Вопрос добавляется в <code>Quiz.java</code> в строку <code>questions.add</code>.</li>
    <li>🌿 Ветка называется <code>question-<ваше_имя></code> (например, <code>question-alex</code>).</li>
    <li>❓ Вопрос — это текст, 4 варианта ответа и правильный ответ (число 1–4).</li>
  </ul>
  <p><strong>Как это сделать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачу:</strong> На GitHub в <code>JavaTeam/team-quiz</code> зайдите в <strong>Issues</strong> и создайте задачу, например, "Добавить вопрос от Alex" (#1). Это как карточка с вашим заданием.</li>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong> Введите команду <kbd>git checkout -b question-alex</kbd>. Ветка — это ваш рабочий процесс.</li>
    <pre>git checkout -b question-alex</pre>
    <li><i class="fas fa-edit step-icon"></i> <strong>Добавьте свой вопрос:</strong> Откройте <code>Quiz.java</code> и добавьте строку с вопросом в метод <code>addQuestion</code> (например, <code>questions.add(new Question("Что такое Java?", "Язык программирования", "Операционная система", "Система управления базами данных", "Игра", 1));</code>).</li>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте изменения:</strong> Когда закончите, отправьте изменения через команду <kbd>git push</kbd>.</li>
    <pre>git push origin question-alex</pre>
    <li><i class="fas fa-check step-icon"></i> <strong>Создайте пул-реквест:</strong> На GitHub откройте репозиторий и создайте пул-реквест, чтобы предложить ваш вопрос для проверки.</li>
  </ol>
  <p style="font-style:italic; color:#555;">Вопрос успешно добавлен! Осталось только ждать одобрения. 📩</p>
</div>

<div style="text-align:center; margin: 2rem 0;">
  <a href="https://github.com/JavaTeam/team-quiz" class="btn">Посмотреть репозиторий</a>
</div>

