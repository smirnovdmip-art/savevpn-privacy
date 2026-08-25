# SaveVPN — материалы для App Store Connect

## 1. Notes for Review (обязательно вставить при подаче)

```
This app provides a free trial (2 GB traffic) accessible immediately after
email verification, with no payment required — please use the "Try it"
option on the sign-in screen to test core VPN functionality directly.

No in-app purchases are offered; the app does not sell or reference any
paid content, pricing, or external payment method within its UI.
```

Смысл: сразу направить ревьюера на бесплатный триал, чтобы он не искал
способ "заплатить" и не встал в тупик.

## 2. Export Compliance (шифрование)

При подаче Apple спросит "Does your app use encryption?" — отвечать **Yes**
(VLESS/REALITY/TLS — это шифрование сетевого трафика). Дальше вопрос
"Is your app exempt from export compliance documentation?" — почти
наверняка **Yes** (стандартное исключение для приложений, использующих
только общедоступную/стандартную криптографию — TLS и т.п., без
собственных проприетарных алгоритмов). Итог обычно: не нужно грузить
отдельный документ, только отметить галочки в форме.

## 3. Возрастной рейтинг (Age Rating) — важный VPN-специфичный пункт

В анкете возрастного рейтинга есть вопрос про **"Unrestricted Web Access"**
(даёт ли приложение неограниченный доступ в интернет/обходит ограничения).
Для VPN-приложения честный ответ — **Yes**. Это обычно поднимает рейтинг
минимум до **17+** — так делают все VPN-приложения в сторе (это НЕ
блокирует публикацию, просто меняет возрастную категорию). Пытаться
ответить "No" рискованно — легко проверяется live-тестом и может привести
к отклонению за недостоверную анкету, что хуже, чем просто рейтинг 17+.

## 4. App Privacy (раздел "Privacy" в App Store Connect — анкета о сборе данных)

Указать примерно так (сверить точные формулировки при заполнении —
Apple даёт закрытый список категорий):

- **Email Address** — Linked to You — используется для: App Functionality
  (создание/авторизация аккаунта), не для трекинга.
- **Device ID** — Linked to You — App Functionality (лимит устройств на
  аккаунт).
- **НЕ отмечать**: Browsing History, Search History, Location, Contacts,
  Financial Info и т.п. — этого приложение не собирает вообще.
- Трекинг между приложениями/сайтами третьих лиц — **No**.

## 5. Описание приложения (черновик, RU) — ПРОВЕРИТЬ И ОТРЕДАКТИРОВАТЬ САМОМУ

```
SaveVPN — простой и быстрый VPN для безопасного доступа в интернет.

• Автоматический выбор самого быстрого сервера
• Частичный режим — VPN только для выбранных приложений
• Экран для проверки, к каким доменам обращаются приложения при
  подключённом VPN
• Бесплатный пробный период — 2 ГБ трафика, без ввода платёжных данных

Подключение в одно нажатие, без сложных настроек.
```

**English draft:**
```
SaveVPN — a simple, fast VPN for secure internet access.

• Automatic selection of the fastest available server
• Partial Mode — route only selected apps through the VPN
• See which domains your apps connect to while VPN is on
• Free trial — 2 GB of traffic, no payment details required

One-tap connection, no complicated setup.
```

## 6. Ключевые слова (Keywords, до 100 символов, через запятую)

```
vpn,proxy,privacy,secure,fast vpn,unblock,anonymous,online privacy,vless
```

## 7. НЕ ЗАБЫТЬ перед сабмитом

- [ ] Privacy Policy URL — вставить ссылку после настройки GitHub Pages
- [ ] Support URL — тоже обязательное поле, можно указать ту же страницу
      или отдельную (сейчас реальной поддержки-страницы нет — уточнить,
      куда направлять; Telegram-бот ссылкой в App Store Connect указывать
      МОЖНО, это обычная практика, не то же самое что платёжная ссылка
      внутри UI приложения)
- [ ] Base app price — убедиться что стоит **Free** (не платный download),
      иначе Apple обработает саму загрузку как платёж через них
- [ ] Скриншоты — на момент подготовки не проверялись, отдельная задача
