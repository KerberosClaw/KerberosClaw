# KerberosClaw

**IoT × MCP × AI Agent**

做了十幾年的 IoT，接過的設備從 Modbus PLC 到 IKEA 檯燈都有。現在把這些經驗打包成 MCP Server，讓 AI Agent 直接用人話操作設備。

底下這些專案就是成果 — 有些是從生產環境的傷疤長出來的，有些是半夜睡不著寫的。歡迎翻翻看，如果覺得有用就拿去，覺得好笑也算我賺到。

## Projects

| Project | One-liner |
|---------|-----------|
| [kc_iot_gateway](https://github.com/KerberosClaw/kc_iot_gateway) | 4 種協議的設備塞進 1 個 REST API + Dashboard + MCP Server |
| [kc_modbus_mcp](https://github.com/KerberosClaw/kc_modbus_mcp) | AI 說「讀取溫度」而不是「讀 register 0x0000 的 float32」 |
| [kc_tradfri_mcp](https://github.com/KerberosClaw/kc_tradfri_mcp) | 讓 AI 開關 IKEA 的燈，經由 CoAP/DTLS，因為事情從來沒有簡單過 |
| [kc_system_design](https://github.com/KerberosClaw/kc_system_design) | 4 個系統設計踩坑故事，大多在凌晨兩點學會的 |
| [kc_ai_skills](https://github.com/KerberosClaw/kc_ai_skills) | 那些做到懶得再手動做的事，包裝成 AI skill |
| [kc_openclaw_local_llm](https://github.com/KerberosClaw/kc_openclaw_local_llm) | 測了 13 個本地 LLM，只有 2 個能穩定 call tool |

## Tech

MQTT, Modbus, CoAP, Webhook | Python, FastAPI, FastMCP | Docker, MCP, Ollama
