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
  <h1 style="font-size:3rem;">👥 Командная работа. Изменение 6</h1>
  <p style="color:#333; font-size:1.5rem;">Создаём викторину на Java вместе!</p>
</div>

<div class="container">
  <h2 style="font-size:2rem;"><i class="fas fa-tools step-icon"></i> Подготовка к работе</h2>
  <p>Мы создаём викторину на Java, где игроки отвечают на вопросы с четырьмя вариантами ответа. Проект уже готов в репозитории <code>JavaTeam/team-quiz</code> на GitHub. Ваша задача — добавить один вопрос в файл <code>Quiz.java</code>. Репозиторий — это как общая папка, где хранятся все файлы проекта, и мы будем работать в ней вместе.</p>
  <p><strong>Почему это важно?</strong> В нашей команде 13 человек, и каждый добавит свой уникальный вопрос. Вместе мы создадим большую и интересную викторину!</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul>
    <li><i class="fas fa-download"></i> Вы скачаете проект на свой компьютер, чтобы работать с файлами локально.</li>
    <li><i class="fas fa-code-branch"></i> Вы создадите свою ветку (например, <code>question-alex</code>), чтобы ваши изменения не мешали другим. Ветка — это как ваш личный черновик проекта.</li>
    <li><i class="fas fa-check"></i> Ваши изменения отправятся на проверку через пул-реквест (PR) — это как запрос: «Проверьте мой вопрос!».</li>
  </ul>
  <h3>Как начать</h3>
  <ol>
    <li><i class="fas fa-download step-icon"></i> <strong>Скачайте проект:</strong> Используйте команду <kbd>git clone</kbd>, чтобы загрузить проект на свой компьютер. Это как скачать папку с файлами викторины. Команда создаст папку <code>team-quiz</code>.</li>
    <pre><kbd>git clone https://github.com/JavaTeam/team-quiz.git</kbd></pre>
    <p>Введите эту команду в терминале (например, в Git Bash или командной строке).</p>
    <li><i class="fas fa-folder-open step-icon"></i> <strong>Зайдите в папку проекта:</strong> Перейдите в папку <code>team-quiz</code> с помощью команды <kbd>cd</kbd> (change directory). Это как открыть папку, чтобы увидеть файлы.</li>
    <pre><kbd>cd team-quiz</kbd></pre>
    <li><i class="fas fa-file-code step-icon"></i> <strong>Проверьте файлы:</strong> Убедитесь, что в папке <code>team-quiz</code> есть следующие файлы:</li>
    <ul>
      <li><code>Question.java</code> — определяет, как выглядит вопрос (текст, варианты, правильный ответ).</li>
      <li><code>Quiz.java</code> — сюда вы добавите свой вопрос.</li>
      <li><code>Main.java</code> — запускает викторину, чтобы вы могли играть.</li>
      <li><code>.gitignore</code> — указывает, какие файлы не загружать на GitHub (например, временные <code>.class</code>).</li>
      <li><code>README.md</code> — содержит инструкции, как запустить проект.</li>
    </ul>
    <p>Откройте папку в проводнике или редакторе кода (например, IntelliJ IDEA, VS Code) и проверьте, что файлы на месте.</p>
    <li><i class="fas fa-user-plus step-icon"></i> <strong>Станьте участником:</strong> Попросите учителя добавить вас в репозиторий на GitHub. Для этого учитель заходит в <strong>Settings > Collaborators</strong> и добавляет ваш GitHub-аккаунт. Это даст вам право вносить изменения.</li>
  </ol>
  <p><strong>Пример:</strong> Вы ввели <kbd>git clone https://github.com/JavaTeam/team-quiz.git</kbd>, получили папку <code>team-quiz</code>, зашли в неё командой <kbd>cd team-quiz</kbd> и увидели файл <code>Quiz.java</code>. Теперь вы готовы добавить свой вопрос!</p>
  <p style="font-style:italic; color:#333;">Репозиторий — это ваша рабочая база для викторины! 🚀</p>

  <h2 style="font-size:2rem;"><i class="fas fa-pen step-icon"></i> Добавление вопроса</h2>
  <p>Теперь вы добавите свой вопрос в викторину. Вы будете работать в своей ветке — это как отдельная копия проекта, где можно экспериментировать, не трогая основную версию. После этого вы отправите вопрос на проверку через пул-реквест.</p>
  <p><strong>Почему это важно?</strong> Ветки позволяют всем 13 участникам работать одновременно, не мешая друг другу. Пул-реквесты дают учителю возможность проверить ваш вопрос, чтобы он был правильным и понятным.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul>
    <li><i class="fas fa-file-alt"></i> Вопрос добавляется в файл <code>Quiz.java</code> в конструктор <code>public Quiz()</code>.</li>
    <li><i class="fas fa-code-branch"></i> Ваша ветка называется <code>question-<ваше_имя></code> (например, <code>question-alex</code>).</li>
    <li><i class="fas fa-question"></i> Вопрос состоит из текста, четырёх вариантов ответа и номера правильного ответа (1–4).</li>
  </ul>
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачу на GitHub:</strong> Задача (issue) — это как заметка, что вы планируете добавить вопрос. Это помогает следить за вашим прогрессом.</li>
    <ul>
      <li>Зайдите на GitHub в репозиторий <code>JavaTeam/team-quiz</code>.</li>
      <li>Нажмите на вкладку <strong>Issues</strong> (вверху страницы).</li>
      <li>Нажмите зелёную кнопку <strong>New issue</strong>.</li>
      <li>Напишите заголовок, например: «Добавить вопрос от Alex».</li>
      <li>В описании укажите ваш вопрос, чтобы учитель сразу его увидел:</li>
      <pre>questions.add(new Question(
    "Какой язык программирования используется для Android?",
    new String[]{"Java", "Python", "C++", "Ruby"},
    1
));</pre>
      <li>Нажмите <strong>Submit new issue</strong>. Запомните номер задачи (например, #1).</li>
    </ul>
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong> Ветка — это ваш черновик, где вы добавите вопрос. Используйте команду <kbd>git checkout -b</kbd>, чтобы создать и переключиться на новую ветку.</li>
    <pre><kbd>git checkout -b question-alex</kbd></pre>
    <p>Замените <code>alex</code> на своё имя. Теперь вы работаете в ветке <code>question-alex</code>, а основная ветка <code>main</code> остаётся нетронутой.</p>
    <li><i class="fas fa-file-alt step-icon"></i> <strong>Откройте <code>Quiz.java</code>:</strong> Найдите файл <code>Quiz.java</code> в папке <code>team-quiz</code>. Откройте его в редакторе кода (например, IntelliJ IDEA или Notepad++). Изначально он выглядит так:</li>

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

<p>Этот код — основа викторины. В конструкторе <code>public Quiz()</code> вы добавите свой вопрос.</p>
    <li><i class="fas fa-plus-circle step-icon"></i> <strong>Добавьте вопрос:</strong> В конструкторе <code>public Quiz()</code> вставьте код для вашего вопроса. Например, Alex добавляет:</li>
    <pre>questions.add(new Question(
    "Какой язык программирования используется для Android?",
    new String[]{"Java", "Python", "C++", "Ruby"},
    1
));</pre>
    <p>После добавления ваш <code>Quiz.java</code> будет выглядеть так:</p>
    <pre>import java.util.ArrayList;

public class Quiz {
    private ArrayList<Question> questions = new ArrayList<>();
    private int score = 0;

    public Quiz() {
        // Здесь добавляем вопросы
        questions.add(new Question(
            "Какой язык программирования используется для Android?",
            new String[]{"Java", "Python", "C++", "Ruby"},
            1
        ));
    }

    public ArrayList<Question> getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</pre>
    <p><strong>Что делает этот код:</strong></p>
    <ul>
      <li><code>questions.add</code> — добавляет ваш вопрос в список вопросов викторины.</li>
      <li><code>new Question</code> — создаёт вопрос с текстом, четырьмя вариантами ответа и правильным ответом (1 — «Java»).</li>
    </ul>
    <p>Этот формат важен, чтобы викторина могла показать ваш вопрос игрокам.</p>
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните изменения:</strong> Скажите Git, что вы хотите сохранить файл <code>Quiz.java</code>, с помощью команды <kbd>git add</kbd>.</li>
    <pre><kbd>git add Quiz.java</kbd></pre>
    <li><i class="fas fa-comment step-icon"></i> <strong>Опишите изменения:</strong> Запишите, что вы сделали, с помощью команды <kbd>git commit</kbd>. Это как заметка для истории изменений.</li>
    <pre><kbd>git commit -m "Added question about Android programming language by Alex"</kbd></pre>
    <p>Сообщение в кавычках объясняет, что вы добавили (например, «Добавил вопрос про язык программирования для Android»).</p>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте изменения на GitHub:</strong> Загрузите вашу ветку <code>question-alex</code> на GitHub с помощью команды <kbd>git push</kbd>.</li>
    <pre><kbd>git push origin question-alex</kbd></pre>
    <p>Это как отправить ваш черновик на сервер, чтобы другие могли его увидеть.</p>
    <li><i class="fas fa-code-pull-request step-icon"></i> <strong>Создайте пул-реквест:</strong> Пул-реквест — это ваш запрос, чтобы учитель проверил и добавил ваш вопрос в викторину.</li>
    <ul>
      <li>Зайдите на GitHub в репозиторий <code>JavaTeam/team-quiz</code>.</li>
      <li>Вы увидите уведомление о ветке <code>question-alex</code> (например, «Recently pushed branches»).</li>
      <li>Нажмите зелёную кнопку <strong>Create Pull Request</strong>.</li>
      <li>В заголовке напишите: «Добавил вопрос про Android от Alex».</li>
      <li>В описании укажите номер задачи (например, «Закрывает #1») и добавьте: «Пожалуйста, проверьте мой вопрос».</li>
      <li>Нажмите <strong>Create Pull Request</strong>.</li>
    </ul>
    <li><i class="fas fa-hourglass-half step-icon"></i> <strong>Дождитесь проверки:</strong> Учитель проверит ваш пул-реквест. Если всё правильно, он добавит ваш вопрос в основную версию викторины. Если нужны правки, смотрите следующий раздел.</li>
  </ol>
  <p><strong>Пример:</strong> Alex создал задачу #1, ветку <code>question-alex</code>, добавил вопрос про Android, отправил изменения и создал пул-реквест. Maria сделала то же самое в ветке <code>question-maria</code>. Вместе вы создаёте викторину!</p>
  <p style="font-style:italic; color:#333;">Ваш вопрос делает викторину уникальной! 🌟</p>

  <h2 style="font-size:2rem;"><i class="fas fa-tasks step-icon"></i> Отслеживание вопросов с GitHub Projects</h2>
  <p>GitHub Projects — это как доска объявлений, где видно, кто какие вопросы добавляет. Она делит задачи на три группы: To Do (надо сделать), In Progress (в работе), Done (готово).</p>
  <p><strong>Почему это важно?</strong> Доска помогает следить за прогрессом всех 13 участников, чтобы никто не забыл добавить свой вопрос.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul>
    <li><i class="fas fa-ticket-alt"></i> Каждая задача (issue) — это один вопрос.</li>
    <li><i class="fas fa-arrows-alt"></i> Задачи перемещаются по колонкам, когда вы начинаете или заканчиваете работу.</li>
    <li><i class="fas fa-clipboard"></i> Доска находится в разделе <strong>Projects</strong> на GitHub.</li>
  </ul>
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-clipboard step-icon"></i> <strong>Создайте доску:</strong> В репозитории <code>JavaTeam/team-quiz</code> зайдите в <strong>Projects</strong> и создайте новый проект с названием «Quiz Board».</li>
    <li><i class="fas fa-columns step-icon"></i> <strong>Добавьте колонки:</strong> Создайте три колонки: To Do, In Progress, Done.</li>
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачи:</strong> В разделе <strong>Issues</strong> создайте 13 задач (по одной для каждого участника). Например, «Добавить вопрос от Alex» (#1). Перетащите каждую задачу в колонку To Do.</li>
    <li><i class="fas fa-arrows-alt step-icon"></i> <strong>Обновляйте доску:</strong> Когда вы создаёте ветку <code>question-alex</code>, переместите задачу #1 в In Progress. Когда ваш пул-реквест одобрен, переместите её в Done.</li>
  </ol>
  <p><strong>Пример:</strong> Задача #1 («Добавить вопрос от Alex») в To Do. Alex создал ветку <code>question-alex</code>, и задача переместилась в In Progress. После одобрения пул-реквеста она в Done. Доска выглядит так: <code>[To Do] → [In Progress] → [Done]</code>.</p>
  <p style="font-style:italic; color:#333;">Доска помогает нам не запутаться! 📅</p>

  <h2 style="font-size:2rem;"><i class="fas fa-search step-icon"></i> Проверка вашего вопроса</h2>
  <p>Ваш пул-реквест — это как письмо учителю: «Пожалуйста, проверьте мой вопрос в <code>Quiz.java</code>!». Учитель убедится, что вопрос понятный и правильный.</p>
  <p><strong>Почему это важно?</strong> Проверка гарантирует, что все вопросы в викторине качественные и без ошибок.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul>
    <li><i class="fas fa-check"></i> Учитель проверит, что у вопроса есть текст, 4 варианта ответа и правильный ответ (1–4).</li>
    <li><i class="fas fa-edit"></i> Если нужно что-то исправить, вы добавите изменения в ту же ветку.</li>
    <li><i class="fas fa-thumbs-up"></i> Одобренный пул-реквест означает, что ваш вопрос добавлен в викторину!</li>
  </ul>
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-eye step-icon"></i> <strong>Проверьте пул-реквест:</strong> Зайдите в ваш пул-реквест на GitHub (вкладка <strong>Pull Requests</strong>). Учитель оставит комментарии в разделах <strong>Conversation</strong> или <strong>Files changed</strong>.</li>
    <li><i class="fas fa-edit step-icon"></i> <strong>Исправьте, если нужно:</strong> Если учитель попросит изменить вопрос, откройте <code>Quiz.java</code> и обновите код. Например, уточните формулировку:</li>
    <pre>questions.add(new Question(
    "Какой язык программирования чаще всего используется для Android?",
    new String[]{"Java", "Python", "C++", "Ruby"},
    1
));</pre>
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните исправления:</strong> Сохраните изменения в Git.</li>
    <pre><kbd>git add Quiz.java</kbd></pre>
    <pre><kbd>git commit -m "Updated question wording as requested"</kbd></pre>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте исправления:</strong> Загрузите обновления в ту же ветку.</li>
    <pre><kbd>git push origin question-alex</kbd></pre>
    <p>Ваш пул-реквест автоматически обновится, и учитель увидит новые изменения.</p>
    <li><i class="fas fa-check-circle step-icon"></i> <strong>Дождитесь одобрения:</strong> Когда учитель одобрит пул-реквест, он сольёт его в основную ветку <code>main</code>. Ваш вопрос теперь часть викторины!</li>
  </ol>
  <p><strong>Пример:</strong> Учитель попросил Alex уточнить вопрос, добавив «чаще всего». Alex исправил <code>Quiz.java</code>, отправил изменения, и после проверки его вопрос добавили в викторину.</p>
  <p style="font-style:italic; color:#333;">Проверка делает нашу викторину лучше! 🔍</p>

  <h2 style="font-size:2rem;"><i class="fas fa-play step-icon"></i> Запуск викторины</h2>
  <p>Когда все 13 участников добавят свои вопросы, вы сможете запустить викторину и ответить на них!</p>
  <p><strong>Почему это важно?</strong> Запуск показывает, как работает ваша викторина, и вы увидите, как выглядят все вопросы команды.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul>
    <li><i class="fas fa-gamepad"></i> Файл <code>Main.java</code> показывает вопросы, принимает ответы (1–4) и считает очки.</li>
    <li><i class="fas fa-cogs"></i> Команды <kbd>javac</kbd> и <kbd>java</kbd> нужны, чтобы скомпилировать и запустить программу.</li>
    <li><i class="fas fa-book"></i> Файл <code>README.md</code> объясняет, как запустить викторину.</li>
  </ul>
  <h3>Как это сделать</h3>
  <ol>
    <li><i class="fas fa-check step-icon"></i> <strong>Проверьте, что все вопросы добавлены:</strong> Зайдите на GitHub и убедитесь, что все 13 пул-реквестов слиты в ветку <code>main</code>.</li>
    <li><i class="fas fa-sync step-icon"></i> <strong>Обновите проект:</strong> Переключитесь на ветку <code>main</code> и скачайте последние изменения.</li>
    <pre><kbd>git checkout main</kbd></pre>
    <pre><kbd>git pull origin main</kbd></pre>
    <p>Команда <kbd>git checkout main</kbd> возвращает вас в основную ветку, а <kbd>git pull</kbd> загружает все вопросы команды.</p>
    <li><i class="fas fa-cogs step-icon"></i> <strong>Скомпилируйте программу:</strong> Используйте команду <kbd>javac</kbd>, чтобы превратить Java-файлы в исполняемую программу.</li>
    <pre><kbd>javac Question.java Quiz.java Main.java</kbd></pre>
    <li><i class="fas fa-rocket step-icon"></i> <strong>Запустите викторину:</strong> Запустите программу командой <kbd>java</kbd>.</li>
    <pre><kbd>java Main</kbd></pre>
    <p>Вы увидите вопросы, выберете ответы (1–4), и программа покажет ваш результат. Например:</p>
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
  <p><strong>Пример:</strong> Вы запустили <kbd>java Main</kbd>, увидели вопрос про Android, выбрали 1 и получили сообщение <samp>Правильно!</samp>. В конце вы узнали свой счёт. Это ваша командная викторина!</p>
  <p style="font-style:italic; color:#333;">Викторина — наш общий успех! 🎉</p>

  <h2 style="font-size:2rem;"><i class="fas fa-exclamation-triangle step-icon"></i> Частые ошибки и как их исправить</h2>
  <p>Новички могут столкнуться с трудностями. Вот несколько типичных ошибок и способы их решения:</p>
  <ul>
    <li><i class="fas fa-bug step-icon"></i> <strong>Ошибка в вопросе:</strong> Если викторина не запускается, проверьте <code>Quiz.java</code>. Убедитесь, что:
      <ul>
        <li>Нет пропущенных запятых или кавычек в коде вопроса.</li>
        <li>Правильный ответ — число от 1 до 4.</li>
        <li>Вариантов ответа ровно 4.</li>
      </ul>
    </li>
    <li><i class="fas fa-upload step-icon"></i> <strong>Не получается отправить изменения:</strong> Если <kbd>git push</kbd> выдаёт ошибку, проверьте:
      <ul>
        <li>Вы в правильной ветке: <kbd>git branch</kbd> покажет текущую ветку (должна быть <code>question-<ваше_имя></code>).</li>
        <li>Используйте правильную команду: <kbd>git push origin question-<ваше_имя></kbd>.</li>
      </ul>
    </li>
    <li><i class="fas fa-conflict step-icon"></i> <strong>Конфликт в <code>Quiz.java</code>:</strong> Если кто-то добавил вопрос в ту же строку, выполните:
      <ul>
        <li><kbd>git pull origin main</kbd> — скачайте последние изменения.</li>
        <li>Откройте <code>Quiz.java</code>, разрешите конфликт (оставьте оба вопроса).</li>
        <li>Сохраните: <kbd>git add Quiz.java</kbd>, <kbd>git commit</kbd>, <kbd>git push</kbd>.</li>
      </ul>
    </li>
    <li><i class="fas fa-times-circle step-icon"></i> <strong>Пул-реквест не создаётся:</strong> Убедитесь, что вы отправили ветку на GitHub (<kbd>git push</kbd>) и видите её в репозитории.</li>
    <li><i class="fas fa-terminal step-icon"></i> <strong>Ошибка компиляции:</strong> Если <kbd>javac</kbd> выдаёт ошибку, проверьте:
      <ul>
        <li>Вы в папке <code>team-quiz</code> (введите <kbd>pwd</kbd> или <kbd>dir</kbd>).</li>
        <li>Все файлы на месте: <code>Question.java</code>, <code>Quiz.java</code>, <code>Main.java</code>.</li>
      </ul>
    </li>
  </ul>
  <p><strong>Совет:</strong> Если что-то не работает, напишите учителю или создайте новую задачу в <strong>Issues</strong> на GitHub. Опишите, что пошло не так, и вам помогут!</p>
  <p style="font-style:italic; color:#333;">Ошибки — это часть обучения! 🛠️</p>
</div>

<div style="text-align:center; margin: 3rem 0;">
  <a href="https://github.com/JavaTeam/team-quiz" class="btn">Посмотреть репозиторий</a>
</div>

<nav style="display:flex; justify-content:space-between; margin:3rem 0;">
  <a href="{{ '/lessons/05-pull-requests/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.4rem;" aria-label="Предыдущий урок: Пул-реквесты">← Назад</a>
  <a href="{{ '/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.4rem;" aria-label="Главная страница">Оглавление</a>
  <a href="{{ '/lessons/07-faq/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.4rem;" aria-label="Следующий урок: Вопросы и итоги">Далее →</a>
</nav>