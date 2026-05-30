# KitsuVisuals(EN)

> A clean, performant HUD & visual overlay mod for Minecraft 1.16.5 (Forge).

KitsuVisuals is a client-side mod that replaces and extends Minecraft's vanilla UI with a cohesive set of HUD panels, in-world overlays, and quality-of-life features — all rendered through smooth OpenGL primitives with a unified visual style.

---

## Features

### HUD Panels

Each panel can be independently moved, resized, hidden, and themed.

- **Top HUD** — `KitsuVisuals · FPS · Ping · time` strip across the top of the screen
- **Coordinates** — current X/Y/Z position with rounded panel background
- **Player Info** — name + HP bar + held weapon and armor of the player you're looking at, with HP bar that matches the displayed HP value precisely (works with vanilla and custom scoreboard-based HP)
- **Active Effects** — compact effect list with colored dot indicators and remaining-time
- **Held / Equipped Items** — durability bars rendered as a vertical strip
- **Keystroke display** — WASD + jump/crouch/click feedback

All panels respect GUI scale and can be relocated by entering Move/Resize mode via the in-game menu.

### In-World Overlays

- **Player nameplates** — custom nick + ping over each player, visible through walls with reduced opacity when occluded
- **Hitbox indicator** — sliding ring around players that highlights their hit area
- **Block highlighter** — colored fill + outline on the block you're looking at, replacing vanilla's white outline
- **Sky particles** — drifting volumetric sparkles in the sky around the player, color-customizable
- **Player trails** — colored cloud trail behind the player (cloud color picker)
- **Jump rings** — expanding wave when you jump
- **Sun hat** — Chinese-hat-style geometry around the player
- **FullBright** — gamma override for clearer dark areas
- **Auto-sprint, motion blur, custom hotbar, swing animation** — toggleable QoL tweaks

### Waypoint System

Press your bound waypoint key (default `K`, configurable in vanilla Controls) to open the waypoint manager.

- Create, edit, delete saved waypoints
- Each waypoint stores name + X/Y/Z + color
- In-world rendering: vertical beam visible through any block + floating label
- **Distance-aware scaling** — the label grows as you move farther away (continuous curve up to 750m, then locked) so it's always readable
- **Far-plane projection** — the label is billboarded at a fixed distance from the camera, so it never disappears past the render distance
- Smooth open animation on the waypoint list screen

### Settings UI

A custom 4-tab settings screen with:

- **Client tab** — language, hit sound toggle, waypoint shortcut
- **Graphics tab** — visual effects, sky particles, block highlight, palette colors
- **Different tab** — view tweaks (right-hand position, hand rotation, slider-based)
- **Styles tab** — theme accent color picker (9 colors)

Settings persist between sessions in `kitsuvisuals_client.properties`.

### Visual Style

- Smooth GPU-rendered rounded corners via custom OpenGL pipeline (no pixel-rect fakery)
- Custom font renderer using Roboto/Arial Bold for clean, high-resolution UI text
- Premultiplied-alpha textures to eliminate corner halos
- Theme accent color permeates all panels, buttons, and overlays
- Smooth open/close animations with ease-out cubic timing

### Audio

- **Hit sound** — plays a custom bell sound when you strike another entity (toggleable). Uses `javax.sound.sampled` directly so it works independently of Minecraft's sound system.

---

## Installation

1. Install Minecraft 1.16.5
2. Install [Forge for 1.16.5](https://files.minecraftforge.net/) (any recent build)
3. Drop the `KitsuVisuals-1.16.5` into your `mods/` folder
4. Launch and enjoy

Configuration file is created automatically at `.minecraft/config/kitsuvisuals_client.properties` on first run.

---

## Usage

- **Open settings** — press `R-Shift` in game (rebindable in vanilla Controls)
- **Open waypoint list** — press `K` (rebindable)
- **Move/Resize a panel** — open settings → enter Move mode → drag panels by their body, resize via the corner handle
- **Cycle through hitbox / trail / cloud / hat colors** — use the `<` `>` arrows next to color labels in Graphics

---

## Compatibility

- **Minecraft** 1.16.5
- **Forge** 36.x or newer
- **Java** 17 (JDK 17 required at runtime)

Should work alongside most other client-side visual mods. If a panel overlaps with another mod's HUD element, use Move mode to reposition it.

---

## Credits

Developed for personal use; rebranded from "SakuraVisuals" in late 2025.

If you find a bug or have a feature request, open an issue on the repository.

---

## License

All rights reserved unless otherwise noted. This mod is distributed for personal and community use; please don't redistribute the compiled jar without permission.



# KitsuVisuals(RU)

> Чистый, производительный мод для HUD и визуальных эффектов в Minecraft 1.16.5 (Forge).

KitsuVisuals — это клиентский мод, который заменяет и расширяет ванильный UI Minecraft единым набором HUD-панелей, мировых оверлеев и удобных функций — всё отрисовывается через сглаженные OpenGL-примитивы в едином визуальном стиле.

---

## Возможности

### HUD панели

Каждую панель можно независимо перемещать, изменять размер, скрывать и оформлять под свою тему.

- **Верхний HUD** — полоса `KitsuVisuals · FPS · Ping · время` в верхней части экрана
- **Координаты** — текущие X/Y/Z с закруглённым фоном
- **Информация об игроке** — имя + шкала HP + предмет в руке и броня игрока, на которого ты смотришь. Шкала HP точно соответствует отображаемому числу (работает с ванильным HP и с кастомным HP из scoreboard)
- **Активные эффекты** — компактный список эффектов с цветными точками и оставшимся временем
- **Снаряжение / экипировка** — полоски прочности предметов в виде вертикальной ленты
- **Отображение нажатий клавиш** — WASD + прыжок/присед/клики

Все панели учитывают GUI scale и могут быть перемещены в режиме Move/Resize из внутриигрового меню настроек.

### Мировые оверлеи

- **Ники игроков** — кастомный ник + пинг над каждым игроком, видимые через стены с пониженной непрозрачностью при перекрытии
- **Индикатор хитбокса** — скользящее кольцо вокруг игроков, подсвечивающее зону попадания
- **Подсветка блока** — цветная заливка + контур на блоке, на который смотришь (заменяет ванильную белую обводку)
- **Частицы в небе** — плавающие объёмные искры вокруг игрока, цвет настраивается
- **Шлейф игрока** — цветной облачный след за игроком (выбор цвета облака)
- **Кольца прыжка** — расходящаяся волна при прыжке
- **Солнечная шляпа** — китайская шляпа над игроком
- **FullBright** — переопределение гаммы для тёмных зон
- **Авто-спринт, размытие движения, кастомный хотбар, анимация удара** — переключаемые QoL-улучшения

### Система меток (Waypoints)

Нажми привязанную клавишу метки (по умолчанию `K`, перенастраивается в ванильных настройках управления) — откроется менеджер меток.

- Создавай, редактируй и удаляй сохранённые метки
- Каждая метка хранит имя + X/Y/Z + цвет
- В мире: вертикальный луч, видимый через любые блоки + плавающая табличка с названием
- **Масштабирование с расстоянием** — табличка растёт по мере удаления (непрерывная кривая до 750 м, потом фиксируется), чтобы всегда оставаться читаемой
- **Проекция на far-plane** — табличка размещается на фиксированной дистанции от камеры и никогда не пропадает за пределами дистанции прорисовки
- Плавная анимация открытия экрана списка меток

### Меню настроек

Кастомный экран настроек с 4 вкладками:

- **Клиент** — язык, звук удара, привязка клавиши меток
- **Графика** — визуальные эффекты, частицы в небе, подсветка блока, выбор цветов палитры
- **Разное** — настройки вида (положение правой руки, повороты руки — слайдеры)
- **Стили** — выбор акцентного цвета темы (9 цветов)

Настройки сохраняются между сессиями в `kitsuvisuals_client.properties`.

### Визуальный стиль

- Гладкие закруглённые углы через кастомный OpenGL-пайплайн (без пиксельных приближений)
- Кастомный рендер шрифта Roboto/Arial Bold для чистого UI-текста в высоком разрешении
- Premultiplied-alpha текстуры — никаких «ореолов» по углам
- Цвет темы пронизывает все панели, кнопки и оверлеи
- Плавные анимации открытия/закрытия с ease-out cubic кривой

### Звук

- **Звук удара** — проигрывает кастомный звук колокольчика при ударе по другому существу (переключаемо). Использует `javax.sound.sampled` напрямую — работает независимо от звуковой системы Minecraft.

---

## Установка

1. Установи Minecraft 1.16.5
2. Установи [Forge для 1.16.5](https://files.minecraftforge.net/) (любая свежая сборка)
3. Положи `KitsuVisuals-1.16.5.jar` в папку `mods/`
4. Запускай и пользуйся

Файл конфигурации создаётся автоматически при первом запуске: `.minecraft/config/kitsuvisuals_client.properties`.

---

## Использование

- **Открыть настройки** — нажми `R-Shift` в игре (перепривязывается в ванильных настройках управления)
- **Открыть список меток** — нажми `Л` (перепривязывается)
- **Переместить / изменить размер панели** — открой настройки → войди в Move-режим → перетаскивай панели за тело, меняй размер за угловой маркер
- **Циклы цветов для хитбокса / шлейфа / облака / шляпы** — стрелки `<` `>` рядом с подписью цвета во вкладке «Графика»

---

## Совместимость

- **Minecraft** 1.16.5
- **Forge** 36.x или новее
- **Java** 17 (требуется JDK 17 при запуске)

Должно работать совместно с большинством клиентских визуальных модов. Если панель перекрывается с HUD другого мода — переключи Move-режим и переставь её.

---

## Авторы

Разрабатывается для личного пользования; переименован из «SakuraVisuals» в конце 2025 года.

Если найдёшь баг или хочешь предложить новую функцию — открой issue в репозитории.

---

## Лицензия

Все права защищены, если иное не указано. Мод распространяется для личного и общественного использования; пожалуйста, не распространяй скомпилированный jar без разрешения.
