# 電影級 AI Prompt 工作流程 (Cinematic AI Prompt Workflow)

此工作流程模擬專業電影攝製團隊，旨在生成高品質的 AI 圖像 Prompt。

## 如何使用
請扮演 **製作人 (Producer)** 的角色，並依照以下順序將您的想法傳遞給各個 Agent。

**核心目標：** 將一個模糊的故事概念 (例如：「結合聖經故事 宣傳EMI教會」) 自動擴增為多個 8 秒的影片片段 (Clips)。

### 第一步：故事開發 (Story Development)
1.  **[小說家 Agent](../agents/core/novelist_agent.md):**
    *   輸入：模糊的故事概念。
    *   輸出：完整且具深度的原創故事文本 (`01_story.md`)。

### 第二步：核心與連戲建立 (Core & Continuity)
2.  **[導演 Agent](../agents/core/director_agent.md):** 
    *   輸入：小說家的原創故事。
    *   輸出：導演願景 + **鏡頭序列 (Shot List)** (`02_director_vision.md`)。
3.  **[連戲指導 Agent](../agents/core/continuity_agent.md):** 
    *   **初始化:** 建立「共同大腦」，鎖定角色外觀、核心環境與風格。
    *   **學習:** 隨著鏡頭推進，記錄狀態變化。
    *   **輸出:** 連戲設定檔 (`03_consistency.md`)。

### 第三步：前期製作 (Pre-Production)
4.  **[編劇 Agent](../agents/pre_production/screenwriter_agent.md):** 
    *   **輸入:** 鏡頭序列 + **共同大腦記憶庫**。
    *   輸出：為每個 Clip 拆解動作時間軸與台詞 (`04_screenplay.md`)。
5.  **[影評人 Agent](../agents/core/critic_agent.md):**
    *   **輸入:** 導演願景 + 劇本。
    *   **動作:** 檢查邏輯漏洞、情感共鳴與陳腔濫調。
    *   **輸出:** 影評報告與修改建議 (`05_critique.md`)。
6.  **[分鏡師 Agent](../agents/pre_production/storyboard_agent.md):** 
    *   **輸入:** 編劇的動作描述。
    *   **輸出:** 定義構圖法則 (如三分法)、空間層次 (前中後景) 與運鏡方式 (`06_storyboard.md`)。
7.  **[動作指導 Agent](../agents/pre_production/action_director_agent.md):** 
    *   **輸入:** 鏡頭序列 + 角色設定。
    *   輸出：定義物理動態、速度與力度 (`07_action.md`)。

### 第四步：拍攝執行 (Production - 畫面質感)
8.  **[美術指導 Agent](../agents/production/production_designer_agent.md):** 
    *   **輸入:** **共同大腦記憶庫**。
    *   輸出：定義環境 (`08_production_notes.md`)。
9.  **[平面設計師 Agent](../agents/production/graphic_designer_agent.md):**
    *   **輸入:** 劇本中的道具需求。
    *   **動作:** 針對中文字道具 (如傳單、招牌) 決定「直接生成」或「留白後製」。
    *   **輸出:** 文字道具清單與 Prompt 策略 (`09_graphic_design.md`)。
10. **[服裝設計師 Agent](../agents/production/costume_designer_agent.md):**
    *   **輸入:** **共同大腦記憶庫** (角色設定)。
    *   輸出：定義服裝與造型細節 (`10_costume.md`)。
11. **[攝影指導 Agent](../agents/production/dop_agent.md):** 
    *   **輸入:** 分鏡表。
    *   **輸出:** 定義相機、鏡頭與 **運鏡參數 (Camera Movement)** (`11_camera.md`)。
12. **[燈光師 Agent](../agents/production/lighting_agent.md):** 定義光影 (`12_lighting.md`)。
13. **[特效指導 Agent](../agents/production/vfx_supervisor_agent.md):**
    *   **輸入:** 鏡頭序列 + 美術設定。
    *   輸出：定義粒子、光效與特殊元素 (`13_vfx.md`)。

### 第五步：後期製作 (Post-Production - 聲音與色彩)
14. **[音效與配樂師 Agent](../agents/post_production/sound_designer_agent.md):**
    *   **輸入:** 故事情緒 + 畫面內容。
    *   輸出：定義 BGM 與 SFX (`14_sound.md`)。
15. **[配音員 Agent](../agents/post_production/voice_actor_agent.md):** 
    *   **輸入:** 劇本中的角色對白。
    *   **限制:** **僅針對角色對白 (Dialogue Only)**，不處理旁白。
    *   輸出：定義聲音人設與情緒 (`15_voice.md`)。
16. **[調色師 Agent](../agents/post_production/colorist_agent.md):** 定義色彩 (`16_color.md`)。

### 第六步：提示詞優化 (Prompt Engineering)
17. **[提示詞工程師 Agent](../agents/core/prompt_engineer_agent.md):** 
    *   **輸入:** 所有視覺、動態與敘事 Agent 的產出。
    *   **動作:** 進行權重分配、負面提示添加與關鍵字精煉。
    *   **輸出:** 針對不同模型 (Midjourney, Stable Diffusion, Runway) 的優化 Prompt (`17_prompt_engineering.md`)。

### 第七步：品質控管與迭代 (QA & Iteration)
18. **[品管 Agent](../agents/core/qa_agent.md):** 審查每個 Clip。
    *   **標準:** 評分需達 9 分以上才可輸出。
    *   **動作:** 若未達標，退回給製作人進行修正 (Iteration)。
    *   **輸出:** QA 報告 (`18_qa_report.md`)。

### 第八步：最終輸出 (Final Output)
19. **[製作人 Agent](../agents/core/producer_agent.md):** 整合通過 QA 的資訊。
    *   **目標:** 建立最終的 Clip 檔案。
    *   **路徑:** `workspace/projects/<project_name>/clips/clip_xx.md`
    *   **格式:** 包含「結構化 Prompt」與「多模型優化 Prompt (MJ, SD, Runway)」。

---

## 最終 Prompt 組合 (Final Prompt Assembly)
製作人將針對**每個 Clip** 輸出以下兩種格式：

1.  **結構化 Prompt (邏輯檢視用):**
    `[導演風格] + [Consistency Block Character] + [Costume Details] + [Consistency Block Environment] + [該 Clip 的動作] + [燈光與氛圍] + [攝影參數] + [分鏡構圖] + [調色風格] --ar [長寬比]`

2.  **優化 Prompt (實戰生成用):**
    *   **Midjourney:** 針對藝術性與構圖優化。
    *   **Stable Diffusion:** 針對細節控制與 LoRA 優化。
    *   **Runway/Luma:** 針對動態描述與運鏡優化。
