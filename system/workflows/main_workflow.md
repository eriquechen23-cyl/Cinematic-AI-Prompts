# 電影級 AI Prompt 工作流程 (Cinematic AI Prompt Workflow)

此工作流程模擬專業電影攝製團隊，旨在生成高品質的 AI 圖像 Prompt。

## 如何使用
請扮演 **製作人 (Producer)** 的角色，並依照以下順序將您的想法傳遞給各個 Agent。
為了簡化檔案管理，**每一步驟 (Step) 僅輸出一個整合的 Markdown 檔案**。

**核心目標：** 將一個模糊的故事概念 (例如：「結合聖經故事 宣傳EMI教會」) 自動擴增為多個 8 秒的影片片段 (Clips)。

### 第一步：故事開發 (Story Development)
1.  **[小說家 Agent](../agents/core/novelist_agent.md):**
    *   輸入：模糊的故事概念。
    *   輸出：完整且具深度的原創故事文本。
    *   **檔案輸出:** `Step1_Story.md`

### 第二步：核心與連戲建立 (Core & Continuity)
2.  **[導演 Agent](../agents/core/director_agent.md):** 
    *   輸入：小說家的原創故事。
    *   輸出：導演願景 + **鏡頭序列 (Shot List)**。
3.  **[連戲指導 Agent](../agents/core/continuity_agent.md):** 
    *   輸入：導演願景。
    *   輸出：連戲設定檔 (角色、環境、風格)。
    *   **檔案輸出:** `Step2_Core_Continuity.md` (包含導演願景與連戲設定)

### 第三步：前期製作 (Pre-Production)
4.  **[編劇 Agent](../agents/pre_production/screenwriter_agent.md):** 
    *   輸入：鏡頭序列 + 共同大腦。
    *   輸出：動作時間軸與台詞。
5.  **[影評人 Agent](../agents/core/critic_agent.md):**
    *   輸入：導演願景 + 劇本。
    *   輸出：影評報告與修改建議。
6.  **[分鏡師 Agent](../agents/pre_production/storyboard_agent.md):** 
    *   輸入：編劇描述。
    *   輸出：構圖與運鏡。
7.  **[動作指導 Agent](../agents/pre_production/action_director_agent.md):** 
    *   輸入：鏡頭序列 + 角色設定。
    *   輸出：物理動態描述。
    *   **檔案輸出:** `Step3_Pre_Production.md` (整合劇本、影評、分鏡與動作設計)

### 第四步：拍攝執行 (Production - 畫面質感)
8.  **[美術指導 Agent](../agents/production/production_designer_agent.md):** 定義環境。
9.  **[平面設計師 Agent](../agents/production/graphic_designer_agent.md):** 定義文字道具。
10. **[服裝設計師 Agent](../agents/production/costume_designer_agent.md):** 定義服裝造型。
11. **[攝影指導 Agent](../agents/production/dop_agent.md):** 定義相機與運鏡。
12. **[燈光師 Agent](../agents/production/lighting_agent.md):** 定義光影。
13. **[特效指導 Agent](../agents/production/vfx_supervisor_agent.md):** 定義特效。
    *   **檔案輸出:** `Step4_Production.md` (整合所有美術、攝影、燈光與特效設定)

### 第五步：後期製作 (Post-Production - 聲音與色彩)
14. **[音效與配樂師 Agent](../agents/post_production/sound_designer_agent.md):** 定義 BGM 與 SFX。
15. **[配音員 Agent](../agents/post_production/voice_actor_agent.md):** 定義聲音人設。
16. **[調色師 Agent](../agents/post_production/colorist_agent.md):** 定義色彩風格。
    *   **檔案輸出:** `Step5_Post_Production.md` (整合聲音與調色設定)

### 第六步：提示詞優化 (Prompt Engineering)
17. **[提示詞工程師 Agent](../agents/core/prompt_engineer_agent.md):** 
    *   輸入：所有前述產出。
    *   動作：權重分配、負面提示、關鍵字精煉。
    *   **檔案輸出:** `Step6_Prompt_Engineering.md` (包含 Prompt 策略與草稿)

### 第七步：品質控管與迭代 (QA & Iteration)
18. **[品管 Agent](../agents/core/qa_agent.md):** 
    *   動作：審查每個 Clip 的 Prompt 品質。
    *   **檔案輸出:** `Step7_QA_Report.md` (QA 報告)

### 第八步：最終輸出 (Final Output)
19. **[製作人 Agent](../agents/core/producer_agent.md):** 
    *   動作：整合通過 QA 的資訊，建立最終檔案。
    *   **檔案輸出:** 
        1.  `Step8_Final_Output.md` (專案總結與 Prompt 清單)
        2.  `clips/` 資料夾 (包含個別的 `clip_xx.md` 檔案)

---

## 最終 Prompt 組合 (Final Prompt Assembly)
製作人將針對**每個 Clip** 輸出以下兩種格式：

1.  **結構化 Prompt (邏輯檢視用):**
    `[導演風格] + [Consistency Block Character] + [Costume Details] + [Consistency Block Environment] + [該 Clip 的動作] + [燈光與氛圍] + [攝影參數] + [分鏡構圖] + [調色風格] --ar [長寬比]`

2.  **優化 Prompt (實戰生成用):**
    *   **Midjourney:** 針對藝術性與構圖優化。
    *   **Stable Diffusion:** 針對細節控制與 LoRA 優化。
    *   **Runway/Luma:** 針對動態描述與運鏡優化。
