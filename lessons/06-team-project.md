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
    <li><i class="fas fa-code-branch step-icon"></i> <strong>Создайте ветку:</strong> Команда <kbd>git checkout -b</kbd> делает новую ветку и переключает вас на неё. Это ваш черновик для вопроса.</li>
    <pre>git checkout -b question-alex</pre>
    <p>Замените <code>alex</code> на своё имя. Теперь вы работаете в ветке <code>question-alex</code>, не трогая главную ветку <code>main</code>.</p>
    <li><i class="fas fa-file-alt step-icon"></i> <strong>Откройте <code>Quiz.java</code>:</strong> Найдите файл в папке <code>team-quiz</code>. Изначально он выглядит так:</li>
    <pre>import java.util.ArrayList;

public class Quiz {
    private ArrayList<Question> questions = new ArrayList<>();
    private int score = 0;

    public Quiz() {
        // Здесь добавляем вопросы
    }

    public ArrayList<Question> getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</pre>
    <p>Этот код — основа викторины. В конструкторе <code>public Quiz()</code> вы добавите свой вопрос.</p>
    <li><i class="fas fa-plus-circle step-icon"></i> <strong>Добавьте вопрос:</strong> В конструкторе <code>public Quiz()</code> вставьте свой вопрос. Например, Alex добавляет:</li>
    <pre>questions.add(new Question(
    "Что такое JVM?",
    new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
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
            "Что такое JVM?",
            new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
            1
        ));
    }

    public ArrayList<Question> getQuestions() { return questions; }
    public int getScore() { return score; }
    public void incrementScore() { score++; }
}</pre>
    <p><strong>Что происходит:</strong></p>
    <ul style="padding-left:1.5rem;">
      <li><code>questions.add</code> — добавляет ваш вопрос в список викторины.</li>
      <li><code>new Question</code> — создаёт вопрос: текст, 4 варианта, правильный ответ (1 — "Виртуальная машина").</li>
    </ul>
    <p>Этот формат нужен, чтобы викторина показала ваш вопрос игрокам.</p>
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните изменения:</strong> Команда <kbd>git add</kbd> говорит Git: "Я хочу сохранить <code>Quiz.java</code>".</li>
    <pre>git add Quiz.java</pre>
    <li><i class="fas fa-comment step-icon"></i> <strong>Опишите изменения:</strong> Команда <kbd>git commit</kbd> сохраняет ваш вопрос с заметкой, что вы сделали.</li>
    <pre>git commit -m "Added question about JVM by Alex"</pre>
    <p>Это как написать: "Я добавил вопрос про JVM".</p>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте на GitHub:</strong> Команда <kbd>git push</kbd> загружает ветку <code>question-alex</code> на GitHub, чтобы другие её увидели.</li>
    <pre>git push origin question-alex</pre>
    <li><i class="fas fa-code-pull-request step-icon"></i> <strong>Создайте пул-реквест:</strong> На GitHub в <code>JavaTeam/team-quiz</code> появится уведомление о ветке <code>question-alex</code>. Нажмите <strong>Create Pull Request</strong>. В описании напишите: "Добавил вопрос про JVM, задача #1". Попросите учителя проверить.</li>
    <li><i class="fas fa-hourglass-half step-icon"></i> <strong>Дождитесь проверки:</strong> Учитель посмотрит ваш PR. Если всё хорошо, вопрос добавят в викторину. Если нужны правки, смотрите следующий раздел.</li>
  </ol>
  <p><strong>Пример:</strong> Alex создал ветку <code>question-alex</code>, добавил вопрос про JVM и отправил PR для задачи #1. Maria сделала ветку <code>question-maria</code> с вопросом про циклы. Вместе вы создаёте викторину!</p>
  <p style="font-style:italic; color:#555;">Ваш вопрос — часть нашей викторины! 🌟</p>

  <h2 style="font-size:1.8rem;"><i class="fas fa-tasks step-icon"></i> Отслеживание вопросов</h2>
  <p>GitHub Projects — это как доска, где видно, кто какие вопросы добавляет. Она делит задачи на три колонки: To Do (надо сделать), In Progress (в работе), Done (готово).</p>
  <p><strong>Почему это важно?</strong> Доска помогает следить, чтобы все 13 участников добавили свои вопросы.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>📌 Каждая задача (issue) — это один вопрос.</li>
    <li>➡️ Задачи перемещаются по колонкам, когда вы начинаете или заканчиваете работу.</li>
    <li>📊 Доска находится в разделе <strong>Projects</strong> репозитория.</li>
  </ul>
  <p><strong>Как это сделать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-clipboard step-icon"></i> <strong>Создайте доску:</strong> В <code>JavaTeam/team-quiz</code> в разделе <strong>Projects</strong> создайте проект "Quiz Board".</li>
    <li><i class="fas fa-columns step-icon"></i> <strong>Добавьте колонки:</strong> Создайте To Do, In Progress, Done.</li>
    <li><i class="fas fa-ticket-alt step-icon"></i> <strong>Создайте задачи:</strong> В <strong>Issues</strong> добавьте 13 задач, например, "Добавить вопрос от Alex" (#1), и переместите их в To Do.</li>
    <li><i class="fas fa-arrows-alt step-icon"></i> <strong>Обновляйте доску:</strong> Когда создаёте ветку <code>question-alex</code>, переместите задачу #1 в In Progress. После слияния PR — в Done.</li>
  </ol>
  <p><strong>Пример:</strong> Задача #1 для Alex в To Do. Он создал ветку <code>question-alex</code>, и задача переместилась в In Progress. После слияния PR она в Done, как на доске: <code>[To Do] → [In Progress] → [Done]</code>.</p>
  <p style="font-style:italic; color:#555;">Доска помогает нам работать вместе! 📅</p>

  <h2 style="font-size:1.8rem;"><i class="fas fa-search step-icon"></i> Проверка вопроса</h2>
  <p>Ваш пул-реквест (PR) — это как запрос: "Проверьте мой вопрос в <code>Quiz.java</code>!" Учитель или друг посмотрит, всё ли правильно.</p>
  <p><strong>Почему это важно?</strong> Проверка делает вопросы понятными и без ошибок, чтобы викторина была классной.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>✔️ Проверяют, что у вопроса 4 варианта и правильный ответ (1–4).</li>
    <li>📝 Если нужно исправить, вы добавите изменения в ту же ветку.</li>
    <li>🎉 Одобренный PR добавляет ваш вопрос в викторину.</li>
  </ul>
  <p><strong>Как это сделать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-eye step-icon"></i> <strong>Проверьте PR:</strong> В PR для <code>question-alex</code> учитель посмотрит ваш вопрос. Комментарии будут в разделе <strong>Conversation</strong> или <strong>Files changed</strong> на GitHub.</li>
    <li><i class="fas fa-edit step-icon"></i> <strong>Исправьте, если нужно:</strong> Если просят уточнить, откройте <code>Quiz.java</code> и измените вопрос, например:</li>
    <pre>questions.add(new Question(
    "Что такое Java Virtual Machine (JVM)?",
    new String[]{"Виртуальная машина", "Компилятор", "Библиотека", "Фреймворк"},
    1
));</pre>
    <li><i class="fas fa-save step-icon"></i> <strong>Сохраните исправления:</strong> Сохраните изменения в Git.</li>
    <pre>git add Quiz.java</pre>
    <pre>git commit -m "Updated question wording as requested"</pre>
    <li><i class="fas fa-upload step-icon"></i> <strong>Отправьте исправления:</strong> Обновите PR на GitHub.</li>
    <pre>git push origin question-alex</pre>
    <p>Ваш PR автоматически обновится, и учитель увидит правки.</p>
    <li><i class="fas fa-check-circle step-icon"></i> <strong>Дождитесь одобрения:</strong> Когда учитель скажет "Всё ок!", он сольёт ваш PR в <code>main</code>. Ваш вопрос теперь в викторине!</li>
  </ol>
  <p><strong>Пример:</strong> Учитель попросил Alex написать "Java Virtual Machine" вместо "JVM". Alex исправил <code>Quiz.java</code>, отправил изменения, и после проверки его вопрос добавили в викторину.</p>
  <p style="font-style:italic; color:#555;">Проверка делает викторину лучше! 🔍</p>

  <h2 style="font-size:1.8rem;"><i class="fas fa-play step-icon"></i> Запуск викторины</h2>
  <p>Когда все 13 вопросов добавлены, можно запустить викторину и ответить на них!</p>
  <p><strong>Почему это важно?</strong> Запуск показывает, как работает ваша викторина, и вы увидите все вопросы команды.</p>
  <p><strong>Что нужно знать:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>🎮 <code>Main.java</code> показывает вопросы, принимает ответы (1–4) и считает очки.</li>
    <li>🛠️ Команды <kbd>javac</kbd> и <kbd>java</kbd> компилируют и запускают программу.</li>
    <li>📖 <code>README.md</code> объясняет, как запустить викторину.</li>
  </ul>
  <p><strong>Как это сделать:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-check step-icon"></i> <strong>Проверьте, что всё готово:</strong> Убедитесь на GitHub, что все 13 PR слиты в <code>main</code>.</li>
    <li><i class="fas fa-sync step-icon"></i> <strong>Обновите проект:</strong> Переключитесь на <code>main</code> и скачайте все вопросы.</li>
    <pre>git checkout main</pre>
    <pre>git pull origin main</pre>
    <p>Команда <kbd>git checkout main</kbd> возвращает вас в главную ветку, а <kbd>git pull</kbd> загружает последние изменения.</p>
    <li><i class="fas fa-cogs step-icon"></i> <strong>Скомпилируйте:</strong> Команда <kbd>javac</kbd> превращает Java-файлы в программу.</li>
    <pre>javac Question.java Quiz.java Main.java</pre>
    <li><i class="fas fa-rocket step-icon"></i> <strong>Запустите:</strong> Команда <kbd>java</kbd> запускает викторину.</li>
    <pre>java Main</pre>
    <p>Вы увидите вопросы, выберете ответы (1–4), и программа покажет ваш счёт, например: <samp>Правильно! Счёт: 1</samp>.</p>
  </ol>
  <p><strong>Пример:</strong> Вы запустили <kbd>java Main</kbd>, увидели вопрос: "Что такое JVM?", выбрали 1 и получили <samp>Правильно!</samp>. В конце узнали счёт. Это ваша командная викторина!</p>
  <p style="font-style:italic; color:#555;">Викторина готова к игре! 🎉</p>

  <h2 style="font-size:1.8rem;"><i class="fas fa-exclamation-triangle step-icon"></i> Частые ошибки и как их исправить</h2>
  <p>Новички могут столкнуться с проблемами. Вот как их решить:</p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><i class="fas fa-bug step-icon"></i> <strong>Ошибка в вопросе:</strong> Если викторина не запускается, проверьте <code>Quiz.java</code>: нет ли пропущенных запятых, кавычек или неправильного номера ответа (должно быть 1–4).</li>
    <li><i class="fas fa-upload step-icon"></i> <strong>Не пушится ветка:</strong> Если <kbd>git push</kbd> выдаёт ошибку, убедитесь, что вы в ветке <code>question-<ваше_имя></code> (<kbd>git branch</kbd>) и используете <kbd>git push origin question-<ваше_имя></kbd>.</li>
    <li><i class="fas fa-conflict step-icon"></i> <strong>Конфликт в <code>Quiz.java</code>:</strong> Если кто-то уже добавил вопрос в ту же строку, выполните <kbd>git pull origin main</kbd>, разрешите конфликт в <code>Quiz.java</code> (оставьте оба вопроса) и снова сделайте <kbd>git push</kbd>.</li>
    <li><i class="fas fa-times-circle step-icon"></i> <strong>PR не создаётся:</strong> Убедитесь, что вы отправили ветку на GitHub (<kbd>git push</kbd>) и видите её в репозитории.</li>
    <li><i class="fas fa-terminal step-icon"></i> <strong>Ошибка компиляции:</strong> Если <kbd>javac</kbd> выдаёт ошибку, проверьте, что вы в папке <code>team-quiz</code> и все файлы (<code>Question.java</code>, <code>Quiz.java</code>, <code>Main.java</code>) на месте.</li>
  </ul>
  <p><strong>Совет:</strong> Если что-то не работает, напишите учителю или спросите в <strong>Issues</strong> на GitHub!</p>
  <p style="font-style:italic; color:#555;">Ошибки — это нормально, мы учимся! 🛠️</p>
</div>

<nav style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="{{ '/lessons/05-pull-requests/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;" aria-label="Предыдущий урок: Пул-реквесты">← Назад</a>
  <a href="{{ '/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;" aria-label="Главная страница">Оглавление</a>
  <a href="{{ '/lessons/07-faq/' | relative_url }}" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;" aria-label="Следующий урок: Вопросы и итоги">Далее →</a>
</nav>