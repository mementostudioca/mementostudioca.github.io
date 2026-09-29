# MEMENTO 产品图 Prompt 手册

用途：等收到产品后，把「PRODUCT LOCK」换成真实产品描述，下面所有 prompt 直接粘给 AI 生图工具（Midjourney / DALL·E / Flux 等）。
原则：**一张图只改镜头和场景，产品本体永远不变**——所以上面有统一的 PRODUCT LOCK 块，所有 prompt 都引用它。

---

## 0. PRODUCT LOCK（收到产品后填一次，全篇替换用）

收到产品后把下面这段换成真实描述（尺寸、颜色、材质、屏幕占比、接口位置、充电指示灯位置）：

> A minimal portable photo frame, approximately 8 inches wide, matte cream-white recycled plastic shell, thin rounded corners, slim integrated base stand, 7-inch photo display taking up most of the front face, no visible logo, one small USB-C port on the back edge, one tiny LED charging indicator near the bottom edge

（所有 prompt 中 `{PRODUCT}` 都指这一段。生图工具支持 reference image 的（如 Midjourney --cref / Flux 图生图）：用你拍的纯产品图做 reference，效果远好于纯文字。）

## 1. STYLE LOCK（每条 prompt 末尾都拼上）

> warm editorial product photography, soft diffused natural window light, cream and warm beige palette, shallow depth of field, 35mm film look, premium minimal aesthetic, generous negative space, no studio flash, no harsh shadows

## 2. NEGATIVE（负面提示，工具支持就加）

> no text, no watermark, no visible brand logo, no smartphone, no app interface, no Wi-Fi symbol, no wires or cables in frame, no clutter, no plastic shine, no oversaturated colors, no people facing camera with full face, no AI artifacts

---

## 3. Etsy Listing 十图（全部 1:1，1080x1080）

Etsy 最多 10 张 + 1 视频。顺序即上传顺序。

**图1 主图（决定点击率）— 纯白奶油底 hero**
> Hero product shot of {PRODUCT} standing at a slight three-quarter angle on a seamless warm cream background, screen showing a photo of a golden retriever puppy looking at the camera, soft diffused window light from the left, product fills 80% of frame, {STYLE} 1:1

**图2 正面平视 — 让屏幕内容说话**
> Front-on straight shot of {PRODUCT} on a seamless warm cream background, screen clearly showing a photo of a tabby cat sleeping in a sunbeam, no angle, product perfectly centered, {STYLE} 1:1

**图3 侧面/背面 — 展示轻薄 + USB 口**
> Side profile shot of {PRODUCT} leaning on its base stand, showing the thin edge and the small USB-C port, warm cream background, one soft shadow, {STYLE} 1:1

**图4 顶视图**
> Top-down view of {PRODUCT} lying flat on warm cream linen fabric, screen showing a photo of a dog resting its head on a person's hand, soft even light, {STYLE} 1:1

**图5 充电细节 macro**
> Macro detail shot of the bottom edge of {PRODUCT}, the tiny LED charging indicator glowing soft warm white, USB-C cable just entering the port, shallow depth of field, warm cream background, {STYLE} 1:1

**图6 包装全家福 — Gift Box listing 主图**
> Flat lay of the MEMENTO gift box: a matte sage-green box with a small twine bow, {PRODUCT} nestled in cream tissue, a blank cream card with a thin ink line border, sprig of dried eucalyptus, on warm cream linen, soft window light, {STYLE} 1:1

**图7 场景：床头**
> {PRODUCT} standing on a wooden bedside table next to a small ceramic lamp with a warm glow, soft morning light through sheer curtains, the screen shows a photo of an elderly woman and grandchild, cozy and quiet, {STYLE} 1:1

**图8 场景：书架**
> {PRODUCT} on a light oak shelf between a stack of two cloth-bound books and a small ceramic vase with dried grasses, screen showing a photo of a French bulldog, warm afternoon light, {STYLE} 1:1

**图9 送礼场景：双手递交**
> Two hands gently offering the closed sage-green gift box with twine bow toward the camera, warm cream background, shallow depth of field, soft window light, no faces, {STYLE} 1:1

**图10 宠物场景：狗在框旁**
> {PRODUCT} on the edge of a sofa, screen showing a photo of the same golden retriever; the real golden retriever sits beside the sofa looking at the camera, tongue slightly out, warm living room, soft light, {STYLE} 1:1

---

## 4. 网站替换图（对应 index.html 五个槽位）

现在网站用 Unsplash 预览图，收到产品后按下面替换 `assets/` 里对应文件。

**frame-hero.jpg — 16:9（暗区大图，1600x900 起）**
> {PRODUCT} on a dark walnut side table beside a warm lit table lamp, deep charcoal-ink background, screen glowing softly with a photo of a dog and its owner, cinematic soft light, {STYLE} 16:9

**dog-still.jpg + Living 侧 — 4:3（双联，各 1200x900）**
> Close-up of a golden retriever's face in a photograph printed on cream card paper, held flat on a wooden table, soft window light, {STYLE} 4:3

> Close-up of the same golden retriever's face inside the screen of {PRODUCT}, the dog's tail blurred in a soft motion, warm room, shallow depth of field, {STYLE} 4:3

（双联两张必须用同一只狗——左右对比才是"Still → Living"。）

**dog-product.jpg — 1:1（Living Memory 产品行）**
> {PRODUCT} at slight angle on seamless warm cream background, screen showing a photo of a Jack Russell terrier with ears up, {STYLE} 1:1

**frame-product.jpg — 1:1（Frame 产品行）**
> {PRODUCT} front view on seamless warm cream background, screen showing a photo of an elderly couple dancing in a kitchen, {STYLE} 1:1

**gift-box.jpg — 1:1（Gift Box 产品行）**
> The closed sage-green MEMENTO gift box with twine bow and a small cream card tucked under the twine, on warm cream linen with a sprig of roses, soft window light, {STYLE} 1:1

---

## 5. 社媒素材

**4:5（IG feed / Etsy 备用）**
> {PRODUCT} on a marble-topped vanity, a perfume bottle and a small mirror beside it, screen showing a photo of a young woman laughing, soft morning light, {STYLE} 4:5

**9:16（TikTok / Reels 封面与静帧）**
> {PRODUCT} being gently placed by a hand onto a windowsill, screen lighting up with a photo of a cat, morning light streaming in, quiet and tender, {STYLE} 9:16

---

## 6. 视频 Prompt（10 条，按渠道分配）

给 Sora/Veo/Runway/Kling 类工具。通用参数：24fps、1080p 起、**生成时不加文字和音乐**（字幕 BGM 后期加）。
**屏幕合成技巧**：屏幕里的照片先让 AI 生成"一张狗/猫的照片"占位即可，**后期用真照片替换屏幕内容**（CapCut/After Effects 做屏幕合成，比让 AI 一次到位稳得多，也保证双联对比用同一张照片）。

**渠道分配**：
- V2 → Etsy listing 视频位：1:1，≤15 秒
- V1/V3/V5/V6/V7/V8/V10 → TikTok/Reels：9:16，7-10 秒
- V4/V9 → 网站 + 社媒：16:9
- 每条都留 0.5 秒首尾黑场或静态帧，方便剪

**NEGATIVE（视频通用，拼在末尾）**
> no text, no subtitles, no watermark, no visible logo, no smartphone, no app interface, no Wi-Fi symbol, no fast cuts, no cartoonish motion, no extra fingers, no plastic shine, no over blur

**V1 「Just turn it on」— 品牌母视频（最优先，9:16 / 8s）**
> A hand presses the single power button on {PRODUCT} on a bedside table in a dim warm bedroom. The screen softly lights up with a photo of a golden retriever. Within two seconds the dog's tail gives one gentle wag and the dog blinks — subtle, believable, not cartoonish. Static camera with a slow push-in, warm practical lamp light, shallow depth of field, tender and quiet, 8 seconds.

**V2 前后对比 — Etsy listing 视频位（1:1 / 10s）**
> Close-up: a printed photograph of a tabby cat on cream card paper rests on a wooden table. Slow dissolve into {PRODUCT} on the same table, its screen showing the same cat, which slowly blinks and shifts its head a few degrees. Warm window light, static camera, no hands after the dissolve, 10 seconds.

**V3 拆箱 — Gift Box listing 视频（9:16 / 10s）**
> Overhead shot of hands opening a sage-green gift box with a twine bow on warm cream linen. Fingers lift cream tissue paper, revealing {PRODUCT} nestled inside, then slide out a small cream card. Slow, tender, no faces, soft window light, 10 seconds.

**V4 充电与安放 — "Just place it. Forget about it"（16:9 / 10s）**
> A hand plugs a USB-C cable into the back of {PRODUCT}; the tiny LED indicator glows warm white. The frame is carried to an oak shelf between books and set down. The screen settles into a subtle looping motion of a dog resting its head on a person's hand. Static camera, warm afternoon room, 10 seconds.

**V5 宠物 POV — 情感钩子（TikTok，9:16 / 8s）**
> Low angle at floor level: a golden retriever sits beside a sofa where {PRODUCT} rests on the edge, its screen showing a photo of the same dog. The real dog watches the screen, tail gives one slow wag, ears flick. Warm living room, soft light, intimate and quietly funny, 8 seconds.

**V6 送礼瞬间 — Gift 定位核心（TikTok，9:16 / 10s）**
> A young woman's hands place the closed sage-green gift box with twine bow into an older woman's hands; the older woman's hands gently close around the box, thumbs brushing the twine. No faces, only hands and the box, warm kitchen background softly blurred, tender, 10 seconds.

**V7 书架循环 — 美学空镜（IG Reels，9:16 / 10s，可无缝 loop）**
> {PRODUCT} on an oak shelf between cloth-bound books and a small ceramic vase with dried grasses. Morning light slowly shifts across the wall. On the screen, a French bulldog's ears twitch and its eyes blink — the only motion in the frame. Static camera, quiet, warm, 10 seconds, designed to loop seamlessly.

**V8 节点：冬日/圣诞（TikTok，9:16 / 10s）**
> A cozy winter scene: {PRODUCT} on a windowsill, soft grey light outside, a small candle and a sprig of pine beside it. On the screen, an elderly couple dancing in a kitchen, the man's hat tilting slightly as if caught mid-motion. Warm golden interior, soft, nostalgic, 10 seconds.

**V9 「No app」证明 — 产品力演示（16:9 / 10s）**
> Wide shot of a calm bright living room. A hand plugs {PRODUCT} into a wall power point with a short USB-C cable; no phone, no app, no other devices anywhere in frame. The screen lights up and settles into a subtle motion of a cat blinking. The hand walks away. Static camera, bright warm daytime light, 10 seconds.

**V10 Remembrance — 静帧情感（TikTok，9:16 / 10s）**
> A quiet bedside at dusk: {PRODUCT} on the nightstand, screen showing a photo of an elderly dog resting in a sunny spot, the dog's breathing rising and falling — the subtlest possible motion. A hand rests a cup of tea on the table beside it. Deeply quiet, warm low light, 10 seconds.

---

## 7. 使用注意

- **一致性优先于单张完美**：工具支持 seed / reference image 就用（产品照做 reference），文字 prompt 只控镜头和场景。
- 你拍的**真产品图做底子**（图1-5 纯产品系列尽量实拍），AI 图主攻**场景和送礼**（图6-10、社媒、视频）——场景实拍成本高、AI 强，正好互补。
- 屏幕里的照片内容统一用：金毛（hero）、英短猫、法斗、老夫妇、Jack Russell——和品牌调性一致，避免"科技产品"感。
- 所有图**不放 logo、不放文字**（logo 后期合成），避免 AI 生成文字翻车。
- 批量生成后先过一遍：屏幕内容是否清晰、产品比例是否变形、有没有多出来的线缆/按键。
