# squint-devices

Device tools for [Squint](https://github.com/DEVBUFF/squint), the UI/UX and branding art director for
Claude Code. Install it next to Squint when you want audits to see your product the way users do.

| Server | What Squint uses it for | Needs |
|---|---|---|
| `browser`: [chrome-devtools-mcp](https://github.com/ChromeDevTools/chrome-devtools-mcp) 1.11.0 | Full-page screenshots, desktop / mobile / dark-mode emulation, Lighthouse accessibility audits, performance traces | Google Chrome, Node.js 20+ |
| `mobile`: [mobile-mcp](https://github.com/mobile-next/mobile-mcp) 1.0.11 | iOS Simulator and Android emulator: screenshots, element lists, taps, swipes, walking through flows | Node.js 20+; Xcode for iOS, Android platform-tools + an emulator for Android |

Both run locally through `npx` with pinned versions. Usage statistics, CrUX lookups and telemetry are
turned off.

## Install

```bash
claude plugin marketplace add DEVBUFF/squint
```
```bash
claude plugin install squint-devices@squint
```

Restart Claude Code. The first start downloads the packages, which can take a minute. You can turn
either server off in `/mcp`.

Without this plugin Squint still works: it falls back to headless Chrome, `xcrun simctl` and `adb`
for screenshots, or asks you for screenshots.

---

**RU.** Инструменты устройств для [Squint](https://github.com/DEVBUFF/squint). Браузерный MCP снимает
скриншоты, эмулирует устройства и тёмную тему и запускает Lighthouse-аудит доступности. Мобильный MCP
работает с iOS Simulator и Android-эмулятором: скриншоты, тапы, свайпы, проход по флоу.
Установка: `claude plugin install squint-devices@squint` после `claude plugin marketplace add DEVBUFF/squint`.
Без этого плагина Squint тоже работает, через запасные способы съёмки.

## License

[MIT](LICENSE)
