# Photo Shoot Method

Use this reference to turn portrait ideas into stable AI photography prompts with real shoot logic.

## Core Principle

Do not write a shopping list of pretty words. Write a shoot: where it is photographed, what the camera sees, how the subject occupies the space, what the light does, and why the styling belongs there.

Good prompts are often not the longest prompts. They read like a shooting cheat sheet for a photographer, stylist, makeup artist, props team, lighting assistant, and retoucher.

## The Eight-Part Prompt Check

1. **Image format and topic**: Aspect ratio, realistic photography, and concrete photo-shoot theme.
2. **Imaging method**: Device or rendering behavior, such as Fuji outdoor film color, Nikon realism, phone snapshot, direct-flash CCD, soft-mist studio, or magazine editorial.
3. **Texture lock**: The image's photographic defects and finishing: near-lens blur, flare, highlight bloom, grain, haze, lifted shadows, muted or saturated film color, and anti-AI-polish constraints.
4. **Adult subject and face**: Clearly adult fictional subject, face shape, temperament, hairstyle, and real skin texture.
5. **Makeup anchor**: One short makeup identity plus two or three details. Keep it coherent.
6. **Wardrobe**: Wearable clothing, color, material, silhouette, accessories, and relation to theme.
7. **Scene layers**: Foreground, subject plane, background, plus optional props.
8. **Camera, pose, light, and constraints**: Distance, crop, lens feeling, pose skeleton, light source direction, highlight/shadow result, and practical guardrails.

## Article-Example Texture Lock

When the user wants the texture from the sample article images, do not merely write "film", "realistic", or "atmosphere". Add a visible texture lock that prevents the model from cleaning the image into a generic AI beauty render.

Use these controls:

- **Foreground pressure**: A near object should touch the lens, blur heavily, and occupy 20-40% of the frame when the composition supports it. Use flowers, leaves, fruit, gauze curtain, desk edge, hair strands, or fabric.
- **Optical imperfection**: Ask for soft focus, mild lens bloom, halation around backlit edges, slight veiling glare, light leak feeling, or low-contrast diffusion. Do not ask for all at once unless the scene is intentionally hazy.
- **Light consequences**: Specify exactly what the light does: leaf-hole dappled marks on skin, rim-lit hair, blown but not pure-white highlights, dusty beams through curtains, hard flash shadow, or milky skylight wash.
- **Film finish**: Add fine grain, lifted blacks, restrained sharpening, local softness, gentle color shift, and non-HDR contrast. Avoid "8K ultra sharp", "perfect commercial retouch", and "crystal clear".
- **Skin and makeup**: Keep skin touchable and slightly imperfect. Do not over-smooth. Makeup should connect to props and light, such as peach blush with peach props or muted rose lips inside a gray-green old room.
- **AI cleanup blocker**: Explicitly reject AI-render polish, plastic skin, studio-perfect sharpness, HDR, hyper-clean commercial retouch, and every prop being crisp at the same time.

Texture-lock snippets:

```text
真实摄影的不完美质感：轻微胶片颗粒、低对比、暗部抬起、局部柔焦、逆光边缘晕开，画面不要过度锐利，不要HDR，不要商业棚拍精修。
```

```text
前景物体贴近镜头并明显虚化，占据画面约三分之一，让镜头像真的藏在场景里；主体清晰但不过度锐化，背景和道具允许被浅景深、雾气和眩光吞掉。
```

```text
强自然光穿过树叶形成筛孔光斑，落在皮肤、草帽、发丝和衣料上；高光轻微溢出但不要死白，皮肤保留细小颗粒和真实质感。
```

## Scene Layers

Avoid empty labels like "indoor", "outdoor", or "studio". Build spatial density:

- **Foreground**: flowers, leaves, curtain, desk edge, hair strand, white bloom, fruit branch, glass reflection, soft fabric.
- **Subject plane**: where the person is and what they are doing.
- **Background**: window, blackboard, orchard path, old bed, dense vegetation, studio backdrop, office at night.

Do not require every prop to appear. Many props should function as an atmosphere library:

```text
道具不需要全部出现，只根据构图需求选取，保持画面自然。
```

Useful scene examples:

- Old study: old wooden desk, birdcage, small yellow-green bird, scattered grain, old books, hand-copied paper, scrolls, ink stone, porcelain fruit plate, peaches, bamboo curtain, lattice window, old daybed, gauze curtain moving in backlight.
- Summer orchard: leaves, branches, green fruit, vines, bamboo basket, fruit basket, straw hat, juice with straw, natural path, dense vegetation; the camera feels hidden between fruit-tree leaves.
- Daisy field: daisies, straw hat, large white flowers in foreground, mottled shade, blue sky, cumulus clouds, grass, picnic cloth, low camera, nearby flowers blurred.

## Imaging Method

Do not stop at "cinematic", "high-end", or "atmospheric". Translate style into capture behavior:

- **Fuji-style outdoor film**: saturated blue sky, warm skin, visible grain, lively greens, summery contrast.
- **Nikon realism**: clean realistic detail, natural skin texture, restrained color, credible lens focus.
- **Phone snapshot**: close everyday distance, imperfect crop, casual motion, spontaneous expression.
- **Direct-flash CCD**: hard frontal flash, shiny skin highlights, crisp shadow behind subject, nightlife or office immediacy.
- **High-key soft-mist studio**: high exposure, low contrast, soft wraparound front and side-front light, Pro-Mist-like bloom, highlights slightly spilling but not pure white.
- **Magazine editorial**: deliberate crop, controlled styling, confident pose, polished but believable retouch.

For the sample-like outdoor look, prefer:

```text
富士户外胶片色彩，高饱和绿叶和青蓝天空，皮肤偏暖，白色衣物高光发亮，细胶片颗粒，轻微眩光，局部失焦，不要HDR锐化。
```

For the old-room sample look, prefer:

```text
低对比青灰雾化胶片质感，窗外逆光被竹帘和白纱打散，空气里有灰尘和雾，暗部柔软抬起，木头和纸张质感旧而潮，亮部轻微溢出但不死白。
```

For the close peach snapshot look, prefer:

```text
近距离自拍式广角抓拍，巨大虚化桃子贴近镜头占据前景，脸部轻微过曝，边缘高光晕开，粉橙前景和桃粉腮红互相呼应，画面甜但不是塑料磨皮。
```

Always specify where the light comes from, where it lands, and what it causes: soft bloom, hard shadow, dappled light, rim light, flare, grain, or edge blur.

## Gufeng Portrait Decisions

When handling gufeng, hanfu, Chinese period-style portraits, or old-room ancient-style photo prompts, first decide the route. Do not mix all routes in one prompt.

### Route 1: Modern Gufeng Photography

Use this when the user wants beauty, shareability, stable faces, and sample-like portrait appeal.

- Face can be more camera-friendly and polished.
- Clothing can be improved hanfu or styled period-inspired wardrobe.
- Makeup can be refined but restrained.
- Light can be photographic: window backlight, Pro-Mist-like bloom, diffusion, film grain.
- Best for commercial/social article images.

Prompt route phrase:

```text
真实摄影，现代古风写真，改良汉服，胶片质感，镜头穿过纱帘和桌案前景拍摄，人物妆容精致但克制。
```

### Route 2: Ancient-Life Snapshot

Use this when the user asks for "really ancient", documentary, living-history, non-studio, or candid period life.

- Face should be less modern-beauty optimized.
- Makeup should be very light or nearly invisible.
- Wardrobe should be simpler and less glossy.
- Action should come from daily life: writing, grinding ink, sorting herbs, making tea, opening a curtain, carrying books.
- Avoid obvious modern studio lighting, idol makeup, and influencer face.

Prompt route phrase:

```text
古代生活场景的电影化纪实画面，服饰朴素，妆容极淡，人物像在真实生活中整理纸页或煮茶，不看镜头，没有现代影楼摆拍感。
```

### Writing Gufeng Faces

Do not write only "classical beauty" or "beautiful hanfu girl". Lock face temperament, geometry, hair, and makeup anchor.

Modern gufeng face:

```text
一位明确成年的虚构东亚女性，清冷小鹅蛋脸，眉眼细长但柔和，鼻梁自然，唇形小而清晰，黑发低挽，几缕碎发贴在脸侧。淡雅古典妆，柔雾底妆，低饱和豆沙唇，眉眼干净，保留真实皮肤纹理。
```

More shareable Chinese social-media beauty version:

```text
一位明确成年的虚构中国女性，精致但不夸张的小鹅蛋脸，清透杏眼，柔和鼻梁，干净下颌线，黑发低挽并有自然碎发。清透古风妆，轻薄底妆，淡粉眼下腮红，自然卧蚕，低饱和玫瑰豆沙唇，皮肤真实但上镜。
```

Ancient-life face:

```text
一位明确成年的虚构东亚女性，脸型柔和朴素，眉眼安静，不是现代网红妆容，黑发简单束起，妆感极淡，皮肤保留真实纹理、细小毛孔和生活感。
```

Use reference images only when face consistency matters. If the user only wants gufeng atmosphere, text is usually enough. If using face references, do not imitate a real celebrity, influencer, or private person identity; describe a fictional face direction instead.

### Writing Gufeng Light

Write light directly in the prompt. Do not rely on post-processing to rescue flat lighting. Use source + modifier + landing area + result.

Old-room window light:

```text
窗外白雾逆光从侧后方透过竹帘和窗棂进入房间，落在纱帘、纸张边缘、发丝和木案上，形成柔和光束、轻微灰尘颗粒、暗部抬起和旧木头潮气感。
```

Garden or orchard light:

```text
强自然光穿过树叶形成筛孔光斑，落在脸颊、发丝、衣料和手背上，高光轻微溢出但不死白，皮肤保留细小颗粒。
```

Indoor candle or lantern light:

```text
低位暖色烛光从桌面侧前方照来，落在手指、下颌、纸页和杯沿上，背景保持青灰暗部，形成暖冷对比、局部柔焦和轻微烟气。
```

### Avoiding AI Skin in Gufeng

Use anti-cleanup texture controls. Avoid "8K", "perfect skin", "ultra sharp", "flawless", "commercial retouch", and "HDR".

Good texture lock:

```text
真实摄影的不完美质感：轻微胶片颗粒、低对比、暗部抬起、局部柔焦、逆光边缘晕开，皮肤保留真实纹理、细小毛孔和轻微瑕疵，不要过度磨皮，不要塑料皮肤，不要HDR，不要商业棚拍锐化。
```

Depth and cleanup blocker:

```text
主体清晰但不过度锐化，背景和道具允许被浅景深、雾气和眩光吞掉，不要所有道具都同样清晰。
```

### Gufeng Expressions

Write micro-expression and gaze relationship instead of broad emotion words.

Quiet and cold:

```text
低头垂眼，嘴唇自然放松，神情安静疏离，像正在想事情，不强求看镜头。
```

Soft:

```text
眼神落在手中的纸页或花枝上，唇角极轻微放松，表情温和但不过度甜美。
```

Story-like pause:

```text
视线越过窗外光线，脸上有轻微停顿感，像刚从动作中安静下来。
```

Avoid high-risk expression/action bundles such as seductive over-the-shoulder gaze, large head turn, exaggerated wink, twisted torso, or looking back while walking away unless the user explicitly asks and accepts anatomy risk.

### Gufeng Quick Template

```text
3:4 竖图，真实摄影，现代古风旧阁书案写真，低对比青灰雾化胶片质感，暗部抬起，柔焦，轻微颗粒。

一位明确成年的虚构东亚女性，清冷小鹅蛋脸，眉眼细长柔和，黑发低挽，几缕碎发贴在脸侧。淡雅古典妆，柔雾底妆，低饱和豆沙唇，眉眼干净，保留真实皮肤纹理。

浅青灰色改良汉服搭配米白长裙，衣料有细密织纹和轻微旧感，玉色发簪和简洁耳坠，避免影楼感和过度华丽。

前景是贴近镜头的旧木案边缘、手抄纸、半卷卷轴和白色纱帘虚影；人物坐在书案旁，手指轻触纸页，低头垂眼，嘴唇自然放松，不强求看镜头。背景有竹帘、窗棂、古书、砚台、旧瓷果盘，道具不需要全部出现，只根据构图需求选取。

窗外白雾逆光从侧后方透过竹帘和窗棂进入房间，落在纱帘、纸张边缘、发丝和木案上，形成柔和光束、轻微灰尘颗粒和旧木头潮气感。
```

## Makeup Anchors

Use the smallest recognizable makeup identity. If one sentence cannot describe the makeup, simplify it.

Good anchors:

- Peach oxygen look: peach-pink sweet makeup, creamy skin, under-eye blush, watery peach lip, fruit hair string, ribbon accessory.
- Soft orchid mist: translucent creamy nude makeup, peach under-eye blush, natural aegyo-sal, watery pale-pink lips.
- Blackboard office flash: cool fair skin, direct-flash career makeup, clean eye line, low-saturation lip.
- Summer creek flower crown: garden-fairy peach-pink makeup, sunlit cheeks, lightweight shimmer.

Avoid conflicting makeup directions, such as cold detached mood plus sweet energetic idol makeup, or Western heavy glam plus transparent Japanese magazine softness, unless the request intentionally asks for contrast.

## Pose Skeletons

Write a body logic, not a rigid anatomy exam.

Stable pose skeletons:

- Lowered eyes, fingertips lightly touching petals on the table.
- Sitting in grass under sunlight, not required to look at camera.
- Running through orchard leaves, smiling sideways with head and shoulders aligned.
- Holding a peach close to the face in a playful close snapshot.
- Standing beside a whiteboard, one hand on the desk, body slightly angled, direct flash, gaze to camera.

High-risk poses:

- Looking back over the shoulder with the body facing away.
- Large neck turns while torso twists in the opposite direction.
- Multiple simultaneous actions: bending, reaching, twisting, turning back, and looking at camera.
- Dance-like poses where hands, feet, and torso all require exact anatomy.

Use this guardrail when relevant:

```text
头部、肩膀和躯干方向保持自然一致，不做大幅扭头回望。
```

## Controlled Variation

Lock the scene, light, and styling. Let the image breathe through controlled variables:

- camera distance may vary
- gaze may or may not meet the camera
- expression may be natural and random within the mood
- foreground can include blurred grass, flowers, hair, curtain, or fabric
- optional props do not all need to appear

This prevents repeated images from becoming clones while preserving the visual direction.

## Copy-Ready Template

```text
[画幅]，真实摄影，[具体写真主题]，[具体成像方式]

[质感锁：真实摄影的不完美、前景压镜头、光学瑕疵、胶片后期、反AI精修约束]

一位明确成年的虚构[人物方向]，[脸型与气质]，[发型]，[妆容锚点与两三个细节]，保留轻微真实皮肤质感。

[服装造型]，[颜色]，[材质]，[配饰]，整体真实可穿，并与[主题/场景]互相呼应。

[前景贴近镜头并明显虚化，可占画面20%-40%]，[人物所在位置与动作]，[背景]，[道具库；不需要全部出现，只根据构图需求选取]。

[镜头距离与构图]，[镜头角度/裁切/景深]，[动作骨架]，[视线方向]，头肩身体方向自然一致。

[光线来源]从[方向]照来，落在[主体/道具/背景]上，产生[高光/阴影/眩光/颗粒/柔雾/硬闪]效果，整体[色彩和质感]。
```

Negative prompt baseline:

```text
不要真实品牌 logo，不要未成年人或年龄模糊，不要暴露生殖器或乳头，不要性行为，不要塑料皮肤，不要过度磨皮，不要商业棚拍锐化，不要HDR，不要8K超清精修感，不要AI渲染感，不要手指畸形，不要多余肢体，不要断裂手脚，不要大幅扭头回望，不要身体结构反人类，不要道具堆砌，不要所有道具都清晰罗列，不要乱码文字，不要水印。
```

## Example: High-Key Soft Orchid Studio

```text
3:4 竖图，真实摄影，高调奶油柔雾棚拍肖像，轻微胶片颗粒，低对比，柔焦高光，不要8K超清精修感

一位明确成年的虚构东亚女性，小鹅蛋脸，安静柔和气质，深棕黑发低盘发，耳后别一朵柔粉色兰花。清透奶油裸妆，桃粉眼下腮红，自然卧蚕，水润浅粉唇，保留轻微真实皮肤质感。

白色挂脖褶皱上衣，珍珠耳钉，细手链，整体干净真实可穿，白色布料、珍珠和兰花共同服务于柔雾棚拍的轻盈感。

浅暖灰色棚拍背景，白色桌面，粉色兰花贴近镜头形成大面积前景柔焦，约占画面四分之一到三分之一，人物坐在桌边，指尖轻触兰花花瓣，桌面可有少量花瓣和浅色织物，不需要全部道具出现。

中近距离半身人像，轻微俯视但保持亲近距离，浅景深，人物低头垂眼，不强求看镜头，头肩身体方向自然一致。

大面积柔光从正前方和侧前方包裹人物，落在手、花、白色桌面和脸侧，形成低对比、亮部轻微溢出但不死白的柔雾效果，像隔着 Pro-Mist 柔雾滤镜拍摄。
```

## Example: Summer Orchard Oxygen Snapshot

```text
3:4 竖图，真实摄影，夏日果园氧气感写真，富士户外胶片色彩，高饱和绿叶和青蓝天空，细胶片颗粒，局部失焦，不要HDR锐化

一位明确成年的虚构东亚女性，圆润小鹅蛋脸，明亮自然气质，深棕长发半扎并有细碎发丝。桃粉氧气妆，奶油肌，粉桃腮红，水润桃粉唇，保留真实皮肤纹理。

浅白色棉麻吊带外搭薄开衫，草帽系带，细小果实发串，服装轻便真实，和果园、桃色妆面、夏日逆光互相呼应。

前景有贴近镜头的虚化树叶、白色小花和几颗青色果实，明显遮挡画面上方和边缘，可占画面三分之一；人物在果树枝叶之间经过，背景是自然小路、藤蔓和浓密植被。竹篮、果篮、果汁吸管、野餐布作为氛围道具，不需要全部出现，只根据构图需求选取。

中近距离抓拍，镜头像藏在果树枝叶之间，前景遮挡镜头，浅景深，人物手拿桃子靠近脸部，笑着侧身但头肩方向一致，可以不看镜头。

强烈夏日自然光从侧后方穿过树叶，落在草帽边缘、脸颊、发丝和水果上，形成筛孔光斑、轻微眩光、边缘虚化和胶片颗粒，整体明亮鲜活。
```

## Example: Old Study Gufeng Room

```text
3:4 竖图，真实摄影，旧阁书案古风写真，低对比青灰雾化胶片质感，暗部抬起，柔焦，轻微颗粒，不要影楼精修

一位明确成年的虚构东亚女性，清冷鹅蛋脸，安静内敛气质，黑色长发低挽。淡雅古典妆，柔雾底妆，低饱和豆沙唇，眉眼干净，保留真实皮肤质感。

浅青灰色改良汉服上衣搭配米白长裙，衣料有细密织纹和轻微旧感，玉色发簪和简洁耳坠与旧阁空间呼应，避免影楼感和过度华丽。

前景是贴近镜头的旧木案边缘、手抄纸、半卷卷轴和白色纱帘虚影，纱帘可大面积遮挡画面边缘并明显柔焦；人物坐在书案旁，背景有鸟笼、黄绿色小鸟、散落谷粒、古书、砚台、旧瓷果盘、桃子、竹帘、窗棂、旧床榻和被风吹动的纱帘；道具不需要全部出现，只根据构图需求选取。

中距离半身到七分身构图，镜头略低并穿过书案前景，浅景深，人物低头垂眼，手指轻触纸页或卷轴边缘，不做大幅扭头回望。

窗外白雾逆光从侧后方透过竹帘和窗棂进入房间，落在纱帘、纸张边缘、发丝和木案上，形成柔和光束、轻微灰尘颗粒和旧木头潮气感，整体安静、有生活痕迹。
```
