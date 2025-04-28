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
    <pre><code>git checkout -b feature-login</code></pre>
    <li>Внесите изменения, например, в <code>AuthController.java</code>, и зафиксируйте:</li>
    <pre><code>git add AuthController.java</code></pre>
    <pre><code>git commit -m "Added login endpoint"</code></pre>
    <li>Отправьте ветку на GitHub:</li>
    <pre><code>git push origin feature-login</code></pre>
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
    <pre><code>git add AuthController.java</code></pre>
    <pre><code>git commit -m "Added exception handling"</code></pre>
    <pre><code>git push origin feature-login</code></pre>
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
    <li>При создании PR автоматически запускаются тесты (например, unit-тесты) через конфигурацию в файле <code>.github/workflows</code>.</li>
  </ul>
  <p><strong>Шаги:</strong></p>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте файл конфигурации CI в директории <code>.github/workflows</code>:</li>
    <pre><code>name: CI</code></pre>
    <pre><code>on: [push, pull_request]</code></pre>
    <pre><code>jobs:
      test:
        runs-on: ubuntu-latest
        steps:
          - uses: actions/checkout@v2
          - name: Set up JDK
            uses: actions/setup-java@v2
            with:
              java-version: '11'
          - name: Run tests
            run: mvn test</code></pre>
    <li>После пуша изменений или PR GitHub автоматически запустит тесты.</li>
  </ol>
  <p><strong>Пример:</strong> Вы добавили тесты для нового метода в <code>AuthController.java</code>. После отправки PR, GitHub Actions запускает тесты и сообщает, если что-то пошло не так. Это поможет избежать багов в продакшене.</p>
</div>

<p style="text-align:center; font-size: 1.2rem; color:#555;">🚀 <strong>Вы теперь знаете, как работать с пул-реквестами!</strong> Продолжайте использовать их для улучшения качества вашего кода и сотрудничества с коллегами.</p>
