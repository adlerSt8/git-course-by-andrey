---
layout: default
title: Пул-реквесты и совместная работа
permalink: /lessons/05-pull-requests/
nav_order: 5
---

<div class="lesson-content">
  <h1>Пул-реквесты и совместная работа</h1>
  <p>В этом уроке вы научитесь работать с пул-реквестами, проводить код-ревью и объединять ветки в вашем проекте.</p>

  <h2 style="font-size:1.8rem;">🎯 Цель урока</h2>
  <p>Научиться предлагать изменения через пул-реквест, проводить ревью и объединять ветки.</p>

  <h2 style="font-size:1.8rem;">📝 Шаги</h2>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li><strong>Создание пул-реквеста:</strong>
      <ul style="padding-left:1.5rem; margin:0.5rem 0;">
        <li>В репозитории <code>java-team-project</code> перейдите во вкладку <strong>Pull requests</strong>.</li>
        <li>Нажмите <strong>New pull request</strong>.</li>
        <li>В поле <strong>base:</strong> выберите <code>main</code>, а <strong>compare:</strong> — вашу ветку <code>add-feature</code>.</li>
        <li>Нажмите <strong>Create pull request</strong>.</li>
        <li>Задайте название (например, «Добавлен метод приветствия») и описание изменений.</li>
        <li>Нажмите <strong>Create pull request</strong>.</li>
      </ul>
    </li>

    <li><strong>Просмотр и ревью изменений:</strong>
      <ul style="padding-left:1.5rem; margin:0.5rem 0;">
        <li>Откройте вкладку <strong>Files changed</strong> в пул-реквесте.</li>
        <li>Изучите, какие строки кода были добавлены или изменены.</li>
        <li>Добавьте комментарий к строке: нажмите на «+» рядом с изменением и оставьте замечание или вопрос.</li>
      </ul>
    </li>

    <li><strong>Слияние пул-реквеста:</strong>
      <ul style="padding-left:1.5rem; margin:0.5rem 0;">
        <li>Когда ревью завершено и правки приняты, нажмите <strong>Merge pull request</strong>.</li>
        <li>Подтвердите слияние кнопкой <strong>Confirm merge</strong>.</li>
        <li>После этого нажмите <strong>Delete branch</strong>, чтобы убрать уже не нужную <code>add-feature</code>.</li>
      </ul>
    </li>
  </ol>

  <h2 style="font-size:1.8rem;">💡 Пример</h2>
  <p>1. Я открыл PR «Добавлен метод приветствия», где в <strong>Files changed</strong> увидел новый метод <code>sayWelcome()</code>.</p>
  <p>2. Я добавил комментарий: «Можно ли описать, что делает параметр?». </p>
  <p>3. После исправлений я нажал <strong>Merge pull request</strong>, и метод попал в <code>main</code>.</p>
  <p>4. Удалил ветку <code>add-feature</code> кнопкой <strong>Delete branch</strong>.</p>

  <h2 style="font-size:1.8rem;">🔍 Объяснение</h2>
  <p><strong>Пул-реквест</strong> — это запрос на включение ваших изменений в основную ветку. Он позволяет команде обсудить изменения, предложить улучшения и решить возможные проблемы до того, как код попадёт в основную ветку проекта.</p>
  <p><strong>Ревью</strong> — это процесс, когда коллеги просматривают ваш код, ищут ошибки или предлагают улучшения, чтобы код стал более качественным.</p>
  <p><strong>Merge</strong> — это операция объединения веток. Когда все изменения одобрены, вы сливаете ветку с <code>main</code>, и изменения становятся частью основного проекта.</p>
  <p><strong>Удаление ветки</strong> помогает поддерживать порядок в репозитории и избежать избыточных веток после слияния.</p>

  <h2 style="font-size:1.8rem;">📝 Задание</h2>
  <ol style="padding-left:1.5rem; margin:0.5rem 0;">
    <li>Создайте пул-реквест из <code>add-feature</code> в <code>main</code>.</li>
    <li>Добавьте комментарий к изменению (например, вопрос о стиле кода).</li>
    <li>Попросите однокурсника или преподавателя провести ревью (в чате пришлите ссылку на PR).</li>
    <li>После одобрения выполните <strong>Merge pull request</strong> и удалите ветку.</li>
    <li>В чате напишите, какие замечания вам дали и как вы их исправили.</li>
  </ol>
</div>

<div class="lesson-nav">
  {% if page.previous %}
    <a href="{{ page.previous.url }}">← Назад</a>
  {% endif %}
  
  {% if page.next %}
    <a href="{{ page.next.url }}">Вперёд →</a>
  {% endif %}
</div>
