<div align="center">
  <img src="https://raw.githubusercontent.com/re-dtf/.github/refs/heads/main/branding/LogoDtf.svg" alt="reDTF" width="200" />

  <blockquote>
    <b>Переосмысление клиентского опыта для DTF</b><br>
    <i>Открытый исходный код, максимальная скорость, кастомизация и никаких нежеланных редизайнов.</i>
  </blockquote>

  <div>
    <a href="https://svelte.dev/"><img src="https://img.shields.io/badge/Svelte_5-FF3E00?style=for-the-badge&logo=svelte&logoColor=white" alt="Svelte 5" /></a>
    <a href="https://www.typescriptlang.org/"><img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" /></a>
    <img src="https://img.shields.io/badge/SPA-100%25_Client--Side-4CAF50?style=for-the-badge" alt="100% Client-Side" />
    <img src="https://img.shields.io/badge/Status-In_Development-F2C94C?style=for-the-badge&logoColor=black" alt="Status" />
  </div>
</div>

<br>

## О проекте

Проект **reDTF** зародился из желания создать альтернативный, легковесный и настраиваемый клиент для DTF, который не будет подвергаться нежеланным нововведениям и полагаться на шметрики.

Главная идея — **Zero Server Logic**. Приложение работает исключительно в браузере, связываясь с публичным API напрямую. Никаких промежуточных серверов для рендеринга, сбора аналитики или скрытых запросов. Наша главная цель — обеспечить полную прозрачность, чтобы пользователи могли доверять клиенту.

<hr>

## Особенности

Главное (но не всё), чем отличается reDTF от обычного DTF:

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>1. Архитектура запросов</h3>
      <p>Никакого Server-Side Rendering (SSR) и скрытых серверных запросов. Все запросы к API идут через ваш браузер, и вы можете проследить путь каждого килобайта ваших данных.</p>
    </td>
    <td width="50%" valign="top">
      <h3>2. Полная прозрачность</h3>
      <p>Весь код проекта находится в открытом доступе, компилируется прямо на Github Actions, а затем деплоится через Github Pages — вы можете убедиться, что пользуетесь именно тем кодом, который видели. А если и этого недостаточно, вы можете <a href="https://github.com/re-dtf/.github/blob/main/guides/fork-and-deploy-guide.md">развернуть свой reDTF</a> буквально за пару минут.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>3. Глубокая кастомизация</h3>
      <p>Благодаря нашему <code>ThemeLoader</code>, вы можете кастомизировать клиент как вам захочется через простые настройки. Дизайн подстраивается под вас, а не наоборот.</p>
    </td>
    <td width="50%" valign="top">
      <h3>4. Overlay Stack</h3>
      <p>Чтобы не сбрасывать состояние ленты при открытии постов, используется кастомный history-backed стек. Открытие контента накладывается поверх ленты с сохранением нативной браузерной навигации «Назад».</p>
    </td>
  </tr>
</table>

<hr>

<div align="center">
  <h3>Следите за новостями проекта</h3>
  <p>Все свежие обновления, анонсы новых фич, актуальные сборки и обсуждения процесса разработки публикуются в нашем официальном Telegram-канале.</p>
  <a href="https://t.me/re_dtf">
    <img src="https://img.shields.io/badge/Telegram_Channel-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram Channel" />
  </a>
  <br>
</div>

<hr>

## Экосистема

В рамках организации планируется развитие нескольких связанных репозиториев:

*   [**`reDTF/client`**](https://github.com/re-dtf/client) <br>
    Основной фронтенд-клиент на Svelte 5. Ядро проекта.
*   [**`reDTF/proxy`**](https://github.com/re-dtf/proxy) <br>
    Прокси авторизации, созданное для обхода ограничений DTF API.
*   <kbd>В ПЛАНАХ</kbd> [**`reDTF/android-app`**](https://github.com/re-dtf/android-app) <br>
    Мобильное приложение, работающее нативно, а не через PWA. Планируется позже.

<hr>

## Стек технологий

Разработка ведется с использованием самых свежих и производительных инструментов:

<details>
<summary><b>Развернуть детали стека</b></summary>
<br>

*   **UI Ядро:** [Svelte 5](https://svelte.dev/) с использованием `Runes`.
*   **Роутинг:** SvelteKit с интеграцией `@sveltejs/adapter-static`.
*   **Язык:** TypeScript со строгой типизацией сетевых запросов.
*   **Стили:** Чистый CSS с CSS Custom Properties (CSS-переменные).
</details>

<hr>

## Вклад в развитие (Contributing)

На данный момент проект находится на стадии активного формирования ядра. Несмотря на то, что сейчас код пишется силами одного разработчика, вся архитектура изначально выстраивается по стандартам Open Source — чтобы любой желающий мог легко вкатиться и помочь.

Если вы хотите присоединиться:
1. Загляните в раздел **Issues** основного клиента.
2. Изучите архитектурные правила в папке `.agents` (особенно полезно при работе с AI-ассистентами).
3. Предлагайте свои идеи через Pull Requests! 

<br>

<div align="center">
  <hr width="50%">
  <i>By the community, for the community ❤️</i>
</div>
