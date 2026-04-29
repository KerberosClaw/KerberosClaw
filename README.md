# KerberosClaw

**IoT × AI Agent × Harness Engineering**

做 IoT 十幾年，從工廠裡會生鏽的 Modbus PLC 到客廳裡發光的 IKEA 檯燈都接過，中間的怪東西就不細數了。後來想想這些泡在協議湯裡的年資也不能白繳學費，於是包成 MCP Server 讓 AI 用人話操作；順手又刻了條 RAG pipeline，主要想搞懂「我用 LangChain」到底算不算懂 RAG。

最近多了一條軸：harness engineering — 不再急著自己寫 code，改去搭一個能讓 AI 寫 code 的工地：skills、hooks、memory layout、PM glue 全攤開放上來。想看就翻翻看，覺得有用拿去，覺得好笑算我賺到。

## IoT × AI Agent × RAG

| Project | One-liner |
|---------|-----------|
| [kc_rag_lab](https://github.com/KerberosClaw/kc_rag_lab) | 從零手刻 RAG pipeline，不用框架，因為「我用 LangChain」不算懂 RAG |
| [kc_iot_gateway](https://github.com/KerberosClaw/kc_iot_gateway) | 4 種協議的設備塞進 1 個 REST API + Dashboard + MCP Server |
| [kc_modbus_mcp](https://github.com/KerberosClaw/kc_modbus_mcp) | AI 說「讀取溫度」而不是「讀 register 0x0000 的 float32」 |
| [kc_tradfri_mcp](https://github.com/KerberosClaw/kc_tradfri_mcp) | 讓 AI 開關 IKEA 的燈，經由 CoAP/DTLS，因為事情從來沒有簡單過 |
| [kc_openclaw_local_llm](https://github.com/KerberosClaw/kc_openclaw_local_llm) | 測了 13 個本地 LLM，只有 2 個能穩定 call tool |
| [kc_system_design](https://github.com/KerberosClaw/kc_system_design) | 4 個系統設計踩坑故事，大多在凌晨兩點學會的 |

## Claude Code Harness

| Project | One-liner |
|---------|-----------|
| [kc_claude_harness](https://github.com/KerberosClaw/kc_claude_harness) | Meta-repo：把這幾個 repo 用 manifesto 跟 dotfiles 黏在一起 |
| [kc_ai_skills](https://github.com/KerberosClaw/kc_ai_skills) | 做到懶得再手動做的事，包成 skills + 4 個攔截手滑用的 hook |
| [kc_pm_kit](https://github.com/KerberosClaw/kc_pm_kit) | 兩個 prompt-driven skill：把會議記錄一路推進 Azure DevOps，省下 PM 一個下午 |
| [kc_claude_memory_sync](https://github.com/KerberosClaw/kc_claude_memory_sync) | SSH + git bare repo，讓 Claude 在多台機器都記得我是誰 |
| [kc_llm_wiki_starter](https://github.com/KerberosClaw/kc_llm_wiki_starter) | Karpathy 的三層 wiki pattern（raw/wiki/schema），LLM 自己當小編 |

## Side / Lab

| Project | One-liner |
|---------|-----------|
| [kc_smart_lamp](https://github.com/KerberosClaw/kc_smart_lamp) | 自己做一盞 USB 供電的 BLE 桌燈，不要 app、不要雲、不要 vendor 綁架 |
| [kc_pet_analyzer](https://github.com/KerberosClaw/kc_pet_analyzer) | 用獸醫行為學分析貓的行為，取代偽科學寵物溝通師 |
| [kc_job_radar](https://github.com/KerberosClaw/kc_job_radar) | 104 職缺雷達 — 自動搜、去重、Gmail 監聽、Telegram 推播，比我自己滑網頁勤勞 |

## Tech

MQTT, Modbus, CoAP, BLE, Webhook | Python, FastAPI, FastMCP | RAG, ChromaDB, Gradio | Docker, MCP, Ollama | Claude Code (skills, hooks, agents)
