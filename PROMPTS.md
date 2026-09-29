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

## 6. 视频 Prompt（4 条，核心转化素材）

给 Sora/Veo/Runway 类工具，每条 5-10 秒。

**V1 「Just turn it on」（品牌母视频，最优先拍/生成）**
> A hand presses the single power button on {PRODUCT} placed on a bedside table; the screen softly lights up with a photo of a golden retriever; within two seconds the dog's tail gives one gentle wag and the dog blinks — subtle, believable, not cartoonish. Camera static, warm dim bedroom light, 8 seconds, shallow depth of field, no text.

**V2 前后对比（Etsy listing 视频位）**
> Split attention shot: first a still photograph of a tabby cat on cream card paper on a table, then a dissolve to the same cat on the screen of {PRODUCT}, where the cat slowly blinks and shifts its head a few degrees. Warm window light, static camera, 8 seconds, no text, no sound cues implied.

**V3 拆箱送礼**
> Overhead shot: hands open a sage-green gift box with twine bow on warm cream linen, lift cream tissue to reveal {PRODUCT}, slide out a small cream card. Slow, tender, no faces, soft window light, 8 seconds, no text.

**V4 充电与安放（"忘记它的存在"）**
> A hand plugs a USB-C cable into the back of {PRODUCT}; the tiny LED indicator glows warm white; the frame is placed on an oak shelf between books; the screen settles into a looping subtle motion of a dog resting its head on a hand. Static camera, warm room, 10 seconds, no text.

---

## 7. 使用注意

- **一致性优先于单张完美**：工具支持 seed / reference image 就用（产品照做 reference），文字 prompt 只控镜头和场景。
- 你拍的**真产品图做底子**（图1-5 纯产品系列尽量实拍），AI 图主攻**场景和送礼**（图6-10、社媒、视频）——场景实拍成本高、AI 强，正好互补。
- 屏幕里的照片内容统一用：金毛（hero）、英短猫、法斗、老夫妇、Jack Russell——和品牌调性一致，避免"科技产品"感。
- 所有图**不放 logo、不放文字**（logo 后期合成），避免 AI 生成文字翻车。
- 批量生成后先过一遍：屏幕内容是否清晰、产品比例是否变形、有没有多出来的线缆/按键。
