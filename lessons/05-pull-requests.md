---
layout: default
title: Пул-реквесты и совместная работа
permalink: /lessons/05-pull-requests/
nav_order: 5
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
  <h1 style="font-size:2.8rem;">🤝 Пул-реквесты и совместная работа</h1>
  <p style="color:#555; font-size:1.3rem;">Создаём пул-реквесты, проводим код-ревью и работаем в команде</p>
</div>

<div style="background:#f8f9fa; border-radius:8px; padding:2rem; box-shadow:0 2px 4px rgba(0,0,0,0.1); margin:2rem 0; line-height:1.8; font-size:1.1rem;">
  <h2 style="font-size:1.8rem;">📬 Что такое пул-реквест?</h2>
  <p>Пул-реквест (PR) — это механизм GitHub для предложения изменений из одной ветки в другую, обычно из ветки с новой функцией в <code>main</code>. PR позволяет команде обсудить, проверить и одобрить изменения перед слиянием.</p>
  <p><strong>Зачем это нужно?</strong> Пул-реквесты критично важны для Java-разработчиков в командной работе, так как они обеспечивают код-ревью, предотвращают ошибки и поддерживают качество кода, например, в классах вроде <code>Service.java</code>.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>PR включает изменения, комментарии, историю коммитов и результаты автоматических тестов.</li>
    <li>GitHub позволяет назначать ревьюеров и добавлять метки для организации.</li>
    <li>PR можно связать с задачами (issues) для отслеживания.</li>
  </ul>
  <p><strong>Пример:</strong> Вы разработали новую функцию в ветке <code>feature-login</code>, изменив <code>AuthController.java</code>. Создав PR, вы приглашаете коллег проверить код. После одобрения изменения сливаются в <code>main</code>, и новая функция становится частью проекта.</p>
  <p style="font-style:italic; color:#555;">Пул-реквесты — ваш мост к совместной разработке!</p>

  <h2 style="font-size:1.8rem;">🌟 Создание пул-реквеста</h2>
  <p>Создание PR начинается с отправки изменений в ветку на GitHub и предложения их для слияния через веб-интерфейс.</p>
  <p><strong>Зачем это нужно?</strong> PR позволяет Java-разработчикам формализовать процесс интеграции кода, например, нового REST-эндпоинта, и получить обратную связь перед включением в проект.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Ветка с изменениями должна быть отправлена на GitHub с помощью <code>git push</code>.</li>
    <li>PR создаётся в веб-интерфейсе GitHub, где указывается целевая ветка (обычно <code>main</code>).</li>
    <li>Описание PR должно быть понятным, с указанием цели изменений.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте и переключитесь на ветку <code>feature-login</code>:</li>
    ```
    <pre><code>git checkout -b feature-login</code></pre>
    ```
    <li>Внесите изменения, например, в <code>AuthController.java</code>, и зафиксируйте:</li>
    ```
    <pre><code>git add AuthController.java</code></pre>
    <pre><code>git commit -m "Added login endpoint"</code></pre>
    ```
    <li>Отправьте ветку на GitHub:</li>
    ```
    <pre><code>git push origin feature-login</code></pre>
    ```
    <li>Перейдите на <a href="https://github.com" style="color:#007bff; text-decoration:none;">GitHub</a>, в ваш репозиторий. Нажмите <strong>Compare & pull request</strong> для ветки <code>feature-login</code>.</li>
    <li>Заполните заголовок (например, "Add login endpoint") и описание, затем нажмите <strong>Create pull request</strong>.</li>
  </ol>
  <p><strong>Пример:</strong> Вы добавили эндпоинт в <code>AuthController.java</code> в ветке <code>feature-login</code> репозитория <code>JavaDev/my-first-repo</code>. После <code>git push</code> вы создали PR на GitHub, описав изменения: "Добавлен эндпоинт /login для аутентификации". PR готов для ревью.</p>
  <p style="font-style:italic; color:#555;">Создание PR запускает обсуждение вашего кода!</p>

  <h2 style="font-size:1.8rem;">🔍 Код-ревью в пул-реквесте</h2>
  <p>Код-ревью — это процесс проверки кода в PR, где команда комментирует, предлагает улучшения и одобряет изменения.</p>
  <p><strong>Зачем это нужно?</strong> Код-ревью повышает качество Java-кода, помогая находить баги, улучшать читаемость и соответствовать стандартам, например, в классах Spring.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Ревьюеры добавляют комментарии к конкретным строкам кода в PR.</li>
    <li>GitHub показывает различия (diff) между версиями файлов.</li>
    <li>После исправлений PR обновляется новыми коммитами.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Откройте PR на GitHub и назначьте ревьюеров в разделе <strong>Reviewers</strong>.</li>
    <li>Ревьюер проверяет изменения, например, в <code>AuthController.java</code>, и оставляет комментарий: "Добавить обработку исключений".</li>
    <li>Внесите исправления локально:</li>
    ```
    <pre><code>git add AuthController.java</code></pre>
    <pre><code>git commit -m "Added exception handling"</code></pre>
    <pre><code>git push origin feature-login</code></pre>
    ```
    <li>PR автоматически обновится с новыми изменениями.</li>
    <li>После одобрения ревьюером нажмите <strong>Merge pull request</strong> на GitHub.</li>
  </ol>
  <p><strong>Пример:</strong> Ваш PR для <code>feature-login</code> получил комментарий о необходимости try-catch в <code>AuthController.java</code>. Вы добавили обработку исключений, отправили изменения, и ревьюер одобрил PR. После слияния эндпоинт доступен в <code>main</code>.</p>
  <p style="font-style:italic; color:#555;">Код-ревью делает ваш код надёжным!</p>

  <h2 style="font-size:1.8rem;">🛠 Интеграция с CI/CD</h2>
  <p>Пул-реквесты часто интегрируются с CI/CD (непрерывная интеграция/доставка), чтобы автоматически тестировать и деплоить код.</p>
  <p><strong>Зачем это нужно?</strong> CI/CD автоматизирует проверку Java-проектов, запуская тесты (например, с Maven) при каждом PR, что снижает риск ошибок в продакшене.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>GitHub Actions — популярный инструмент для CI/CD, встроенный в GitHub.</li>
    <li>CI/CD проверяет PR перед слиянием, показывая статус тестов (pass/fail).</li>
    <li>Конфигурация CI/CD хранится в файле <code>.github/workflows/ci.yml</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте файл <code>.github/workflows/ci.yml</code> в репозитории:</li>
    ```
    <pre><code>name: CI
on: [push, pull_request]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v3
    - name: Set up JDK 17
      uses: actions/setup-java@v3
      with:
        java-version: '17'
    - name: Run tests
      run: mvn test</code></pre>
    ```
    <li>Отправьте изменения:</li>
    ```
    <pre><code>git add .github/workflows/ci.yml</code></pre>
    <pre><code>git commit -m "Added CI workflow"</code></pre>
    <pre><code>git push origin feature-login</code></pre>
    ```
    <li>Проверьте статус тестов в PR на GitHub (вкладка <strong>Checks</strong>).</li>
  </ol>
  <p><strong>Пример:</strong> Ваш PR для <code>feature-login</code> включает <code>AuthController.java</code>. GitHub Actions запускает <code>mvn test</code>, и статус "Passed" подтверждает, что тесты успешны. Если тесты не проходят, вы исправляете <code>AuthControllerTest.java</code> и обновляете PR.</p>
  <p style="font-style:italic; color:#555;">CI/CD автоматизирует проверку качества!</p>

  <h2 style="font-size:1.8rem;">🔐 Управление доступом в команде</h2>
  <p>GitHub позволяет управлять доступом к репозиторию, назначая роли (владелец, участник, ревьюер) и защищая ветки.</p>
  <p><strong>Зачем это нужно?</strong> В Java-проектах управление доступом предотвращает несанкционированные изменения в критических файлах, таких как <code>pom.xml</code>, и обеспечивает контроль качества.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Настройки доступа находятся в разделе <strong>Settings > Collaborators</strong> репозитория.</li>
    <li>Защита веток (branch protection) требует одобрения PR перед слиянием.</li>
    <li>Роли определяют, кто может пушить, сливать или администрировать.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Перейдите в <strong>Settings > Collaborators</strong> и добавьте коллег по их GitHub-именам.</li>
    <li>Настройте защиту ветки <code>main</code> в <strong>Settings > Branches > Branch protection rules</strong>:
      <ul style="padding-left:1.5rem;">
        <li>Включите <strong>Require pull request reviews before merging</strong>.</li>
        <li>Включите <strong>Require status checks to pass</strong> для CI/CD.</li>
      </ul>
    </li>
    <li>Проверьте, что PR для <code>main</code> требует одобрения.</li>
  </ol>
  <p><strong>Пример:</strong> Вы добавили коллегу как участника в <code>JavaDev/my-first-repo</code> и защитили ветку <code>main</code>. Теперь PR для <code>AuthController.java</code> требует минимум одного одобрения и успешных тестов, что гарантирует качество.</p>
  <p style="font-style:italic; color:#555;">Управление доступом защищает ваш проект!</p>

  <h2 style="font-size:1.8rem;">👥 Совместная работа в команде</h2>
  <p>Совместная работа в GitHub включает координацию через PR, issues, обсуждения и интеграцию с инструментами, такими как Slack или Jira.</p>
  <p><strong>Зачем это нужно?</strong> Для Java-разработчиков командная работа через GitHub упрощает управление задачами, такими как разработка API или рефакторинг, и повышает прозрачность.</p>
  <p><strong>Подробности:</strong></p>
  <ul style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Issues в GitHub помогают отслеживать задачи и баги.</li>
    <li>Комментарии в PR и issues обеспечивают коммуникацию.</li>
    <li>Интеграции уведомляют команду о новых PR или изменениях.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте issue в репозитории для задачи, например, "Добавить эндпоинт /logout".</li>
    <li>Создайте ветку <code>feature-logout</code> и PR, связав его с issue:</li>
    ```
    <pre><code>git checkout -b feature-logout</code></pre>
    <pre><code>git add LogoutController.java</code></pre>
    <pre><code>git commit -m "Added logout endpoint"</code></pre>
    <pre><code>git push origin feature-logout</code></pre>
    ```
    <li>В PR укажите связь с issue, добавив "#номер_issue" в описание.</li>
    <li>Обсудите изменения в PR, используя комментарии.</li>
  </ol>
  <p><strong>Пример:</strong> Ваша команда работает над <code>my-first-repo</code>. Вы создали issue #5 для эндпоинта /logout, затем ветку <code>feature-logout</code> с <code>LogoutController.java</code>. PR ссылается на #5, и после ревью изменения сливаются, а issue автоматически закрывается.</p>
  <p style="font-style:italic; color:#555;">Совместная работа делает команду эффективной!</p>
</div>

<div style="display:flex; justify-content:space-between; margin:2rem 0;">
  <a href="/lessons/04-branches/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">← Назад</a>
  <a href="/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Оглавление</a>
  <a href="/lessons/06-advanced-git/" style="text-decoration:none; color:#fff; background:#007bff; padding:0.8rem 1.5rem; border-radius:8px; font-size:1.1rem;">Далее →</a>
</div>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  Сделано с любовью ❤️
</footer>