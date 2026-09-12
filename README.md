# KerberosClaw 🐾

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
| [kc_agent_persona_pack](https://github.com/KerberosClaw/kc_agent_persona_pack) | 讓 AI agent 換 session 還記得自己是誰 — 純讀文件維持人格，不 fine-tune |
| [kc_agent_a2a](https://github.com/KerberosClaw/kc_agent_a2a) | 從 persona pack 長出的群聊技術預覽：紙條、夜聊、Discord Party，再把聊天經歷帶回主人格；原來連 AI 聚會都要顧帳本 |
| [kc_proactive_poke](https://github.com/KerberosClaw/kc_proactive_poke) | 讓 AI 不等你開口 — 定期自己判斷有沒有值得說的事，然後大多數時候決定閉嘴 |
| [kc_claude_memory_sync](https://github.com/KerberosClaw/kc_claude_memory_sync) | SSH + git bare repo，讓 Claude 在多台機器都記得我是誰 |
| [kc_llm_wiki_starter](https://github.com/KerberosClaw/kc_llm_wiki_starter) | Karpathy 的三層 wiki pattern（raw/wiki/schema），LLM 自己當小編 |

## LLM Failure & Safety

| Project | One-liner |
|---------|-----------|
| [kc_text2sql_failure_lab](https://github.com/KerberosClaw/kc_text2sql_failure_lab) | Executable ≠ Correct — SQL 跑得動 ≠ 答對，一間專抓 Text-to-SQL 語意錯的實驗室 |
| [kc_llm_jailbreak_test_kit](https://github.com/KerberosClaw/kc_llm_jailbreak_test_kit) | 同一個 jailbreak 殼丟給 ChatGPT / Claude / Gemini 各自怎麼破 — 附可複現 mock prompts 測你自家 LLM |
| [kc_llm_lazy_thinking_lab](https://github.com/KerberosClaw/kc_llm_lazy_thinking_lab) | 叫 AI「自己想、show your work」真的會變快嗎？四模型控制實驗：全部變慢，「快」的答案其實是提早放棄 |

## Side / Lab

| Project | One-liner |
|---------|-----------|
| [kc_smart_lamp](https://github.com/KerberosClaw/kc_smart_lamp) | 自己做一盞 USB 供電的 BLE 桌燈，不要 app、不要雲、不要 vendor 綁架 |
| [kc_pet_analyzer](https://github.com/KerberosClaw/kc_pet_analyzer) | 用獸醫行為學分析貓的行為，取代偽科學寵物溝通師 |
| [kc_locspoof](https://github.com/KerberosClaw/kc_locspoof) | 從 macOS 改 iPhone GPS 座標、免越獄 — Swift daemon + Web UI 全鏈路打通 |
| [kc_wherebear_oss](https://github.com/KerberosClaw/kc_wherebear_oss) | 自架個人位置平台 — 手機低頻回報「我大概在哪」到自己的 Supabase，本地 bridge 撈成 JSON 餵下游；拒絕連續高精度追蹤、省電優先 |
| [kc_healthsteps_oss](https://github.com/KerberosClaw/kc_healthsteps_oss) | 沒開過 Xcode 也能有一支自己的 iOS app — 簽章跟插線你來、Swift 交給 Claude Code；刻意不給你 clone，你自己長一支 |
| [kc_job_radar](https://github.com/KerberosClaw/kc_job_radar) | 104 職缺雷達 — 自動搜、去重、Gmail 監聽、Telegram 推播，比我自己滑網頁勤勞 |
| [kc_booking_radar_oss](https://github.com/KerberosClaw/kc_booking_radar_oss) | 訂位空位雷達 — 餐廳、住宿、機票都能盯，只報變動的那一筆；也是 proactive-poke 第一個會看外面世界的語料源 |

## Write-ups

- [對話錄音 → 分色字幕影片產線](https://gist.github.com/KerberosClaw/adcaf49ec692593006556494d160708d) — 一支麥錄「你 × AI 語音對談」換掉本聲 + 上你/AI 分色字幕。踩坑重點：ASR 時間碼估歪 ~3 秒 → 用 RMS 能量掃描驗 ground truth → 挖出「兩人聲音 overlap」才是換聲拆不乾淨的根因 → 收斂成一套錄音紀律。

## Tech

MQTT, Modbus, CoAP, BLE, Webhook | Python, FastAPI, FastMCP | RAG, ChromaDB, Gradio | Whisper ASR, Seed-VC, ffmpeg, PIL | Docker, MCP, Ollama | Claude Code (skills, hooks, agents)
