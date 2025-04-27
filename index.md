---
layout: default
title: Главная
permalink: /
---

<div style="text-align:center; margin: 2rem 0;">
  <h1 style="font-size:2.5rem;">🚀 {{ site.title }}</h1>
  <p style="font-size:1.2rem; color:#555;">{{ site.description }}</p>
</div>

<nav>
  <ul style="list-style:none; padding:0; display:grid; grid-template-columns:repeat(auto-fit, minmax(250px, 1fr)); gap:1rem;">
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/01-intro/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">📘</span>
        <strong>1. Введение в GitHub</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/02-signup/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">📝</span>
        <strong>2. Регистрация и настройка</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/03-create-repo/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">📂</span>
        <strong>3. Создание репозитория</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/04-branches/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">🌿</span>
        <strong>4. Работа с ветками</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/05-pull-requests/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">🔀</span>
        <strong>5. Пул-реквесты</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/06-team-project/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">🤝</span>
        <strong>6. Командный проект</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/07-faq/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">❓</span>
        <strong>7. Вопросы и итоги</strong>
      </a>
    </li>
    <li style="background:#f8f9fa; border-radius:8px; padding:1rem; box-shadow:0 2px 4px rgba(0,0,0,0.1);">
      <a href="{{ site.baseurl }}/lessons/08-github-desktop/" style="text-decoration:none; color:#333;">
        <span style="font-size:1.5rem;">💻</span>
        <strong>8. GitHub Desktop</strong>
      </a>
    </li>
  </ul>
</nav>

<footer style="text-align:center; margin:2rem 0; color:#777; font-size:0.9rem;">
  © {{ site.time | date: "%Y" }} {{ site.title }}. Курс открыт для всех.
</footer>
