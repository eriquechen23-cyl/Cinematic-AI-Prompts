# Cinematic AI Prompts (電影級 AI 提示詞系統)

這是一個模擬專業電影攝製團隊的 AI Agent 系統，旨在將模糊的故事概念轉化為高品質、結構化且連戲的 AI 影片生成提示詞 (Prompts)。本系統特別針對 Google Flow 等影片生成工具優化，支援 8 秒片段的精準控制。

## 核心特色 (Features)

*   **專業分工 (Role-Based Agents)**: 模擬真實劇組，包含導演、編劇、攝影指導 (DoP)、美術指導、服裝設計師等 10+ 個專業角色。
*   **連戲控制 (Continuity System)**: 透過「共同大腦 (Shared Brain)」機制，確保角色外觀、環境與風格在不同鏡頭間保持一致。
*   **結構化輸出 (Structured Output)**: 自動生成符合 Google Flow 格式的 Markdown 腳本，包含時間軸 (Timeline)、運鏡 (Camera Motion) 與負面提示詞。
*   **模組化架構 (Modular Architecture)**: 系統邏輯 (`system`) 與使用者資料 (`workspace`) 分離，易於擴充與維護。

## 目錄結構 (Directory Structure)

```text
Cinematic-AI-Prompts/
├── system/                  # 系統核心 (Engine)
│   ├── agents/              # 各職位 Agent 設定檔 (Prompt Templates)
│   │   ├── core/            # 核心團隊 (製作人, 導演, 小說家, 連戲, QA, Prompt Engineer)
│   │   ├── pre_production/  # 前期製作 (編劇, 分鏡, 動作指導)
│   │   ├── production/      # 拍攝執行 (美術, 攝影, 燈光, 服裝, 特效)
│   │   └── post_production/ # 後期製作 (調色, 配音, 字幕, 音效)
│   ├── workflows/           # 工作流程指南
│   └── agents/              # 各職位 Agent 設定檔 (Prompt Templates)
└── workspace/               # 使用者工作區 (User Data)
    ├── assets/              # 共用資產庫 (風格, 角色)
    └── projects/            # 專案資料夾 (存放 Bible 與 最終腳本)
```

## 快速開始 (Getting Started)

本系統設計為搭配 LLM (如 ChatGPT, Claude) 使用。請扮演 **製作人 (Producer)** 的角色，並依照 `system/workflows/main_workflow.md` 的指引操作。

1.  **啟動專案**:
    *   在 `workspace/projects/` 下建立一個新的專案資料夾 (例如 `My_SciFi_Short`).
    *   開啟 `system/workflows/main_workflow.md` 查看完整流程。

2.  **執行流程**:
    *   **Step 1 故事開發**: 呼叫 [小說家 Agent] 將您的模糊想法轉化為完整故事。
    *   **Step 2 視覺化**: 呼叫 [導演 Agent] 與 [連戲指導 Agent] 建立鏡頭序列與角色設定 (Bible)。
    *   **Step 3 前期製作**: 呼叫 [編劇 Agent] 拆解 8 秒片段的時間軸。
    *   **Step 4 拍攝執行**: 依序呼叫 [美術]、[服裝]、[攝影]、[燈光] 豐富畫面細節。
    *   **Step 5 後期製作**: 加入 [配音] 與 [調色] 設定。

3.  **最終輸出**:
    *   最後由 [製作人 Agent] 彙整所有資訊，產出最終的 Markdown 檔案 (例如 `episode_01.md`)。
    *   該檔案可直接用於 Google Flow 或其他 AI 影片生成工具。

## 系統擴充 (Expansion)

若需要新增角色 (例如：動作指導)，請依以下步驟擴增：
1.  **建立檔案**: 在 `system/agents/` 下建立新的 Agent 檔案 (參考其他 Agent 格式)。
2.  **更新流程**: 修改 `system/workflows/main_workflow.md`，將新 Agent 納入適當的步驟中。
3.  **連接大腦**: 確保新 Agent 能讀取 `Continuity Agent` 的資料，以保持設計一致。

---
*Created by Cinematic AI Team*
