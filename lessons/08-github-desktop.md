---
layout: default
title: Использование GitHub Desktop
permalink: /lessons/08-github-desktop/
nav_order: 8
---

## Цель урока

Научиться управлять репозиториями и изменениями локально через GitHub Desktop без командной строки.

## Шаги

1. **Установка GitHub Desktop**
   - Перейдите на https://desktop.github.com и скачайте версию для вашей ОС.  
   - Установите приложение, следуя инструкциям установщика.

2. **Авторизация**
   - Запустите GitHub Desktop и выберите **Sign in to GitHub.com**.  
   - Войдите через браузер в свой аккаунт GitHub, подтвердите авторизацию.

3. **Клонирование репозитория**
   - В меню **File → Clone repository…** откроется список ваших репозиториев.  
   - Выберите `java-team-project` и нажмите **Clone**.  
   - Дождитесь, пока репозиторий загрузится локально.

4. **Внесение изменений и коммиты**
   - Откройте папку проекта в вашей IDE (например, IntelliJ IDEA).  
   - Измените файл `HelloWorld.java` или добавьте новый файл `Welcome.java`.  
   - В GitHub Desktop вы увидите раздел **Changes** с изменёнными файлами.  
   - В поле **Summary** напишите краткое сообщение (например, `Добавлен класс Welcome`).  
   - Нажмите **Commit to main**.

5. **Отправка на GitHub (Push)**
   - Нажмите кнопку **Push origin** в верхней панели GitHub Desktop.  
   - Убедитесь, что изменения появились на GitHub в разделе **Commits** вашего репозитория.

6. **Работа с ветками**
   - В верхней панели нажмите текущее имя ветки (обычно `main`).  
   - Выберите **New branch**, назовите ветку `desktop-feature` и нажмите **Create**.  
   - Сделайте изменения и коммит в этой ветке, затем нажмите **Publish branch**.

7. **Создание пул-реквеста**
   - Нажмите **Create Pull Request** рядом с недавно опубликованной веткой.  
   - Это откроет окно в браузере с формой PR: проверьте `base: main`, `compare: desktop-feature`.  
   - Укажите название и описание PR, нажмите **Create pull request**.

## Объяснение

- GitHub Desktop упрощает базовые операции Git: клонирование, коммиты, push/pull, ветвление и PR через GUI.  
- **Commit** в Desktop аналогичен `git commit` в терминале: фиксирует изменения в локальной ветке.  
- **Push** отправляет локальные коммиты в удалённый репозиторий на GitHub.  
- Создание ветки и PR через Desktop помогает быстро переключаться между задачами и инициировать код-ревью.

## Пример

1. Я клонировал `java-team-project` через **File → Clone repository**.  
2. Добавил класс `Welcome.java`:

```java
public class Welcome {
    public static void greet() {
        System.out.println("Добро пожаловать в Java-проект!");
    }
}
```

3. Сделал коммит «Добавлен класс Welcome» и нажал **Push origin**.  
4. Создал ветку `desktop-feature`, изменил `HelloWorld.java`, и опубликовал ветку.  
5. Нажал **Create Pull Request** — GitHub открыл PR-форму в браузере.

## Задание

1. Установите GitHub Desktop и авторизуйтесь в своём аккаунте.  
2. Клонируйте репозиторий `java-team-project`.  
3. Создайте в IDE новый Java-файл и закоммитьте его через GitHub Desktop.  
4. Push изменения на GitHub и убедитесь, что коммит появился на сайте.  
5. Создайте новую ветку `desktop-practice` и опубликуйте её.  
6. Через Desktop инициируйте пул-реквест и пришлите ссылку в чате.

---

<div class="lesson-nav">
  {% if page.previous %}
    <a href="{{ page.previous.url }}">← Назад</a>
  {% endif %}
  
  {% if page.next %}
    <a href="{{ page.next.url }}">Вперёд →</a>
  {% endif %}
</div>
