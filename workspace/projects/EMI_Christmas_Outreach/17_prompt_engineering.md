# 提示詞優化 (Prompt Engineering)

### Clip 1
*   **鏡頭類型:** Wide Shot to Close Up to Medium Shot (Montage)
*   **優化策略:** 強化 Alex 的疲憊感與環境的寒冷，使用蒙太奇關鍵字。
*   **Midjourney Prompt:**
    `[Cinematic Shot]::2, [Alex] a weary architect in his 30s, tired eyes, dark circles, stubble beard, wearing a dark grey wool coat, dark scarf, carrying a distressed brown leather messenger bag stuffed with blueprints::1.5, walking against crowd, heavy snow falling, stumbling, exhausted expression, [City Street] modern metropolis at night, cold blue and teal neon lights, wet pavement, crowded, bokeh traffic lights::0.8, High Key lighting, deep shadows, Arri Alexa 65, Panavision Anamorphic, Blue flares, Teal & Orange color grading --no text, watermark, blurry, deformed, cartoon, 3d render, happy, sunny --ar 2.39:1`
*   **Stable Diffusion Prompt:**
    `(masterpiece, best quality), (photorealistic:1.2), [Alex] a weary architect in his 30s, tired eyes, dark circles, stubble beard, wearing a dark grey wool coat, dark scarf, carrying a distressed brown leather messenger bag stuffed with blueprints, walking against crowd, heavy snow falling, stumbling, exhausted expression, [City Street] modern metropolis at night, cold blue and teal neon lights, wet pavement, crowded, bokeh traffic lights, High Key lighting, deep shadows, Arri Alexa 65, Panavision Anamorphic, Blue flares, Teal & Orange color grading, <lora:cinematic:0.8>, (cold atmosphere:1.1)`
*   **Runway/Luma Prompt (Natural Language):**
    `Wide shot of Alex, a weary architect, walking against a crowd on a snowy city street at night. Fast cut to close up of his boots trudging in slush. Fast cut to medium shot of him leaning against a wall, exhaling vapor. The lighting is high contrast with cold blue and teal neon lights. Cinematic, 4k, slow motion.`

### Clip 2
*   **鏡頭類型:** OTS to POV to Close Up (Montage)
*   **優化策略:** 強化前景與背景的對比，利用框中框構圖，強調眼神光。
*   **Midjourney Prompt:**
    `[Cinematic Shot]::2, [Alex] from behind, wearing dark grey wool coat::1.5, looking at [Church Interior] entrance, glowing warm light, contrast between cold street and warm door, [City Street] modern metropolis at night, heavy snow falling::0.8, Framing within a frame, Dirty frame, Low angle, Rack focus, High Key lighting, deep shadows, Arri Alexa 65, Panavision Anamorphic, Blue flares, Teal & Orange color grading --no text, watermark, blurry, deformed, cartoon, 3d render --ar 2.39:1`
*   **Stable Diffusion Prompt:**
    `(masterpiece, best quality), (photorealistic:1.2), [Alex] from behind, wearing dark grey wool coat, looking at [Church Interior] entrance, glowing warm light, contrast between cold street and warm door, [City Street] modern metropolis at night, heavy snow falling, Framing within a frame, Dirty frame, Low angle, Rack focus, High Key lighting, deep shadows, Arri Alexa 65, Panavision Anamorphic, Blue flares, Teal & Orange color grading, <lora:cinematic:0.8>`
*   **Runway/Luma Prompt (Natural Language):**
    `Over-the-shoulder shot of Alex looking across a snowy street at a warm, glowing church entrance. Transition to POV shot of the glowing cross through snow. Fast cut to close up of Alex's face with golden reflection in his eyes. Cinematic, 4k.`

### Clip 3
*   **鏡頭類型:** Tracking to Medium to Close Up (Montage)
*   **優化策略:** 強化光線的變化與擁抱的溫暖感。
*   **Midjourney Prompt:**
    `[Cinematic Shot]::2, [Alex] entering [Church Interior], dropping bag, being embraced by silhouette of light::1.5, tension leaving body, [Church Interior] warm golden interior, wooden pews, soft candlelight, amber ambient lighting, peaceful atmosphere, sanctuary, volumetric lighting::1.2, Symmetrical composition, Silhouette foreground, Eye-level, Dolly In, Warm golden lighting, soft diffusion, Arri Alexa 65, Panavision Anamorphic, Creamy bokeh, Teal & Orange color grading --no text, watermark, blurry, deformed, cartoon, 3d render, scary, ghost --ar 2.39:1`
*   **Stable Diffusion Prompt:**
    `(masterpiece, best quality), (photorealistic:1.2), [Alex] entering [Church Interior], dropping bag, being embraced by silhouette of light, tension leaving body, [Church Interior] warm golden interior, wooden pews, soft candlelight, amber ambient lighting, peaceful atmosphere, sanctuary, volumetric lighting, Symmetrical composition, Silhouette foreground, Eye-level, Dolly In, Warm golden lighting, soft diffusion, Arri Alexa 65, Panavision Anamorphic, Creamy bokeh, Teal & Orange color grading, <lora:cinematic:0.8>`
*   **Runway/Luma Prompt (Natural Language):**
    `Tracking shot of Alex pushing open church doors, light flooding in. Fast cut to medium shot of him dropping his bag and being embraced by a warm silhouette. Fast cut to slow motion of snow melting on his coat. Cinematic, 4k.`

### Clip 4
*   **鏡頭類型:** Extreme Close Up to Wide Shot (Montage)
*   **優化策略:** 強化面部微表情與眼神光，以及最後的拉遠鏡頭。
*   **Midjourney Prompt:**
    `[Cinematic Shot]::2, [Alex] close up face, crying tears of relief, peaceful expression, warm candlelight reflection in eyes::2, [Church Interior] warm golden interior, wooden pews, soft candlelight::0.5, Extreme Close Up, Golden ratio, Shallow depth of field, Bokeh background, Static shot, Warm golden lighting, soft diffusion, Arri Alexa 65, Panavision Anamorphic, Creamy bokeh, Teal & Orange color grading --no text, watermark, blurry, deformed, cartoon, 3d render, sad, angry --ar 2.39:1`
*   **Stable Diffusion Prompt:**
    `(masterpiece, best quality), (photorealistic:1.2), [Alex] close up face, crying tears of relief, peaceful expression, warm candlelight reflection in eyes, [Church Interior] warm golden interior, wooden pews, soft candlelight, Extreme Close Up, Golden ratio, Shallow depth of field, Bokeh background, Static shot, Warm golden lighting, soft diffusion, Arri Alexa 65, Panavision Anamorphic, Creamy bokeh, Teal & Orange color grading, <lora:cinematic:0.8>`
*   **Runway/Luma Prompt (Natural Language):**
    `Extreme close up of Alex's face crying tears of relief. Slow zoom out to wide shot of him sitting alone in the warm, glowing church sanctuary. Cinematic, 4k.`
