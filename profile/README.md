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

Главные (но не все) особенности reDTF:

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>1. Архитектура запросов</h3>
      <p>Никакого Server-Side Rendering (SSR), скрытых серверных запросов и телеметрии. Все обращения к API идут напрямую<sup>*</sup> из браузера к серверам DTF — путь каждого килобайта данных можно отследить в DevTools.</p>
      <br>
    </td>
    <td width="50%" valign="top">
      <h3>2. Полная прозрачность</h3>
      <p>Весь код проекта открыт, собирается на GitHub Actions и деплоится через GitHub Pages. Код в браузере в точности совпадает с репозиторием, а при желании можно за пару минут <a href="https://github.com/re-dtf/.github/blob/main/guides/fork-and-deploy-guide.md">развернуть свой reDTF</a>.</p>
      <br>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>3. Глубокая кастомизация</h3>
      <p>Благодаря модульной системе <code>ThemeLoader</code> интерфейс полностью в ваших руках: переключайтесь между эпохами дизайна DTF (2022, 2023, скоро 2025), меняйте стиль оценок, типографику, анимации и компоновку под себя.</p>
      <br>
    </td>
    <td width="50%" valign="top">
      <h3>4. Легковесность</h3>
      <p>Клиент на Svelte 5 скомпилирован в чистый JavaScript без тяжелого рантайма. Минимальный вес бандла гарантирует быстрый запуск и стабильную работу на слабых устройствах и при плохом интернете.</p>
      <br>
    </td>
  </tr>
</table>

<p><sub>* <b>Исключение — авторизация:</b> из-за технических ограничений DTF API (политика CORS) запросы на вход и обновление временного токена отправляются через <a href="https://www.val.town/x/donnertech/redtf-proxy">открытый прокси</a> только с явного подтверждения пользователя. Прокси ничего не сохраняет и не умеет отправлять запросы никуда кроме DTF. А развернуть собственный инстанс можно <a href="https://github.com/re-dtf/proxy#инструкция-по-развертыванию">буквально за пару минут</a>. Подробный разбор безопасности читайте в <a href="https://github.com/re-dtf/.github/blob/main/SAFETY.md">SAFETY.md</a>.</sub></p>

<br>

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

В рамках организации развивается семейство взаимосвязанных репозиториев:

*   [**`reDTF/client`**](https://github.com/re-dtf/client) <br>
    Основной фронтенд-клиент на Svelte 5. Ядро проекта.
*   [**`reDTF/proxy`**](https://github.com/re-dtf/proxy) <br>
    Прозрачный прокси авторизации для безопасного обхода CORS-ограничений DTF API.
*   [**`reDTF/api-docs`**](https://github.com/re-dtf/api-docs) ([сайт](https://docs.redtf.org/)) <br>
    Актуальная документация по API DTF (OpenAPI 3.1) для разработчиков reDTF и сторонних проектов.

<hr>

## Стек технологий

*   **Svelte 5 (Runes)** — реактивность на нативных рунах без сторонних стейт-менеджеров и рантайм-оверхеда.
*   **SvelteKit 3 (`adapter-static`)** — 100% статичный SPA-клиент без SSR и выполнения кода на сервере.
*   **TypeScript** — строгая типизация фасада API, моделей данных и контрактов тем оформления.
*   **Чистый CSS** — изоляция стилей компонентов и CSS-переменные для тем оформления без тяжелых фреймворков.

<hr>

## Участие в разработке

reDTF открыт для контрибьюторов — как людей, так и разработчиков в паре с AI-ассистентами (но не вайбкодеров, пожалуйста.). Архитектура и правила прозрачны и подробно задокументированы:

*   **Документация и архитектура**: устройство хранилища, темы, анимации и фасад API описаны в [docs/architecture](https://github.com/re-dtf/client/tree/dev/docs/architecture). Пошаговые инструкции (добавить тему, настройку, метод API) — в [docs/guides](https://github.com/re-dtf/client/tree/dev/docs/guides).
*   **Правила для людей и агентов**: ознакомьтесь с [CONTRIBUTING.md](https://github.com/re-dtf/client/blob/dev/CONTRIBUTING.md) и [AGENTS.md](https://github.com/re-dtf/client/blob/dev/AGENTS.md).
*   **Задачи и идеи**: заглядывайте в [Issues](https://github.com/re-dtf/client/issues) и предлагайте Pull Requests. Крупные изменения (новые темы или компоненты) сначала обсуждаются в issue.

<hr>

## Правовая информация (Disclaimer)
**reDTF** является независимым фанатским проектом с открытым исходным кодом. Данное приложение не аффилировано, не спонсируется и никак официально не связано с сайтом DTF или компанией ООО «Комитет». Все права на торговые марки, логотипы и оригинальный контент, отображаемый в клиенте, принадлежат их законным владельцам.
Ознакомьтесь с нашими [Пользовательским соглашением](https://github.com/re-dtf/.github/blob/main/TERMS.md), [Политикой конфиденциальности](https://github.com/re-dtf/.github/blob/main/PRIVACY.md) и [Безопасностью авторизации](https://github.com/re-dtf/.github/blob/main/SAFETY.md).

<br>

<div align="center">
  <hr width="50%">
  <i>By the community, for the community 🩵</i>
</div>
