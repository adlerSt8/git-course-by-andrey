---
layout: default
title: Командная работа
permalink: /lessons/06-team-project/
nav_order: 6
---

<style>
  pre, code {
    background: #e9ecef;
    padding: 0.5rem;
    border: 1px solid #ddd;
    border-radius: 4px;
    font-family: 'Courier New', Courier, monospace;
    font-size: 1rem;
    display: block;
    overflow-x: auto;
  }
  code {
    padding: 0.2rem 0.4rem;
    display: inline;
  }
</style>

<div style="text-align:center; margin: 2rem 0;">
  <h1 style="font-size:2.8rem;">👥 Командная работа</h1>
  <p style="color:#555; font-size:1.3rem;">Создаём викторину на Java вместе</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:2rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0; line-height:1.8; font-size:1.1rem;">
  <h2 style="font-size:1.8rem;">🏗 Подготовка к работе</h2>
  <p>Мы будем работать над викториной — программой, где игроки отвечают на вопросы с четырьмя вариантами ответа. Проект уже готов в репозитории <code>JavaTeam/team-quiz</code> на GitHub. Там есть файлы: <code>Question.java</code>, <code>Quiz.java</code>, <code>Main.java</code>, <code>.gitignore</code> и <code>README.md</code>. Ваша задача — добавить один вопрос в <code>Quiz.java</code>.</p>
  <p><strong>Зачем это нужно?</strong> Репозиторий объединяет нашу команду из 13 человек. Каждый добавит свой вопрос, и вместе мы создадим крутую викторину!</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Репозиторий уже настроен, и вы можете его скачать.</li>
    <li>Вы создадите свою ветку с именем <code>question-<ваше_имя></code>, например, <code>question-alex</code>.</li>
    <li>Все изменения вносятся через пул-реквесты, чтобы их проверили.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Скачайте проект с GitHub:</strong> Команда <code>git clone</code> копирует репозиторий на ваш компьютер, создавая папку <code>team-quiz</code>.</li>
    ```
    <pre><code>git clone https://github.com/JavaTeam/team-quiz.git</code></pre>
    ```
    <li><strong>Перейдите в папку проекта:</strong> Команда <code>cd</code> открывает папку <code>team-quiz</code>, где лежат файлы.</li>
    ```
    <pre><code>cd team-quiz</code></pre>
    ```
    <li><strong>Проверьте файлы:</strong> Убедитесь, что в папке есть:
      <ul style="padding-left:1.5rem;">
        <li><code>Question.java</code> — класс для хранения вопроса и ответа.</li>
        <li><code>Quiz.java</code> — класс, куда вы добавите свой вопрос.</li>
        <li><code>Main.java</code> — класс для запуска викторины.</li>
        <li><code>.gitignore</code> — исключает ненужные файлы.</li>
        <li><code>README.md</code> — инструкция по запуску.</li>
      </ul>
    </li>
    <li><strong>Добавьтесь в участники:</strong> Попросите учителя включить вас в <strong>Settings > Collaborators</strong> на GitHub, чтобы вы могли отправлять изменения.</li>
  </ol>
  <p><strong>Пример:</strong> Вы скачали проект с помощью <code>git clone</code> и зашли в папку <code>team-quiz</code>. Вы видите <code>Quiz.java</code> и готовы добавить свой вопрос.</p>
  <p style="font-style:italic; color:#555;">Репозиторий — ваш старт для викторины!</p>

  <h2 style="font-size:1.8rem;">📋 Добавление вопроса в викторину</h2>
  <p>Вы создадите свою ветку, добавите вопрос в <code>Quiz.java</code> и отправите его на проверку. Ветка — это как ваша личная копия проекта, где вы работаете, не мешая другим.</p>
  <p><strong>Зачем это нужно?</strong> Ветки позволяют всем 13 участникам добавлять вопросы одновременно. Пул-реквесты помогают убедиться, что ваш вопрос правильный.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Вопрос добавляется в <code>Quiz.java</code> в месте с <code>questions.add</code>.</li>
    <li>Ветка называется <code>question-<ваше_имя></code>, например, <code>question-alex</code>.</li>
    <li>Вопрос включает текст, 4 варианта ответа и правильный ответ (1–4).</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создайте задачу на GitHub:</strong> В репозитории <code>JavaTeam/team-quiz</code> зайдите в <strong>Issues</strong> и создайте задачу, например, "Добавить вопрос от Alex" (#1).</li>
    <li><strong>Создайте ветку:</strong> Команда <code>git checkout -b</code> создаёт ветку и переключает вас на неё. Замените <code>alex</code> на своё имя.</li>
    ```
    <pre><code>git checkout -b question-alex</code></pre>
    ```
    <p>Это создаёт ветку <code>question-alex</code>, где вы будете работать.</p>
    <li><strong>Откройте <code>Quiz.java</code>:</strong> В папке <code>team-quiz</code> найдите <code>Quiz.java</code>. Он выглядит так:</li>
    ```
    <pre><code>import java.util.ArrayList;

public class Quiz {
    private ArrayList<Question> questions = new ArrayList<>();
    private int score = 0;

    public Quiz() {
        // Участники добавляют вопросы здесь
    }

    public ArrayList<Question> getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</code></pre>
    ```
    <li><strong>Добавьте вопрос:</strong> В конструкторе <code>public Quiz()</code> добавьте свой вопрос, например:</li>
    ```
    <pre><code>import java.util.ArrayList;

public class Quiz {
    private ArrayList<Question> questions = new ArrayList<>();
    private int score = 0;

    public Quiz() {
        // Участники добавляют вопросы здесь
        questions.add(new Question(
            "Что такое JVM?",
            new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
            1
        ));
    }

    public ArrayList<Question> getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</code></pre>
    ```
    <p>Что это делает:
      <ul style="padding-left:1.5rem;">
        <li><code>questions.add</code> — добавляет вопрос в список.</li>
        <li><code>new Question</code> — создаёт вопрос с текстом, четырьмя вариантами и правильным ответом (1).</li>
      </ul>
    </p>
    <li><strong>Сохраните изменения:</strong> Команда <code>git add</code> выбирает <code>Quiz.java</code> для сохранения.</li>
    ```
    <pre><code>git add Quiz.java</code></pre>
    ```
    <li><strong>Опишите изменения:</strong> Команда <code>git commit</code> сохраняет ваш вопрос с описанием.</li>
    ```
    <pre><code>git commit -m "Added question about JVM by Alex"</code></pre>
    ```
    <p>Это как заметка: "Я добавил вопрос про JVM".</p>
    <li><strong>Отправьте на GitHub:</strong> Команда <code>git push</code> загружает ветку <code>question-alex</code> на GitHub.</li>
    ```
    <pre><code>git push origin question-alex</code></pre>
    ```
    <li><strong>Создайте пул-реквест:</strong> На GitHub в <code>JavaTeam/team-quiz</code> появится уведомление о ветке <code>question-alex</code>. Нажмите <strong>Create Pull Request</strong>, укажите задачу (#1) и попросите учителя проверить.</li>
    <li><strong>Дождитесь проверки:</strong> Если всё хорошо, ваш PR сольют в <code>main</code>. Если нужны исправления, смотрите следующий раздел.</li>
  </ol>
  <p><strong>Пример:</strong> Alex создал ветку <code>question-alex</code>, добавил вопрос про JVM и отправил PR для задачи #1. Maria сделала ветку <code>question-maria</code> и добавила свой вопрос. Вместе вы создаёте викторину!</p>
  <p style="font-style:italic; color:#555;">Ваш вопрос делает викторину особенной!</p>

  <h2 style="font-size:1.8rem;">📅 Отслеживание вопросов с GitHub Projects</h2>
  <p>GitHub Projects — это доска, где мы видим, кто какие вопросы добавляет. Она делит задачи на To Do (надо сделать), In Progress (в работе), Done (готово).</p>
  <p><strong>Зачем это нужно?</strong> Доска помогает следить за 13 вопросами, чтобы все добавили свои.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Каждый вопрос — это задача (issue).</li>
    <li>Задачи двигаются по колонкам, когда вы работаете.</li>
    <li>Доска в разделе <strong>Projects</strong>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создайте доску:</strong> В <code>JavaTeam/team-quiz</code> в <strong>Projects</strong> создайте "Quiz Board".</li>
    <li><strong>Добавьте колонки:</strong> To Do, In Progress, Done.</li>
    <li><strong>Создайте задачи:</strong> В <strong>Issues</strong> добавьте 13 задач, например, "Добавить вопрос от Alex" (#1), и поместите их в To Do.</li>
    <li><strong>Обновляйте доску:</strong> Переместите задачу #1 в In Progress, когда создадите ветку <code>question-alex</code>. После слияния PR — в Done.</li>
  </ol>
  <p><strong>Пример:</strong> Задача #1 для Alex в To Do. Он создал ветку <code>question-alex</code>, и задача переместилась в In Progress. После слияния PR она в Done.</p>
  <p style="font-style:italic; color:#555;">Доска помогает нам не запутаться!</p>

  <h2 style="font-size:1.8rem;">🔍 Проверка вашего вопроса</h2>
  <p>Ваш пул-реквест (PR) проверят, чтобы убедиться, что вопрос в <code>Quiz.java</code> правильный и понятный.</p>
  <p><strong>Зачем это нужно?</strong> Проверка помогает избежать ошибок и делает викторину лучше.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Проверяют, что у вопроса 4 варианта и правильный ответ (1–4).</li>
    <li>Если нужно исправить, вы обновите свою ветку.</li>
    <li>Одобренный PR добавляет ваш вопрос в викторину.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Проверьте PR:</strong> В PR для <code>question-alex</code> учитель посмотрит ваш вопрос.</li>
    <li><strong>Исправьте, если нужно:</strong> Если попросят уточнить, измените <code>Quiz.java</code>, например:</li>
    ```
    <pre><code>questions.add(new Question(
    "Что такое Java Virtual Machine (JVM)?",
    new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
    1
));</code></pre>
    ```
    <li><strong>Сохраните исправления:</strong> Добавьте и сохраните изменения.</li>
    ```
    <pre><code>git add Quiz.java</code></pre>
    <pre><code>git commit -m "Updated question wording"</code></pre>
    ```
    <li><strong>Отправьте исправления:</strong> Обновите PR.</li>
    ```
    <pre><code>git push origin question-alex</code></pre>
    ```
    <li><strong>Дождитесь одобрения:</strong> После проверки PR сольют в <code>main</code>.</li>
  </ol>
  <p><strong>Пример:</strong> Ревьюер попросил Alex уточнить "JVM". Он исправил <code>Quiz.java</code>, отправил изменения, и вопрос добавили в викторину.</p>
  <p style="font-style:italic; color:#555;">Проверка улучшает нашу викторину!</p>

  <h2 style="font-size:1.8rem;">🚀 Запуск викторины</h2>
  <p>Когда все 13 вопросов готовы, запустите викторину, чтобы увидеть результат!</p>
  <p><strong>Зачем это нужно?</strong> Запуск показывает, как работают ваши вопросы вместе.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><code>Main.java</code> показывает вопросы и считает очки.</li>
    <li>Используем <code>javac</code> и <code>java</code>.</li>
    <li><code>README.md</code> объясняет запуск.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Проверьте, что все PR слиты:</strong> Убедитесь на GitHub, что 13 вопросов в <code>main</code>.</li>
    <li><strong>Обновите проект:</strong> Переключитесь на <code>main</code> и скачайте вопросы.</li>
    ```
    <pre><code>git checkout main</code></pre>
    <pre><code>git pull origin main</code></pre>
    ```
    <li><strong>Скомпилируйте:</strong> Превратите файлы в программу.</li>
    ```
    <pre><code>javac Question.java Quiz.java Main.java</code></pre>
    ```
    <li><strong>Запустите:</strong> Увидите вопросы и сможете ответить.</li>
    ```
    <pre><code>java Main</code></pre>
    ```
  </ol>
  <p><strong>Пример:</strong> Вы запустили <code>java Main</code>, увидели вопрос "Что такое JVM?", выбрали 1 и получили "Правильно!". Это ваша командная викторина!</p>
  <p style="font-style:italic; color:#555;">Викторина — наш общий успех!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/05-pull-requests/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/07-advanced-git/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>