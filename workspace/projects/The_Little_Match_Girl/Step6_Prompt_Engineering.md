# Step 6: Prompt Engineering (提示詞優化)

## 17. 提示詞工程師 Agent (Prompt Engineer)

### 提示詞策略
*   **通用權重:** `(masterpiece, best quality:1.2), (cinematic lighting, atmospheric:1.1)`
*   **負面提示:** `(worst quality, low quality:1.4), deformation, bad anatomy, disfigured, cartoon, 3d render, sketch, drawing, anime, text, watermark`
*   **模型優化:**
    *   **Midjourney:** `--v 6.0 --style raw`
    *   **Stable Diffusion:** `8k, uhd, dslr`
    *   **Runway/Luma:** 動態描述 `camera moves forward`, `snow falling`

### 綜合 Prompt 草稿
*   **Clip 01:** `cinematic film still, 8yo girl with messy blonde hair and tattered brown coat walking in heavy snowstorm on 19th century victorian street, holding matches, shivering, bare feet, cold blue atmosphere, night time, gas lamps in background, handheld camera style, emotional, photorealistic, 8k --ar 16:9 --v 6.0 --style raw`
*   **Clip 02:** `cinematic film still, extreme close up of 8yo girl face illuminated by a single lit match, glowing warm orange light on face, hope in eyes, dark cold snowy background, brick wall, chiaroscuro lighting, high contrast, emotional, detailed eyes, photorealistic, 8k --ar 16:9 --v 6.0 --style raw`
*   **Clip 03:** `cinematic film still, vision of a magnificent christmas feast and glowing christmas tree, roast goose, candles, warm golden lighting, magical atmosphere, soft focus edges, dreamlike, seen from perspective of a poor girl, contrast with cold reality, photorealistic, 8k --ar 16:9 --v 6.0 --style raw`
*   **Clip 04:** `cinematic film still, 8yo girl hugging a kind elderly grandmother, surrounded by blinding divine warm light, ascending to heaven, snow fading away, ethereal atmosphere, emotional, spiritual, peace, photorealistic, 8k --ar 16:9 --v 6.0 --style raw`
*   **Clip 05:** `cinematic film still, morning light, 8yo girl sitting frozen in a snowy corner, peaceful smile on face, eyes closed, snow piled around her, 19th century street, sad but beautiful, tragedy, photorealistic, 8k --ar 16:9 --v 6.0 --style raw`
