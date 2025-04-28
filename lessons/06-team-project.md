---
layout: default
title: Командный проект
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
  <h1 style="font-size:2.8rem;">👥 Командный проект</h1>
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
    <li><strong>Скачайте проект с GitHub:</strong> Используйте команду <code>git clone</code>, чтобы скопировать репозиторий на свой компьютер. Она создаёт папку <code>team-quiz</code> с файлами проекта.</li>
    ```
    <pre><code>git clone https://github.com/JavaTeam/team-quiz.git</code></pre>
    ```
    <li><strong>Перейдите в папку проекта:</strong> Команда <code>cd</code> меняет текущую папку, чтобы вы могли работать с файлами викторины.</li>
    ```
    <pre><code>cd team-quiz</code></pre>
    ```
    <li><strong>Проверьте файлы:</strong> В папке должны быть:
      <ul style="padding-left:1.5rem;">
        <li><code>Question.java</code> — класс для хранения вопроса и ответа.</li>
        <li><code>Quiz.java</code> — класс, куда вы добавите свой вопрос.</li>
        <li><code>Main.java</code> — класс для запуска викторины.</li>
        <li><code>.gitignore</code> — исключает ненужные файлы.</li>
        <li><code>README.md</code> — инструкция по запуску.</li>
      </ul>
    </li>
    <li><strong>Убедитесь, что вы в списке участников:</strong> Попросите учителя добавить вас в <strong>Settings > Collaborators</strong> на GitHub, чтобы вы могли отправлять изменения.</li>
  </ol>
  <p><strong>Пример:</strong> Вы ввели <code>git clone https://github.com/JavaTeam/team-quiz.git</code> и получили папку <code>team-quiz</code>. Внутри вы нашли <code>Quiz.java</code>, где скоро добавите свой вопрос. Теперь вы готовы к работе!</p>
  <p style="font-style:italic; color:#555;">Репозиторий — это ваш старт для викторины!</p>

  <h2 style="font-size:1.8rem;">📋 Добавление вопроса в викторину</h2>
  <p>Каждый из вас создаст свою ветку, добавит один вопрос в <code>Quiz.java</code> и отправит изменения на GitHub для проверки. Ветка — это как отдельная копия проекта, где вы работаете, не мешая другим.</p>
  <p><strong>Зачем это нужно?</strong> Ветки позволяют всем 13 участникам работать одновременно, добавляя свои вопросы. Пул-реквесты помогают проверить ваш вопрос, чтобы он был правильным и интересным.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Вы добавите вопрос в файл <code>Quiz.java</code> в части, где написано <code>questions.add</code>.</li>
    <li>Ветка называется <code>question-<ваше_имя></code>, например, <code>question-alex</code>.</li>
    <li>Вопрос — это текст, 4 варианта ответа и правильный ответ (число от 1 до 4).</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создайте задачу на GitHub:</strong> Зайдите в репозиторий <code>JavaTeam/team-quiz</code> на GitHub, перейдите в раздел <strong>Issues</strong> и создайте новую задачу, например, "Добавить вопрос от Alex". Это будет ваш номер задачи, например, #1.</li>
    <li><strong>Создайте свою ветку:</strong> Команда <code>git checkout -b</code> создаёт новую ветку и сразу переключает вас на неё. Замените <code>alex</code> на своё имя.</li>
    ```
    <pre><code>git checkout -b question-alex</code></pre>
    ```
    <p>Эта команда говорит: "Создай ветку <code>question-alex</code> и работай в ней". Теперь ваши изменения не затронут главную ветку <code>main</code>.</p>
    <li><strong>Откройте <code>Quiz.java</code>:</strong> Найдите файл <code>Quiz.java</code> в папке <code>team-quiz</code>. Он выглядит так:</li>
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
    <li><strong>Добавьте свой вопрос:</strong> Внутри <code>public Quiz()</code> добавьте строку с вашим вопросом. Например, Alex добавляет вопрос про JVM:</li>
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
    <p>Что здесь происходит:
      <ul style="padding-left:1.5rem;">
        <li><code>questions.add</code> — добавляет новый вопрос в список.</li>
        <li><code>new Question</code> — создаёт вопрос с текстом, четырьмя вариантами и правильным ответом (1 — это "Виртуальная машина").</li>
      </ul>
    </p>
    <li><strong>Сохраните изменения в Git:</strong> Команда <code>git add</code> говорит Git, что вы хотите сохранить изменения в файле <code>Quiz.java</code>.</li>
    ```
    <pre><code>git add Quiz.java</code></pre>
    ```
    <li><strong>Запишите, что вы сделали:</strong> Команда <code>git commit</code> сохраняет ваши изменения с описанием. Описание в кавычках объясняет, что вы добавили.</li>
    ```
    <pre><code>git commit -m "Added question about JVM by Alex"</code></pre>
    ```
    <p>Это как сделать заметку: "Я добавил вопрос про JVM".</p>
    <li><strong>Отправьте изменения на GitHub:</strong> Команда <code>git push</code> загружает вашу ветку <code>question-alex</code> на GitHub, чтобы другие могли её увидеть.</li>
    ```
    <pre><code>git push origin question-alex</code></pre>
    ```
    <p>Здесь <code>origin</code> — это адрес репозитория, а <code>question-alex</code> — ваша ветка.</p>
    <li><strong>Создайте пул-реквест:</strong> Зайдите на GitHub в репозиторий <code>JavaTeam/team-quiz</code>. Вы увидите предложение создать пул-реквест для ветки <code>question-alex</code>. Нажмите <strong>Create Pull Request</strong>. В описании напишите, что это за вопрос, и укажите номер вашей задачи, например, <code>#1</code>. Попросите учителя или друга проверить ваш PR.</li>
    <li><strong>Дождитесь проверки:</strong> Ваш PR проверят, и если всё хорошо, его сольют в главную ветку <code>main</code>. Если попросят исправить вопрос, вы узнаете, как это сделать, в следующем разделе.</li>
  </ol>
  <p><strong>Пример:</strong> Alex создал ветку <code>question-alex</code>, добавил вопрос про JVM в <code>Quiz.java</code> и отправил изменения на GitHub. На сайте он создал PR для задачи #1. Maria делает то же самое в ветке <code>question-maria</code>, добавляя свой вопрос. Вместе вы создаёте викторину!</p>
  <p style="font-style:italic; color:#555;">Ваш вопрос — часть большой викторины!</p>

  <h2 style="font-size:1.8rem;">📅 Отслеживание вопросов с GitHub Projects</h2>
  <p>GitHub Projects — это как доска, где мы видим, кто какие вопросы добавляет. Она делится на колонки: To Do (надо сделать), In Progress (работа начата), Done (готово).</p>
  <p><strong>Зачем это нужно?</strong> Доска помогает следить за прогрессом всех 13 участников, чтобы никто не забыл добавить свой вопрос.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Каждый вопрос — это задача (issue) на GitHub.</li>
    <li>Задачи перемещаются по колонкам, когда вы начинаете или заканчиваете работу.</li>
    <li>Доска находится в разделе <strong>Projects</strong> репозитория.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создайте доску:</strong> В репозитории <code>JavaTeam/team-quiz</code> перейдите в <strong>Projects</strong> и создайте проект "Quiz Board".</li>
    <li><strong>Добавьте колонки:</strong> Создайте три колонки: To Do, In Progress, Done.</li>
    <li><strong>Создайте задачи:</strong> В разделе <strong>Issues</strong> создайте 13 задач, например, "Добавить вопрос от Alex" (#1), "Добавить вопрос от Maria" (#2). Добавьте их в колонку To Do.</li>
    <li><strong>Обновляйте доску:</strong> Когда вы создаёте ветку <code>question-alex</code>, переместите задачу #1 в In Progress. Когда ваш PR сольют, переместите её в Done.</li>
  </ol>
  <p><strong>Пример:</strong> Задача #1 для Alex начинается в To Do. Когда он создаёт ветку <code>question-alex</code>, задача перемещается в In Progress. После слияния PR она в Done, и все видят, что Alex добавил вопрос.</p>
  <p style="font-style:italic; color:#555;">Доска помогает нам работать вместе!</p>

  <h2 style="font-size:1.8rem;">🔍 Проверка вашего вопроса</h2>
  <p>Пул-реквест (PR) — это когда вы просите команду проверить ваш вопрос в <code>Quiz.java</code>. Кто-то посмотрит ваш код и скажет, всё ли правильно.</p>
  <p><strong>Зачем это нужно?</strong> Проверка помогает сделать вопросы понятными и без ошибок, чтобы викторина была классной.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Проверяют, что у вопроса 4 варианта ответа и правильный ответ от 1 до 4.</li>
    <li>Если нужно исправить, вы добавите изменения в ту же ветку.</li>
    <li>Когда PR одобрят, ваш вопрос станет частью викторины.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Проверьте PR:</strong> В PR для <code>question-alex</code> ревьюер (учитель или друг) посмотрит ваш вопрос в <code>Quiz.java</code>.</li>
    <li><strong>Исправьте, если нужно:</strong> Допустим, ревьюер попросил уточнить вопрос. Откройте <code>Quiz.java</code> и измените его, например:</li>
    ```
    <pre><code>questions.add(new Question(
    "Что такое Java Virtual Machine (JVM)?",
    new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
    1
));</code></pre>
    ```
    <li><strong>Сохраните исправления:</strong> Снова используйте <code>git add</code> и <code>git commit</code>, чтобы сохранить изменения.</li>
    ```
    <pre><code>git add Quiz.java</code></pre>
    <pre><code>git commit -m "Updated question wording as requested"</code></pre>
    ```
    <li><strong>Отправьте исправления:</strong> Команда <code>git push</code> обновит ваш PR с новыми изменениями.</li>
    ```
    <pre><code>git push origin question-alex</code></pre>
    ```
    <p>Ваш PR на GitHub автоматически покажет обновления, и ревьюер проверит их.</p>
    <li><strong>Дождитесь одобрения:</strong> Когда ревьюер скажет, что всё хорошо, он сольёт ваш PR в ветку <code>main</code>. Ваш вопрос теперь в викторине!</li>
  </ol>
  <p><strong>Пример:</strong> В PR для <code>question-alex</code> ревьюер попросил написать "Java Virtual Machine" вместо "JVM". Alex исправил <code>Quiz.java</code>, отправил изменения, и после проверки его вопрос добавили в викторину.</p>
  <p style="font-style:italic; color:#555;">Проверка делает нашу викторину лучше!</p>

  <h2 style="font-size:1.8rem;">🚀 Запуск викторины</h2>
  <p>Когда все 13 вопросов добавлены, мы можем запустить викторину и попробовать ответить на вопросы!</p>
  <p><strong>Зачем это нужно?</strong> Запуск показывает, как работает наша викторина, и позволяет увидеть все вопросы, которые мы создали вместе.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><code>Main.java</code> показывает вопросы, принимает ответы (1–4) и считает очки.</li>
    <li>Мы используем <code>javac</code> для компиляции и <code>java</code> для запуска.</li>
    <li><code>README.md</code> уже объясняет, как запустить викторину.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Убедитесь, что все вопросы добавлены:</strong> Проверьте на GitHub, что все 13 PR слиты в ветку <code>main</code>.</li>
    <li><strong>Обновите свой проект:</strong> Переключитесь на ветку <code>main</code> и скачайте последние изменения с GitHub. Команда <code>git checkout main</code> переключает вас на главную ветку, а <code>git pull</code> загружает все вопросы.</li>
    ```
    <pre><code>git checkout main</code></pre>
    <pre><code>git pull origin main</code></pre>
    ```
    <li><strong>Скомпилируйте проект:</strong> Команда <code>javac</code> превращает Java-файлы в программу, которую можно запустить.</li>
    ```
    <pre><code>javac Question.java Quiz.java Main.java</code></pre>
    ```
    <li><strong>Запустите викторину:</strong> Команда <code>java</code> запускает программу, и вы увидите вопросы.</li>
    ```
    <pre><code>java Main</code></pre>
    ```
    <p>Вы увидите вопросы, выберете ответы (1–4), и программа покажет ваш счёт.</p>
  </ol>
  <p><strong>Пример:</strong> После слияния всех вопросов вы запустили <code>java Main</code>. Викторина показала вопрос: "Что такое JVM?", вы выбрали 1 и получили "Правильно!". В конце вы увидели счёт. Это результат работы всей команды!</p>
  <p style="font-style:italic; color:#555;">Наша викторина готова к игре!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/05-pull-requests/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/07-advanced-git/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>